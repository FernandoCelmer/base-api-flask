# Api mercado

## gerar executável da api:

Para gerar o executável sem subir o console, é necessário comentar as seguintes linhas nos arquivos do flask

arquivo:
> .env\Lib\site-packages\flask\cli.py

```` python
#    if app_import_path is not None:
#        click.echo(f" * Serving Flask app '{app_import_path}'")

#    if debug is not None:
#        click.echo(f" * Debug mode: {'on' if debug else 'off'}")
````

Para gerar o executável utilizar o seguinte comando

```` shell
pyinstaller --onefile --path .env/Lib/site-packages/ --noconsole api.py
````
