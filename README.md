# sphinx-internationalization-test

1. `pip install Sphinx sphinx-intl python-levenshtein furo`

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

4. Set theme to furo

    ```
    # html_theme = 'alabaster'`
    html_theme = 'furo'
    ```

5. Copy furo's `page.html` to `docs/_templates`

    ```
    wget -P docs/_templates https://raw.githubusercontent.com/pradyunsg/furo/main/src/furo/theme/furo/page.html
    ```

6. Run VSC tasks to generate files for translation.

    > **NOTE**
    > 1. Default language is set to `pl` - Polish.
    > 2. You need to configure first `virtualenvPath` in `.vscode/settings.json` to run VCS tasks.

    - Internationalization - build gettext
    - Internationalization - intl update

7. Translate generated `*.po` files.
8. Run VSC task to see translated page.
    - Internationalization - build html
9. Push to repository.
10. Configure project in RTD.

    https://docs.readthedocs.io/en/stable/localization.html

11. Now you have option to change language for your documentation.

    Direct links below:

    - https://sphinx-internationalization-test.readthedocs.io
    - https://sphinx-internationalization-test.readthedocs.io/pl/latest/


## More resources

- https://www.sphinx-doc.org/en/master/usage/advanced/intl.html

