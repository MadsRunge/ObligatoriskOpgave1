# obligatoriskOpgave1
Øvelse 1: der er forbindelse til dropbox app

Øvelse 2:
https://api.dropboxapi.com/2/files/create_folder_v2
skabt en ny mappe kaldt testmappe:
HTTP verb: post
{
    "path": "/TestMappe"
}
   

Øvelse 3:
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

Øvelse 4: 
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
Øvelse 5: 
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
