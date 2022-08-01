![MagicModal](https://user-images.githubusercontent.com/50031755/182190421-708be214-503e-4aeb-9311-0a7151805072.png)
_A modal component that can be used imperatively from anywhere!_

## React Native Magic Modal 🦄

Do you find using modals in React Native to be a bit of a pain? Trying to keep control of its open state and repeating the code everywhere you want to use it can be pretty tedious.

And the problem only gets worse when you try to create complex flows, where one modal opens another with conditionals in place. Once you get past two modals, your main component is a mess, and the state is all over the place.

This library thoughtfully encapsulates complex concepts to provide a smooth experience when using React modals, inside or outside components (In Sagas, for example!)

Take a look to a in-depth explanation of its concepts on its [Medium article](https://medium.com/@gabrieltaveira/you-have-been-using-react-native-modals-wrong-9b8c17de2f96).

## 📸 Examples

| IOS                                                                                                                           | Android                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://user-images.githubusercontent.com/50031755/155215573-df8f20fb-9b3f-4ce6-9d48-2afa8cb41daa.gif" height=600/> | <img src="https://user-images.githubusercontent.com/50031755/155215547-d2b45f33-264e-4c90-8ff1-e33b72e2c3b1.gif" height=600/> |

## 🛠 Installation

```sh
yarn add react-native-magic-modal
```

## ⚙️ Usage

First, insert a `MagicModalPortal` in the top of the application.

```js
import { MagicModalPortal } from 'react-native-magic-modal';

export default function App() {
  return (
    <SomeRandomProvider>
      <MagicModalPortal />  // <-- On the top of the app component hierarchy
      <Router /> // Your app router or something could follow below
    </SomeRandomProvider>
  );
}
```

Then, you are free to use the `magicModal` as shown from anywhere you want.

```js
// ...
import { magicModal } from 'react-native-magic-modal';

// ...
const ExampleModal = () => (
  <TouchableOpacity onPress={() => magicModal.hide('hey')}>
    <Text>Test!</Text>
  </TouchableOpacity>
);

const result = await magicModal.show(ExampleModal);
console.log(result); // Returns 'hey' when the modal is closed by the TouchableOpacity.
```

See [example](example/src) to understand in practice.

## 📖 Documentation

The docs are located [here](https://gstj.github.io/react-native-magic-modal/) in the project's [Github Pages](https://gstj.github.io/react-native-magic-modal/)

## 👨‍🏫 Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## ⚖️ License

[MIT](LICENSE)
