# FluentUI React Native

FluentUI React Native is a javascript component library that provides developers with controls that are part of the [Fluent Design System](https://www.microsoft.com/design/fluent/). These controls are built on [React Native](https://reactnative.dev/) and fully customizable.

FluentUI React Native is still in the alpha stages of development for both the components and the repo. We encourage anyone who is interested in getting an early glimpse of our plans to download and use our components, but please note that you may hit bumps along the way. Please leave us feedback or file issues if you run into bumps, and we will continue to improve the quality of the repo.

## Getting Started

If you have an existing React Native project, it's easy to begin using FluentUI React Native. If you need to setup a new React Native project, please see the [React Native Windows Getting Started documentation](https://microsoft.github.io/react-native-windows/docs/getting-started).

### Prerequisites

- [Standard React Native dependencies](https://reactnative.dev/docs/environment-setup)
- [Node.js](https://nodejs.org/en/download/)

### Create New React Native project (if needed)

1. Follow the instructions on the [React Native Windows Getting Started documentation](https://microsoft.github.io/react-native-windows/docs/getting-started) to create a React Native project.

2. Navigate to the root folder of your project, and use npm to install the package:

```
 npm i @fluentui/react-native
```

3. After successful installation, you can test the package by importing components at the top of your app's entry file, e.g. `App.js`:

```
 import { Checkbox } from '@fluentui/react-native';
```

4. After importing the @fluentui/react-native package, you can use components such as `Text` and `Checkbox` in your JSX.

```
// In App.js in a new project
import React from 'react';
import { View, Text } from 'react-native';
import { Checkbox } from '@fluentui/react-native';
function HelloWorldApp() {
  return (
    <View
      style={{
        flex: 1,
        justifyContent: "center",
        alignItems: "center"
      }}>
      <Text>Hello, world!</Text>
      <Checkbox label="Hello World Checkbox"/>
    </View>
  )
}
export default HelloWorldApp;
```

## Documentation

### Components and Controls

Our component documentation is hosted on the [FluentUI documentation](https://developer.microsoft.com/fluentui).

### Theming framework

Our FluentUI framework documentation is found in this repository alongside the implementation.

- [Theming Overview](./packages/framework/theming-react-native/README.md)
- [StyleSheets](./packages/framework/themed-stylesheet/README.md)
- [Customizing Theme Settings](./packages/framework/themed-settings/README.md)
- [Theme Registry](./packages/framework/theme-registry/README.md)
- [Tokens](./packages/framework/foundation-tokens/README.md)
- [Settings and Slots](./packages/framework/foundation-settings/README.md)
- [Compose](./packages/framework/foundation-compose/README.md) and [Composable](./packages/framework/foundation-composable/README.md)

## Developing in the repo

### Yarn + Lerna

This repo is set up as a monorepo using Lerna + Yarn workspaces. The yarn commands will trigger the lerna commands which will execute yarn commands in each package. To install yarn, please follow instructions in the [Yarn documentation](https://classic.yarnpkg.com/en/docs/install/).

### Setup your development environment

To start developing in the repository you can:

1. `git clone https://github.com/microsoft/fluentui-react-native.git`
1. `cd fluentui-react-native`
1. `yarn`
1. `yarn build`

After a successful yarn build, you can explore FluentUI Tester, our demo application to play with each of the controls. To run FluentUI Tester, please follow instructions in the [FluentUI Tester readme](./apps/fluent-tester/README.md).

### Beachball

This repo manages semantic versioning and publishing using [Beachball](https://github.com/microsoft/beachball). When contributing, make sure to run the following before making a pull request:

1. `yarn change` will take you through a command line wizard to generate change files
2. Make sure to commit and push the newly generated change file

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
