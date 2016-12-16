ansible-role-locale
===================

Ansible role to configure system-wide locale settings.

The abstracts generation and setting of system locales.

Requirements
------------

None

Role Variables
--------------

The character set defined by `locale_character_set` will be used for all locale sets. Defaults to `UTF-8`.

	locale_character_set: UTF-8

The locale set for `locale_lang` will be used for all variables that are not explicitly set. Defaults to `en_US`.

	locale_lang: en_US

Programs which use `gettext` for translations respect the `locale_language` variable in addition to the usual variables. This allows to specify a list of locales that will be used in that order. If a translation for the preferred locale is unavailable, another from a similar locale will be used instead of the default. Defaults to `en, de`

	locale_language:
	  - en
	  - de

The `locale_type` variable defines the interpretation of byte sequences as characters (e.g., single versus multibyte characters), character classifications (e.g., alphabetic or digit), and the behavior of character classes. This variable will only be set in configuration when defined. Defaults to not set.

	locale_ctype:

The `locale_numeric` parameter determines the formatting rules used for nonmonetary numeric values—for example, the thousands separator and the radix character (a period in most English-speaking countries, but a comma in many other regions). This variable will only be set in configuration when defined. Defaults to not set.

	locale_numeric:

The `locale_time` parameter defines the formatting used for date and time values. For example, most of Europe uses a 24-hour clock versus the 12-hour clock used in the United States. This variable will only be set in configuration when defined. Defaults to not set.

	locale_time:

The `locale_collate` parameter defines the collation rules used for sorting and regular expressions, including character equivalence classes and multicharacter collating elements. This variable will only be set in configuration when defined. Defaults to not set.

	locale_collate:

The `locale_monetary` parameter defines the formatting used for monetary-related numeric values. This variable will only be set in configuration when defined. Defaults to not set.

	locale_monetary:

The `locale_messages` parameter defines the language in which messages are displayed and what an affirmative or negative answer looks like. This variable will only be set in configuration when defined. Defaults to not set.

	locale_messages:

The `locale_paper` parameter defines the settings relating to the dimensions of the standard paper size (e.g., US letter versus A4). This variable will only be set in configuration when defined. Defaults to not set.

	locale_paper:

The `locale_name` parameter defines the formats used to address persons. This variable will only be set in configuration when defined. Defaults to not set.

	locale_name:

The `locale_address` parameter defines the formats (e.g., postal addresses) used to describe locations and geography-related items. This variable will only be set in configuration when defined. Defaults to not set.

	locale_address:

The `locale_telephone` parameter defines the formats to be used with telephone services. This variable will only be set in configuration when defined. Defaults to not set.

	locale_telephone:

The `locale_measurement` parameter defines formats relating to the measurement system in the locale (i.e., metric versus US customary units). This variable will only be set in configuration when defined. Defaults to not set.

	locale_measurement:

The `locale_identification` parameter defines the settings that relate to the metadata for the locale. This variable will only be set in configuration when defined. Defaults to not set.

	locale_identification:

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: knowhy.ansible-role-locale }

License
-------

BSD

Author Information
------------------

This role was created in 2016 by Henrik Pingel.
