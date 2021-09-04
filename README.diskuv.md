# Build

1. `_S='Z:\source\opam'; eval $(opam env --switch "$_S" --set-switch | awk 'BEGIN{FS="="} $1 != "PATH" {print}') ; eval $(opam env --switch "$_S" --set-switch | awk 'BEGIN{FS="="} $1 == "PATH" {print}') ; PATH=$(/usr/bin/cygpath --path "$PATH")`
2. `opam install . --with-test --deps-only`
   which will fail on dose3. But keep the other packages.
3. `opam uninstall cudf`
4. ```bash
   git clean -d -x -f src_ext && make -C src_ext clone-pkg
   PKGSKIP=() && for i in findlib ocamlbuild cppo extlib re ocamlgraph cudf; do PKGSKIP+=(-o $i.pkgbuild); done
   PKGSKIP=() && for i in dune-local findlib ocamlbuild cppo extlib re ocamlgraph; do PKGSKIP+=(-o $i.pkgbuild); done
   rm -f src_ext/dose3.pkgbuild src_ext/mccs.pkgbuild src_ext/cudf.pkgbuild && make -C src_ext "${PKGSKIP[@]}" mccs.pkgbuild cudf.pkgbuild dose3.pkgbuild
   ```
5. `MSVS_PREFERENCE='VS16.*;VS15.*;VS14.0;VS12.0;VS11.0;10.0;9.0;8.0;7.1;7.0' ./configure --enable-developer-mode`
   (`--enable-developer-mode` is optional)
6. `make`
7. Optional: `make install`
