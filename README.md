# Mare Nostrum LAB Thesaurus Plugin for Recogito

This is a fork of the [Recogito Geotagging Plugin](https://github.com/recogito/plugin-geotagging) modified for the Mare Nostrum LAB Platform.

It uses the same Recogito Studio plugin schema (Astro integration, admin settings, annotation-editor extension), but tags annotations with concepts from the Mare Nostrum LAB Thesaurus instead of geographic gazetteers. 

IMPORTANT. This fork adds the following relative to plugin-geotagging:

- Thesaurus tagging over SPARQL from https://thesaurus.mn.cenagis.edu.pl.
- Project admins can enable or disable individual dictionaries (amphora type, vessel form, chronology, material, and the rest of the Mare Nostrum LAB vocabularies) and optionally pre-fill search from the selected annotation text.
## Installation

Same as plugin-geotagging: install the package into your Recogito Studio client, register it, then restart.

1. In the recogito-client directory, add this plugin from a local path or your Git remote. The package name is mn-thesaurus-plugin.
2. Register it. Put mn-thesaurus-plugin in INSTALLED_PLUGINS in the client environment file. On older setups that still wire plugins in astro.config.mjs, import the default export and add it to integrations.
3. Restart the Recogito Studio client.

## Configuration

In Recogito project admin settings:

- Use selected annotation text as the thesaurus search query (on by default).
- Dictionaries: which MN thesaurus branches are searchable (Q449 amphora type, Q450 vessel form, Q451 vessel part, and others).

The thesaurus base URL and SPARQL endpoint are hardcoded to https://thesaurus.mn.cenagis.edu.pl.