# convert-html-to-dash

This will help you convert some raw html into Python code for Dash and Plotly.

`python convert.py -h`
```
usage: convert.py [-h] [-i INFILE] [-o OUTFILE] [-p PRIORITY_LIST]

Convert HTML into Python Code for Dash with bootstrap


optional arguments:
  -h, --help        show this help message and exit
  -i INFILE         input file
  -o OUTFILE        output file
  -p PRIORITY_LIST  priority list for replacing tags.
                    Options: dcc = dash_core_components, dbc = dash_bootstrap_components, html = dash_html_components
                    Exanple: -p dbc -p html -p dcc
                    Default Order: dcc, dbc, html
                    Note: You can omit a modules too ie. -p html would only use html components
```

`python convert.py -i infile.html -o outfile.html`
```
  dbc.Container(
      className="container",
      children=[
          html.H1(children=["Some Test Information"]),
          dbc.Row(
              className="row",
              children=[
                dbc.Col(className="col", children=[]),
                ...
```

`python convert.py -i infile.html -o outfile.html -p html`
```
html.Div(
    className="container",
    children=[
        html.H1(children=["Some Test Information"]),
        html.Div(
            className="row",
            children=[
                html.Div(className="col", children=[]),
                ...
```


