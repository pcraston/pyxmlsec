pyxmlsec
========

pyxmlsec_x86_64

A small patch, that wasn't commit to official pyxmlsec,
that allows it to compile and install into x86_64 arch.

Patch:
<code>
--- pyxmlsec-0.3.0/setup.py     2006-01-01 15:43:37.000000000 -0200
+++ pyxmlsec-0.3.0/setup.py     2009-11-10 17:57:29.390253522 -0200
@@ -182,7 +182,8 @@
                define_macros = define_macros,
                include_dirs  = include_dirs,
                library_dirs  = library_dirs,
-               libraries     = libraries
+               libraries     = libraries,
+               extra_compile_args = ['-DXMLSEC_NO_SIZE_T']
                )

 doclines = __doc__.split("\n")
</code>
