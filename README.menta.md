# pkg-mate-clipboard (Menta Linux)

Debian packaging of mate-clipboard (Clipman) 2.0.1 from
https://github.com/KeremSoke/mate-clipboard (tag v2.0.1; upstream HEAD).
No Debian/Salsa packaging exists, so `debian/` is written from scratch.

- Built with `-Dx11=enabled -Dwayland=enabled` (wlr/ext data-control + gtk-layer-shell).
- The panel applet is an in-process module (`InProcess=true`, `libmate-clipman-applet.so`).
- Version `2.0.1-1menta1`; bump with `dch -i` for menta rebuilds.
- Needs the menta mate-panel (`libmate-panel-applet-dev >= 1.29.2`); CI on plain
  Debian unstable fails until that package is installable.

CI builds on every push to `master`; tag `menta/<version>` publishes a release.
