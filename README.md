# sphinx-internationalization-test

1. `pip install Sphinx sphinx-intl python-levenshtein`

2. `sphinx-quickstart docs`
    ```
    > Separate source and build directories (y/n) [n]:
    > Project name: Sphinx internationalization test
    > Author name(s): Damian Krawczyk
    > Project release []: 0.0.1
    > Project language [en]: 
    ```

3. `vi docs/conf.py`

```
# https://www.sphinx-doc.org/en/master/usage/advanced/intl.html#quick-guide
locale_dirs = ['locale/']   # path is example but recommended.
gettext_compact = False     # optional.

# https://docs.readthedocs.io/en/stable/guides/manage-translations.html
gettext_uuid = True
```

4. Run VSC tasks to generate files for translation.

    > **NOTE**
    > 1. Default language is set to `pl` - Polish.
    > 2. You need to configure first `virtualenvPath` in `.vscode/settings.json` tu run VCS tasks.

    - Internationalization - build gettext
    - Internationalization - intl update

5. Translate generated `*.po` files.
6. Run VSC task to see translated page.
    - Internationalization - build html
7. Push to repository.
8. Configure project in RTD.

    https://docs.readthedocs.io/en/stable/localization.html
## More resources

- https://www.sphinx-doc.org/en/master/usage/advanced/intl.html
