# obligatoriskOpgave1
## Øvelse 1: 
https://api.dropboxapi.com/2/files/list_folder

status 200 OK

der er forbindelse til dropbox app!

## Øvelse 2:
https://api.dropboxapi.com/2/files/create_folder_v2

HTTP verb: post

skabt en ny mappe kaldt testmappe:

{
    "path": "/TestMappe"
}
   

## Øvelse 3:
https://api.dropboxapi.com/2/files/get_metadata

HTTP verb: post

Status 200 OK

{
    "path": "/TestMappe"
}
 "metadata": {
        "name": "TestMappe",
        "path_lower": "/testmappe",
        "path_display": "/TestMappe",
        "id": "id:pyVxVY3w32oAAAAAAAAABg"
    }
}

## Øvelse 4: 
https://content.dropboxapi.com/2/files/upload

http verb: post

ændret content type: application/octet-stream

tilføjet Dropbox-API-Arg key

body:
{    "autorename": false,    "mode": "add",    "mute": false,    "path": "/TestMappe/testfil.txt",    "strict_conflict": false}

resultat:
{
    "name": "testfil.txt",
    "path_lower": "/testmappe/testfil.txt",
    "path_display": "/TestMappe/testfil.txt",
    "id": "id:pyVxVY3w32oAAAAAAAAABw",
    "client_modified": "2023-09-06T08:29:58Z",
    "server_modified": "2023-09-06T08:29:59Z",
    "rev": "01604ac8c8afe03000000010d02b111",
    "size": 136,
    "is_downloadable": true,
    "content_hash": "c70adb602e69b47d9a343034bfcfcc23221272a2898257f66fe5f6e9da0133fa"
}

## Øvelse 5: 
https://api.dropboxapi.com/2/files/delete_v2

Http verb: post

body:

{
    "path": "/TestMappe/testfil.txt"
}

resultat:
{
    "metadata": {
        ".tag": "file",
        "name": "testfil.txt",
        "path_lower": "/testmappe/testfil.txt",
        "path_display": "/TestMappe/testfil.txt",
        "id": "id:pyVxVY3w32oAAAAAAAAABw",
        "client_modified": "2023-09-06T08:29:58Z",
        "server_modified": "2023-09-06T08:29:59Z",
        "rev": "01604ac8c8afe03000000010d02b111",
        "size": 136,
        "is_downloadable": true,
        "content_hash": "c70adb602e69b47d9a343034bfcfcc23221272a2898257f66fe5f6e9da0133fa"
    }
}

## Øvelse 7:
https://api.dropboxapi.com/2/files/search_v2

http verb: post

body:
{
    "match_field_options": {
        "include_highlights": false
    },
    "options": {
        "file_status": "active",
        "filename_only": false,
        "max_results": 20,
        "path": "/TestMappe"
    },
    "query": "testfil"
}

Resultat: 
{
    "has_more": false,
    "matches": []
}

## Øvelse 8:
https://api.dropboxapi.com/2/files/move_v2

http verb: post

body:
{
    "allow_ownership_transfer": false,
    "allow_shared_folder": false,
    "autorename": false,
    "from_path": "/TestMappe/testfil.txt",
    "to_path": "/TestMappe2/testfil.txt"
}

Resultat:
{
    "metadata": {
        ".tag": "file",
        "name": "testfil.txt",
        "path_lower": "/testmappe2/testfil.txt",
        "path_display": "/TestMappe2/testfil.txt",
        "id": "id:pyVxVY3w32oAAAAAAAAACA",
        "client_modified": "2023-09-06T08:57:32Z",
        "server_modified": "2023-09-06T09:03:10Z",
        "rev": "01604ad03406177000000010d02b111",
        "size": 128,
        "is_downloadable": true,
        "content_hash": "9b7848a6e25ce0a547677824ceb0fcc8a2afcf669c6dc315ceedd8eb33b43efc"
    }
}

## Øvelse 9:
https://api.dropboxapi.com/2/files/copy_v2

http verb: post

Body:
{
    "allow_ownership_transfer": false,
    "allow_shared_folder": false,
    "autorename": false,
      "from_path": "/TestMappe2/testfil.txt",
    "to_path": "/TestMappe/testfil.txt"
}

Resultat:
{
    "metadata": {
        ".tag": "file",
        "name": "testfil.txt",
        "path_lower": "/testmappe/testfil.txt",
        "path_display": "/TestMappe/testfil.txt",
        "id": "id:pyVxVY3w32oAAAAAAAAACg",
        "client_modified": "2023-09-06T08:57:32Z",
        "server_modified": "2023-09-06T09:14:44Z",
        "rev": "01604ad2c9966d5000000010d02b111",
        "size": 128,
        "is_downloadable": true,
        "content_hash": "9b7848a6e25ce0a547677824ceb0fcc8a2afcf669c6dc315ceedd8eb33b43efc"
    }
}
