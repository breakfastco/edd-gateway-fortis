# edd-gateway-fortis

WordPress plugin. Add-on for Easy Digital Downloads. Adds a [FortisPay](https://fortispay.com/) payment option to Easy Digital Downloads. Implements the [Fortis Elements API](https://docs.fortis.tech/v/1_0_0.html#/rest/elements/overview).

&nbsp;

## FILTER HOOKS

### Change Transaction Description

`edd_gateway_fortis_charge_description`

Change the description saved with the transaction at Fortis. Defaults to "Easy Digital Downloads".

#### Example

```
<?php
add_filter( 'edd_gateway_fortis_charge_description', 'eddgf_change_description' );
/**
 * Changes the description on all charges to "WordPress plugins".
 *
 * @return string
 */
function eddgf_change_description() {
	return __( 'WordPress plugins', 'edd-gateway-fortis-customizations' );
}

```

### Change the Theme

`edd_gateway_fortis_elements_theme`

Change the theme of Fortis Elements. [Supports 'default' and 'dark'](https://docs.fortis.tech/v/1_0_0.html#/rest/elements/configuration-options).  Defaults to 'default'.


### Change the Font Size

`edd_gateway_fortis_elements_font_size`

Change the font size. Defaults to '17px'.
