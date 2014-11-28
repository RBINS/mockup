Changelog
=========

1.8.3 (unreleased)
------------------

New patterns:

- Add "markspeciallinks" pattern.
  [agitator, fulv]

- Add mimetype selector pattern for textareas.
  [thet]

- Add Cookie Trigger pattern. It shows a DOM element if browser cookies are
  disabled.
  [jcbrand]

- Add Inline Validation pattern for z3c.form, Archetypes and zope.formlib
  inline validation.
  [jcbrand]

- Add passwordstrength pattern based on the ``zxcvbn`` library. Ref: #433.
  [lentinj]


Fixes and enhancements:

- Modal Pattern: If ``data-base-url`` attribute is available on the body, use
  it. Otherwise search for a ``<base>`` tag. Plone 5 dropped the usage of base
  tags.
  [ACatlla, thet]

- Fix less variable overrides on resourceregistry pattern when building
  CSS from less resources
  [datakurre]

- Depend on ``tinymce-builded`` 4.1.6, include TinyMCE copy and sed
  configuration in here and fix some sed tasks.
  Revert cd89d377e10a28b797fd3c9d48410ad6ad597486: "Remove bower dependency on
  ``tinymce-builded``, since the ``tinymce`` dependency already points to the
  official builded ``tinymce-dist`` reposotory." ``tinymce-dist`` doesn't
  include the language files, which are needed.
  [thet]

- Fix thememapper pattern.
  [ebrehault]

- Fix broken HTML tag on structure pattern's ``actionmenu.xml``.
  [datakurre]

- File label cannot be used as path.
  [ebrehault]

- Include ``docs.less`` from ``mockup-core``, which can better be reused. Use
  ``@{bowerPath}`` less variable where possible.
  [thet]

- Eventedit pattern: Use more specific CSS selectors, so that switching
  whole_day on and off doesn't hide the publication date's time component.
  Refs: https://github.com/plone/plone.app.event/pull/169
  [thet]

- Depend on newer `mockup-core` version.
  [thet]

- Fix tests to run within reorganized folder structure from 1.8.2.
  [thet]


1.8.2 (2014-11-01)
------------------

- Reorganize folders so that javascript is included in the cooked egg.
  [esteele]


1.8.1 (2014-11-01)
------------------

- Size for modals may be specified.
  [bloodbare]

- Include vagrant setup as an install option for Mockup.
  [frapell]


v1.8.0 (2014-10-26)
-------------------

- Bower updates, except pickadate and backbone.paginator.
  [thet]

- Cleanup: Remove unused ``*._develop.js`` bundles. Remove unused bundles
  ``toolbar`` and ``tiles``. Remove unused bower dependencies ``domready``,
  ``respond`` and ``html5shiv``. Move all NixOS plattform specific ``*.nix``
  config files to a ``.nix`` subdirectory. Fix index.html markup. Remove unused
  ``__init__.py``.
  [thet]

- Remove licensing and author information from source files. Fixes #421 Fixes
  #422.
  [thet]

- Package metadata changes including removal of deprecated version specifier
  from bower.json.
  [thet]

- Remove bower dependency on ``tinymce-builded``, since the ``tinymce``
  dependency already points to the official builded ``tinymce-dist``
  reposotory. Raise TinyMCE version to 4.1.6.
  [thet]

- Fix Makefile for node versions < and >= 0.11.x.
  [petschki, thet]
