
# Prérequis


///usr/lib/python2.7/site-packages

```
apk update
apk add py-lxml
apk add py-pillow
apk add build-base libffi-dev freetype-dev jpeg-dev libwebp-dev tiff-dev libpng-dev lcms2-dev openjpeg-dev zlib-dev

pip install --upgrade pillow

#pip install zipfile36

ln -s /opt/docs/sphinx-docxbuilder/ /usr/lib/python2.7/site-packages/sphinx-docxbuilder

sphinx-build -b docx -t docx -d _build/doctrees -D latex_paper_size=a4 . _build/docx

```

in conf.py
```

extensions = ['sphinx.ext.graphviz','sphinx-docxbuilder']
```