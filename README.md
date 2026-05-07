# NachetosEngine
UI Engine for web (HTML + CSS + JS) - Just a JSON parser/interpreter

## UI scheme designed in JSON format

### JSON format

The JSON file/template will have this format:

```JSON
{
  "title" : {
    "content": "Example Title"
  },
  "description" : {
    "content": "${example_description}"
  },
  "author" : {
    "content": "Ignacio Benito Herrero"
  },
  "languages": [
    {
      "iso": "en",
      "example_description": "Description",
      "example_screen": "Example screen",
      "hello_world": "Hello world!",
      "hello_world_dialog": "This is the hello world dialog."
    },
    {
      "iso": "es",
      "example_description": "Descripción",
      "example_screen": "Pantalla de ejemplo",
      "hello_world": "¡Hola mundo!",
      "hello_world_dialog": "Este es el diálogo de hola mundo."
    }
  ],
  "screens": [
    {
      "id": 1,
      "first": true,
      "title": {
        "content": "${hello_world}",
        "background-color": "transparent",
        "color": "white"
      },
      "size": {
        "x": 100,
        "y": 100
      },
      "border": {
        "color": "white",
        "width": 0.1
      },
      "background": {
        "color": "grey"
      },
      "buttons": [
        {
          "id": 1,
          "defaultFocused": true,
          "size": {
            "x": 10,
            "y": 5
          },
          "position": {
            "x": 80,
            "y": 85
          },
          "text": {
            "content": "${hello_world}",
            "background-color": "transparent",
            "color": "#1A1A1A"
          },
          "background": {
            "color": "#AEAEAE"
          },
          "action": {
            "name": "loadScreen",
            "args": [2]
          }
        },
        {
          "id": 2,
          "size": {
            "x": 10,
            "y": 5
          },
          "position": {
            "x": 20,
            "y": 85
          },
          "text": {
            "content": "Hasta la vista!",
            "background-color": "transparent",
            "color": "#1A1A1A"
          },
          "border": {
            "color": "red",
            "width": 5,
            "radius": 30
          },
          "background": {
            "color": "#AEAEAE"
          },
          "action": {
            "name": "exit"
          }
        }
      ],
      "dialogs": [
        {
          "id": 1,
          "size": {
            "x": 80,
            "y": 20
          },
          "position": {
            "x": 50,
            "y": 75
          },
          "border": {
            "color": "red",
            "width": 1,
            "radius": 50
          },
          "action-to-show": null,
          "text": {
            "content": "${hello_world_dialog}",
            "background-color": "white",
            "color": "#1A1A1A"
          },
          "z-index": 1
        }
      ],
      "pictures": [
        {
          "id": 1,
          "size": {
            "x": 80,
            "y": 20
          },
          "position": {
            "x": 50,
            "y": 75
          },
          "border": {
            "color": "red",
            "width": 0.1,
            "radius": 10
          },
          "action-to-show": null,
          "image": {
            "content": "image01.png",
            "background-color": "white",
            "color": "#1A1A1A"
          },
          "z-index": 1
        }
      ]
    },
    {
      "id": 2,
      "title": {
        "content": "${hello_world}",
        "background-color": "transparent",
        "color": "white"
      },
      "size": {
        "x": 100,
        "y": 100
      },
      "border": {
        "color": "white",
        "width": 0.1
      },
      "background": {
        "color": "white"
      },
      "buttons": [
        {
          "id": 1,
          "size": {
            "x": 10,
            "y": 5
          },
          "position": {
            "x": 20,
            "y": 85
          },
          "text": {
            "content": "Hasta la vista!",
            "background-color": "transparent",
            "color": "#1A1A1A"
          },
          "border": {
            "color": "red",
            "width": 0.1,
            "radius": 0.05
          },
          "background": {
            "color": "#AEAEAE"
          },
          "action": {
            "name": "exit"
          }
        }
      ]
    }
  ]
}
```

### Description of elements

- _title_:
- _description_:
- _content_:
- _screens_: This field represent the list of screens in the app.
- _blablabla_


## A little bit of history

Calling it an engine is a little bit over the top. It is more an HTML generator. Let me explain myself:

A current issue I've faced designing UIs, is not having a way to update the UI without publishing/updating the app in the Stores.

As an example, in Apple Store updates can take 1-2 days, making even the slightest change in the UI an enormous pain.

This project was inspired by @lordcuch from a small talk in BCN Game Fest while I was "crying" in desperation about my UI problems in Flutter.

This way, you can have all your UI elements on a JSON format, allowing you to update the UI without publishing a new version of your app.

As final goal, HTML result file should be compiled into different formats, so this "engine" serves not only as an HTML generator, but also as a multiplatform app designer.

