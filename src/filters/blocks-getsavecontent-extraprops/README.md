# blocks.getSaveContent.extraProps

Allows filtering of the props for the `save` function.

[Offical docs](https://wordpress.org/gutenberg/handbook/designers-developers/developers/filters/block-filters/#blocks-getsavecontent-extraprops)

## Example
In this example, we set all of the blocks to have a background color of red.

```js
const { addFilter } = wp.hooks;

function addSaveProps( props ) {
	return Object.assign( props, { style: { background: 'red' } } );
}

addFilter( 'blocks.getSaveContent.extraProps', 'my-custom-namespace', addSaveProps );
```
