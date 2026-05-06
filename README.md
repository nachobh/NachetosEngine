# NachetosEngine
UI Engine for web (HTML + CSS + JS) - Just a JSON parser/interpreter

## UI designed in JSON format

### JSON format

The JSON file/template will have this format:

```JSON
{
  "screens": [
    {
      "id": 1,
      "first": true,
      "title": "Hello world",
      "size": {
        "x": 100,
        "y": 100
      }
    }
  ]
}
```

### Decription of elements

app/game → This is the parent/main element/node without any name.
"screens" → This field represent the list of screens in the app.

## A little bit of history

Calling it an engine is a little bit over the top. It is more an HTML generator. Let me explain myself:

A current issue I've faced designing UIs, is not having a way to update the UI without publishing/updating the app in the Stores.

As an example, in Apple Store updates can take 1-2 days, making even the slightest change in the UI an enormous pain.

This project was inspired by @lordcuch from a small talk in BCN Game Fest while I was "crying" in desperation about my UI problems in Flutter.

This way, you can have all your UI elements on a JSON format, allowing you to update the UI without publishing a new version of your app.

As final goal, html result file should be compiled into different formats, so this "engine" serves not only as an HTML generator, but also as a multiplatform app designer.

