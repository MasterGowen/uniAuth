# Django uniAuth

Django Unified Authentication System is an IDentity Provider built on top of [IdentityPython](https://idpy.org) stack.

This Release Candidate supports a SAML2 IDP, an OIDC Provider will be available in the next release.

## Features

uniAuth, as a SAML2 IDP, supports HTTP-REDIRECT and POST bindings, AuthnRequest with ForceAuthn but not AllowCreate NameIDPolicy, it simply ignore AllowCreate. Features set are:

- All already availables in [pysaml2](https://github.com/IdentityPython/pysaml2);
- Full Internazionalization support (i18n);
- Interactive Metadata Store definitions through the Admin Backend UI;
- Interactive ServiceProvider Federation through the Admin Backend UI;
- Customizable Template and style based on [AGID guidelines](https://www.agid.gov.it/it/argomenti/linee-guida-design-pa);
- MetadataStore and SP validations on save, to prevent faulty configurations in production environment;
- Optional and quite granular Agreement Screen;
- Many options definable for every SP, like:
    - signature and digest algorithms;
    - attributes release policies;
    - attribute rewrite and creation, fully configurable AttributeProcessors per SP, every aspect of attribute release can be customized from schratch;
    - selectable hashing algorithm for Computed NameID;
    - agreement screen message, availability, data consent form. 
- Configurable log rotation through uwsgi;
- Importable StoredPersistentID for each user, for migrations from other IDP;
- An LDAP web manager with a configurable app (`ldap_peoples`); 
- Multifactor support, as available in djangosaml2idp;
- Detailed but not huge logs.


## Documentation 
 - [Official Documentation @readthedocs]()

## Contribute

Feel free to contribute creating separate PR from dedicated branches for each feature.
Open an Issue if you want to talk before develop to reduce the risk to be unmerged for some latest reason.
All the things will be collected in a new roadmap to the next release candidate.

Still need to handle Continuous Integration with unit test.

## Author

Giuseppe De Marco
