### Features

- Scan Qr Codes using a smartphone camera or webcam.

### Demo
Checkout the [Demo](https://yudielcurbelo.github.io/react-qr-scanner/).

### Install

    yarn add @yudiel/react-qr-scanner

    npm install @yudiel/react-qr-scanner

### Usage

```jsx
import QrScanner from 'react-qr-scanner';

const App = () => {
  return (
      <QrScanner
          onDecode={(result) => console.log(result)}
          onError={(error) => console.log(error?.message)}
      />
  );
}
```
### Limitations
- Due to browser implementations the camera can only be accessed over https or localhost.
- Server side rendering won't work so only require the component when rendering in a browser environment.

### API
| Properties     | Types                                                                                           | Default Value                   | Description                                                       |
|----------------|-------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------------------------------------|
| constraints    | [MediaTrackConstraints](https://developer.mozilla.org/en-US/docs/Web/API/MediaTrackConstraints) | `{ facingMode: 'environment' }` | Specify which camera should be used (if available).               |
| containerStyle | `object`                                                                                        | none                            | Style object for the container element.                           |
| videoStyle     | `object`                                                                                        | none                            | Style object for the video element.                               |
| scanDelay      | `number`                                                                                        | `500`                           | The scan period for the QR hook.                                  |
| videoId        | `string`                                                                                        | `videoId`                       | The Id for the video element.                                     |
| onResult       | `function`                                                                                      | none                            | Scan event handler for result object.                             |
| onDecode       | `function`                                                                                      | none                            | Scan event handler for decode value.                              |
| onError        | `function`                                                                                      | none                            | Scan event handler for error object.                              |
| ViewFinder     | `component`                                                                                     | none                            | ViewFinder component to rendering as overlay in the video element |
| hideCount      | `boolean`                                                                                       | `true`                          | Hide the scanned count as overlay in the video element            |
