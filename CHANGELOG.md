# Changelog

All notable changes to ```UtilityBelt``` will be noted in this file.

## 4.0.0

Now supports PHP 7.4, 8.0, 8.1, 8.2

### Fixes

* strtolower does not support null values in php 8+. Relevant code updated

### Breaking Changes

* Minimum PHP version is now PHP 7.4
* Behaviour of sort functions changes in php 8 when it comes to the order of values that are considered to be
  the same. PHP 8+ switches all sorting functions to be stable. This means that the values in a list that are
  identical are guaranteed to be in the same order in the output array. This is only a breaking change if
  the existing non guaranteed sort order was relied on https://lindevs.com/stable-sorting-functions-in-php-8-0.
  The test cases for a specific test in this repo were updated to account for this change.

## 3.0.1

### Minor changes

- Minor optimisations, annotations, and type declarations for >= PHP 7.0
- Reformat code to PSR-1/PSR-2 standards

## 3.0.0

### Breaking Changes

* Moved to new package and namespace
* Minimum PHP version is now PHP 7.0

### Repository Change

UtilityBelt has now been moved to our `rexlabsio` repository.

The following changes have occurred:

* Repository URL changed:
  `https://github.com/bkvfoundry/utility-belt` => https://github.com/rexlabsio/utility-belt-php
* Composer package name changed:
  `bkvfoundry/utility-belt` => `rexlabs/utility-belt`
* PHP namespace changed: `BkvFoundry\UtilityBelt` => `Rexlabs\UtilityBelt`

To install `composer require rexlabs/utility-belt:^3.0`

## 2.2.0

### Methods Added
* ArrayUtility::dotExists
* ArrayUtility::dotWrite
* ArrayUtility::dotMutate

### Other Changes
* Extend ArrayUtility::dotRead to handle nulls being passed in as the array
* Improved README including install instructions

## 2.1.0

### Methods Added
* ArrayUtility::first
* ArrayUtility::last
* ArrayUtility::firstKey
* ArrayUtility::lastKey

New methods added to ArrayUtility to make it easier to deal with function call results immediately without first assigning the result to another variable.

## 2.0.0

### Features
* CollectionUtility::keepKeys, ArrayUtility::keepKeys: removal action option added. Keys can now be deleted (default behaviour) or nullified.
* CollectionUtility::removeKeys, ArrayUtility::removeKeys: removal action option added. Keys can now be deleted (default behaviour) or nullified.
* ArrayUtility::map function that supports value, key, array being passed into the callback added.
* ArrayUtility::mapRecursive now passes three arguments to callback.

### Breaking Changes
* CollectionUtility::mapRecursive now passes three arguments (may break on calls to string based callbacks like "trim").
* ArrayUtility::map method signature now explicitly requires an array (brought in line with other method calls).

## 1.0.1

### Features
* Added support for sort/asort 

## 1.0.0

Initial release.
