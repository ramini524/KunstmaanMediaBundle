# Intro

A field for media references. It has a "choose" button which opens a popup where you can select your media item from the media repository.

## Example Usage:

```php
$builder->add('ogImage', 'media', array(
    'mediatype' => 'image',
    'label' => 'OG image'
));
```

## Options:

mediatype:
	type: string
	default: null
	description:
		You can specify a specific mediahandler by its name, when this is null all media items are possible.
		Knows possible values are: image|file|remotevideo|remoteslide

## Parent type:

form

## Class:

Kunstmaan\MediaBundle\Form\Type\MediaType