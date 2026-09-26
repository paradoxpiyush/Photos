# App icon: raster set (the artwork is a raster illustration, no vector master).
# Regenerate after replacing io.github.paradoxpiyush.Photos.Source.png, e.g.:
#   for s in 16 24 32 48 64 128 256 512; do
#     magick io.github.paradoxpiyush.Photos.Source.png -filter Lanczos -resize ${s}x${s} \
#       -alpha set -strip -define png:compression-level=9 \
#       hicolor/${s}x${s}/apps/io.github.paradoxpiyush.Photos.png
#   done
icon_sizes = ['16', '24', '32', '48', '64', '128', '256', '512']

foreach size : icon_sizes
  icon_dir = 'hicolor' / '@0@x@0@'.format(size) / 'apps'
  install_data(
    icon_dir / 'io.github.paradoxpiyush.Photos.png',
    install_dir: datadir / 'icons' / icon_dir,
    rename: '@0@.png'.format(app_id),
  )
endforeach

symbolic_dir = 'hicolor' / 'symbolic' / 'apps'

install_data(
  symbolic_dir / 'io.github.paradoxpiyush.Photos-symbolic.svg',
  install_dir: datadir / 'icons' / symbolic_dir,
  rename: '@0@-symbolic.svg'.format(app_id),
)
