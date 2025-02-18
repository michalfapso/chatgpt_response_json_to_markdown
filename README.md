[Online tool here](https://michalfapso.github.io/chatgpt_response_json_to_markdown/index.html)

## Math notation
By checking the "includes math" checkbox it also converts math markdown notation because the one used by ChatGPT doesn't seem to be well supported by markdown editors with a preview. E.g. [xyzeditor.com](https://www.xyzeditor.com), [stackedit.io](https://stackedit.io/app) or VSCode with a markdown preview extension work well.

- inline from `` `2 + 2` `` to `$2 + 2$`
- blocks from
  ```
  \[
    y = 2 + 3x
  \]
  ```
  to
  ```
  $$
    y = 2 + 3x
  $$
  ```

## Example
Input JSON:
```json
{
  "messages": [
    {
      "role": "user",
      "content": [
        {
          "type": "text",
          "text": "How are you?"
        }
      ]
    },
    {
      "role": "assistant",
      "content": [
        {
          "type": "text",
          "text": "I'm fine, thanks."
        }
      ]
    }
  ]
}
```

Output Markdown:
```markdown
# Role: user
How are you?

<br/><br/><br/>
# Role: assistant
I'm fine, thanks.

<br/><br/><br/>
```
