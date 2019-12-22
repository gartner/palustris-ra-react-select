# palustris-ra-react-select
An input-component for React-admin, for use inside a ReferenceArrayInput. Has the ability to create new entries.

The component is based on [react-select](https://react-select.com/home).

The component will only work as expected if placed inside a `<ReferenceArrayInput>`-component
 
## Properties
__isCreatable__ *(bool)* If true, you can enter a value that is not present in the choices, and it will be created in the resource from which the choices are taken from.

__labelField__ *(string)* Name of the field that contains the label in choices. Defaults to 'label'.

__valueField__ *(string)* Name of the field that contains the value in choices. Defaults to 'id'.

## Notes
The material-ui theme used by react-admin has overflow: hidden, which in some cases will make some of the select-menu hidden, if the field is placed at the bottom of a form. This can be changed by customizing the theme:

```typescript jsx
import { createMuiTheme } from '@material-ui/core/styles';

const myTheme = createMuiTheme({
    overrides: {
        MuiCard: {
            root: {
                overflow: "overflow",
            },
        },
    },
});

const App = () => (
    <Admin theme={myTheme} dataProvider={}>
    </Admin>
);
```
