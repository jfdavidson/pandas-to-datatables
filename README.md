# pandas-to-datatables
Pandas dataframe to jQuery DataTables

I had some trouble searching for the correct format to export a pandas dataframe to jQuery DataTables.

python code:

```
table = df.to_json(orient='split', index=False)
return table
```

DataTables js

```
$(document).ready(function() {
                    $('#example').DataTable( {
                        'ajax':{url: 'link/to/above', dataSrc: 'data'}
                    } );
                } );
```

Hopefully this helps someone. 