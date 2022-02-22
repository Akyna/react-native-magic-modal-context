# react-native-magic-modal 🦄

A modal component that can be used imperatively from anywhere!

| IOS                                                                                                                           | Android                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://user-images.githubusercontent.com/50031755/155215573-df8f20fb-9b3f-4ce6-9d48-2afa8cb41daa.gif" height=600/> | <img src="https://user-images.githubusercontent.com/50031755/155215547-d2b45f33-264e-4c90-8ff1-e33b72e2c3b1.gif" height=600/> |

## Installation

```sh
yarn add react-native-magic-modal
```


## Usage

First, insert a `MagicModalPortal` in the top of the application.

```js
import { MagicModalPortal } from 'react-native-magic-modal';

export default function App() {
  return (
    <View>
      <MagicModalPortal />
      // <Router />
    </View>
  );
}
```

Then, you are free to use the `magicModal` as shown from anywhere you want.

```js
import { magicModal } from 'react-native-magic-toast';

// ...

const ExampleModal = () => <Text testID={testId}>Test!</Text>
magicModal.show(() => <ExampleModal />);
```
See [example](example/src) to understand more complex uses.

## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT
