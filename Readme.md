## &lt;actindo-toggle-group&gt;
`<actindo-toggle-group>` automatically generates a list of paper-buttons bases on and array.
It allows to toggle only a single button with the group. It is possible to select items using the arrow keys.

## Example
The following example creates a toggle group of three items that are aligned vertically.
```
<dom-module id="your-element">
    <template>
        <actindo-toggle-group
                    items="[[items]]"
                    value="{{returnValue}}"
                    value-field="key"
                    display-field="display"
                    selected-item="{{selectedItem}}"
                    allow-deselect
                    class="vertical"
        ></actindo-toggle-group>
    </template>
    <script>
    class YourElement extends Polymer.Element {
        static get is() { return 'your-element';}
        static get properties()
        {
            return {
                items: {
                    type: Array,
                    value: [
                        {
                            key: "key1",
                            display: "value1"
                        },
                        {
                            key: "key2",
                            display: "value2"
                        },
                        {
                            key: "key3",
                            display: "value3"
                        }
                    ]
                },
                returnValue: {
                    type: String
                },
                selectedItem: {
                    type: Object
                }
            };
        }
    }
    customElements.define( YourElement.is, YourElement );
    </script>
</dom-module> 
```
