project('arcmenu',
  version: '3.38.8',
  license: 'GPL3'
)

gnome = import ('gnome')
i18n = import('i18n')

prefix = get_option('prefix')
datadir = join_paths (prefix, get_option('datadir'))
schema_dir = join_paths(datadir, 'glib-2.0', 'schemas')

extensions_dir = join_paths(prefix, 'share', 'gnome-shell', 'extensions', 'arc-menu@pardus.org.tr')

install_data([
    'constants.js',
    'controller.js',
    'convenience.js',
    'COPYING',
    'extension.js',
    'helper.js',
    'menuButton.js',
    'menuWidgets.js',
    'metadata.json',
    'placeDisplay.js',
    'prefs.js',
    'prefsWidgets.js',
    'README.md',
    'search.js',
    'utils.js'
  ],
  install_dir: extensions_dir
)

install_subdir('menulayouts', install_dir : extensions_dir)

install_subdir('media', install_dir : extensions_dir)

subdir(
  'po'
)
subdir(
  'schemas'
)

meson.add_install_script('meson_post_install.py')
