# GETTING STARTED WITH SERASI

<Subtitle>
  Use the Serasi components to solve common UI problems like layout, typography, displaying product or data input. When no component fits
  your case, either extend an existing one or create a new one on guild components.
</Subtitle>

## Installation

Serasi is typically installed into a project managed by npm or yarn as a JavaScript package from the Hafizfattah GitHub Package Registry.

Now add this project as a dependency of your project with:

```
  yarn add @Hafizfattah/serasi-web
```

or

```
  npm install @Hafizfattah/serasi-web
```

## How to Use

We ship two types of module formats: CommonJS and ESModules. Most modern build tools will use the latter resolved from the package.json module entry. To keep our module code as clean as possible, we try to use the latest possible ECMAScript version as target for our transpilation. So if you have to support browsers that don't support certain modern ECMAScript features, you may want to configure your build tools accordingly.

### Import as Global Component

With this kind of import, you will include the whole bundle of the library, but you can use all components directly.

```
import { SerasiProvider } from '@Hafizfattah/serasi-web'
import * as React from 'react'
import * as ReactDOM from 'react-dom'

ReactDOM.render(
  <SerasiProvider>
    <App />
  </SerasiProvider>,
)
```

### Selective Import

Don't forget to install babel-import-plugin and setup babel config, otherwise you'll include the whole bundle and can't resolve component's style

```
import { Button, TextField } from '@Hafizfattah/serasi-web'

const MyComponent = () => (
 <div>
  <TextField label="Search" />
  <Button variant="primary" size="large">
    Submit
  </Button>
 </div>
)
```
