<a href="https://novel.sh">
  <img alt="Novel is a Notion-style WYSIWYG editor with AI-powered autocompletions." src="https://novel.sh/opengraph-image.png">
  <h1 align="center">Novel</h1>
</a>

<p align="center">
  An open-source Notion-style WYSIWYG editor with AI-powered autocompletions. 
</p>

## Introduction

[Novel](https://novel.sh/) is a Notion-style WYSIWYG editor with AI-powered autocompletions.

<br />

The `Editor` is a React component that takes in the following props:

| Prop                | Type                        | Description                                                                                                                                                                                | Default                                                                                                                                                |
| ------------------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `completionApi`     | `string`                    | The API route to use for the OpenAI completion API.                                                                                                                                        | `/api/generate`                                                                                                                                        |
| `className`         | `string`                    | Editor container classname.                                                                                                                                                                | `"relative min-h-[500px] w-full max-w-screen-lg border-stone-200 bg-white p-12 px-8 sm:mb-[calc(20vh)] sm:rounded-lg sm:border sm:px-12 sm:shadow-lg"` |
| `defaultValue`      | `JSONContent` or `string`   | The default value to use for the editor.                                                                                                                                                   | [`defaultEditorContent`](https://github.com/steven-tey/novel/blob/main/packages/core/src/ui/editor/default-content.tsx)                                |
| `extensions`        | `Extension[]`               | A list of extensions to use for the editor, in addition to the [default Novel extensions](https://github.com/steven-tey/novel/blob/main/packages/core/src/ui/editor/extensions/index.tsx). | `[]`                                                                                                                                                   |
| `editorProps`       | `EditorProps`               | Props to pass to the underlying Tiptap editor, in addition to the [default Novel editor props](https://github.com/steven-tey/novel/blob/main/packages/core/src/ui/editor/props.ts).        | `{}`                                                                                                                                                   |
| `onUpdate`          | `(editor?: Editor) => void` | A callback function that is called whenever the editor is updated.                                                                                                                         | `() => {}`                                                                                                                                             |
| `onDebouncedUpdate` | `(editor?: Editor) => void` | A callback function that is called whenever the editor is updated, but only after the defined debounce duration.                                                                           | `() => {}`                                                                                                                                             |
| `debounceDuration`  | `number`                    | The duration (in milliseconds) to debounce the `onDebouncedUpdate` callback.                                                                                                               | `750`                                                                                                                                                  |
| `storageKey`        | `string`                    | The key to use for storing the editor's value in local storage.                                                                                                                            | `novel__content`                                                                                                                                       |
