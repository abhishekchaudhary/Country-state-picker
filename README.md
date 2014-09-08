Country-state-picker
====================

A cool dropdown picker to select country and state.

## How to Use

* Include the crs.min.js file in your webpage.
* Add two <select> fields in the appropriate locations in your form.
* Give the country field a class of crs-country.
* Now we need to map each country field to its corresponding region field so the script knows what to update when a    country is selected. Add an attribute to the country dropdown: data-region-id="TEST" where TEST is any string. Now   Give the region dropdown an id of "TEST".


## Default "Please select" Values

If you want to add default "Please select" options to either the country or region fields, just go ahead and add it directly in the markup. The script will append the country and region <option> fields - not overwrite them.

## Adding default values for each field

If your form is used for people returning to it (e.g. "Edit Contact Info" or whatever), you'll need the country and region fields to be prefilled with the appropriate value on page load. To do that, just add a data-default-value="" attribute to each element containing the country / region value last saved. Note: the region value will only ever be populated if the country field is as well.

## List of data-* attributes

This lists all the available data-* attributes that you can add to the country/region fields to customize the appearance and behaviour.

## country fields

* data-region-id - required. This should contain the ID of the region field that it's being mapped to.
* data-default-option - optional. Default: "Select country". This determines the default, blank option display value.
* data-default-value - optional. The default selected value in the country dropdown (e.g. "Canada")
* data-value="2-char" - optional. The default behaviour is for the value attributes of the country dropdown options to be the full country name. If you'd rather use a 2-char code, add this attribute. Note: the 2-char codes are mostly ISO standard 2-char country codes, but not all. They are, however, unique across the dataset.

## region fields

* data-blank-option - before the user selects a country, there's a single displayed which by default is the "-" character.
* data-default-option - optional. Default: "Select region". This determines the default, blank option display value that shows up after a user has selected a country.
* data-default-value - optional. The default selected value in the region dropdown (e.g. "British Columbis")
