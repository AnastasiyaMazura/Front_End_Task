# Timezynk

## The task

```
AS a user
I WOULD like to be able to use emoji in messages
IN ORDER to convey my meaning and feelings better
Support both picker and slack-like emoji codes for a good experience on both mobile and web.
```

## Explanations to the solution

1. For the emoji picker implementation, the [emoji-picker-react](https://www.npmjs.com/package/emoji-picker-react) library was used.
2. Since Slack does not provide any API to get the full emojis codes dictionary, it was decided to use the [emojibase](https://emojibase.dev/) package. It's most likely that emojibase does not contain the full list of Slack codes, so here are examples of codes that do exist in this library for testing: ":cucumber:", ":smile:", ":beaming_face:", etc.
3. Regarding the mobile version, there are some concerns that emoji picker is necessary because the virtual keyboard on tablets and mobiles contains its own emoji tab. Moreover, handling the proper size of the picker in landscape mode with the opened keyboard will also be required. This solution does not provide mentioned handling, but if necessary, it can be done for example via the [use-detect-keyboard-open](https://www.npmjs.com/package/use-detect-keyboard-open) hook by allowing the user to utilize the emoji picker only when the keyboard is closed.
