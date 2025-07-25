## chara_card_v3 PList+AliChat Workflow
1. Evaluate `st3-card-example.json` for structure and available placeholders.
2. Check `1Todo` directory for available characters to convert, unless stated otherwise.
- If stated, check `2Completed` directory for conflicting characters. If any, prompt user to resolve conflicts before proceeding.
3. Check and evaluate the ENTIRE information of a character database from the `1Todo` directory.
- Database usually begin with dialogues, then character information at the end.
- It's usually best to check via `wc` to reference text size.
4. Evaluate `PListPromptTemplate.json` and `AliChatPromptTemplate.json` for structure and conversion.
5. Temporarily stage character database conversion for `PList` and `AliChat` formats.
6. Clone the chara_card_v3 template `st3-card-example.json` and rename it to override placeholder with character-name `<character-name>.json`.
- Don't append `DB` to `<character-name>.json`.
7. Edit the cloned template to replace placeholders with character-specific information, including PList and AliChat.
- Greetings/firstMessage (including alternative and group greetings), which should be AliChat (singleturn: narration, dialogue; keep it short) formatted, open-ended, and dependent on scenario, which must only include `{{char}}`.
- Scenario should be open-ended and relevant to the character.
- Tags (limit to 6) should also be relevant to the character, including traits, MBTI, and enneagram.
- Personality summary should include three sentences.
- AliChat should begin with `<START>` before multiturn.
- Talkativeness should be between 0 and 1.
- Avoid changing non-placeholder values, including creation date, unless stated otherwise.
- `character_version` should always be `0.1.0`.
8. Validate the converted character card by checking the output against the original character database.
9. Review syntax and formatting of the converted character card.
10. Move completed character database and `<character-name>.json` from `1Todo` to `2Completed`.
11. Self check
- Make sure the card follows AliChat formatting rules.
- Lint check JSON.
- Tags should include reference, residence prefix, role, title, or any relevant keywords.
- Clean up temporary files made in this session if needed.
- Ensure filenames are consistent.
12. Report brief bullet point summary.
