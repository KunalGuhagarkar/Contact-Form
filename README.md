# Contact Form

An accessible, no-JavaScript HTML contact form, built as a solution to the [roadmap.sh Contact Form project](https://roadmap.sh/projects/contact-form).

The goal is to practice the fundamentals of real HTML forms: proper labels, grouped controls, built-in browser validation, and understanding how a form turns into an HTTP request. The page is intentionally unstyled; styling is covered in a later roadmap.sh project.

## Features

- Semantic `<form>` using `method="post"` and a placeholder `action` URL
- Every input paired with a real `<label>` (`for` / `id`), not just a placeholder
- Browser-native validation using `required`, `minlength` and `type="email"`
- Radio buttons grouped in a `<fieldset>` with a `<legend>`
- Descriptive submit button text
- Correct head metadata: `<title>`, `<meta charset>` and `<meta viewport>`
- Zero JavaScript, zero dependencies

## Form fields

| Field | Control | Validation |
| --- | --- | --- |
| Full name | `<input type="text">` | Required |
| Email | `<input type="email">` | Required, must be a valid email |
| Subject | `<select>` with 3+ `<option>`s | n/a |
| Message | `<textarea>` | Required, with a `minlength` |
| How did you hear about us? | `<input type="radio">` group in a `<fieldset>` | n/a |
| Newsletter | `<input type="checkbox">` | Optional |

## Project structure

```
Contact-Form/
├── src/
│   └── index.html
└── README.md
```

## Getting started

No build step or installation is needed.

1. Clone the repository:

   ```bash
   git clone https://github.com/KunalGuhagarkar/Contact-Form.git
   cd Contact-Form
   ```

2. Open `src/index.html` in your browser.

   Or serve it locally, for example:

   ```bash
   npx serve src
   ```

## Seeing the form become a request

1. Open the page and press `F12` to open DevTools.
2. Go to the **Network** tab and tick **Preserve log**.
3. Fill in the form and submit it.
4. Click the request and look at the **Payload** tab. You will see the `name=value` pairs the form sent, which is exactly what a backend would receive.

Since the `action` is a placeholder URL, the request will fail or go nowhere. That is expected, as there is no backend.

## What I learned

- A placeholder is not a label. Labels are what screen readers and click targets rely on.
- `<fieldset>` and `<legend>` give related controls (like radio buttons) a shared, announced context.
- The `name` attribute decides what is sent to the server, while `id` is only for linking labels.
- Browser validation is a UX convenience, not a security boundary. A server must always validate the data again.

## Credits

Project idea from [roadmap.sh](https://roadmap.sh/projects/contact-form).

## Author

[KunalGuhagarkar](https://github.com/KunalGuhagarkar)