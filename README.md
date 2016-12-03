# GUC API

REST API wrapper for the German University in Cairo (GUC) ~~private~~ API.

## Why?

* The GUC API is only exclusively used by the official GUC mobile application
* The GUC API is altogether poorly designed _(e.g. JSON embedded within XML responses)_

## API

### Authentication

All API calls require [basic authentication](https://en.wikipedia.org/wiki/Basic_access_authentication#Client_side).
Example: if your username is `john.doe` & your password is `12345`, then your HTTP `Authorization` header should look like this: `Basic Z3VjaWFuOjEyMzQ1`.

### API Calls

<<<<<<< HEAD
* `GET http://guc-api.herokuapp.com/api/login`

Response:
```
{
    "authorized": true
}
```
or
```
{
    "authorized": false
}
```

***

* `GET http://guc-api.herokuapp.com/api/coursework`

Response:
=======
#### Login 

`GET http://guc-api.herokuapp.com/api/login`

Response:
```
{
    "authorized": true
}
```
or
>>>>>>> 6b64e1c716e8fb8e1a2ffceac7ac9a52dbe004ee
```
{
    "authorized": false
}
```

***

<<<<<<< HEAD
* `GET http://guc-api.herokuapp.com/api/midterms`

Response:
```
[  
   {  
      "name": "MET Computer Science 7th Semester - Analysis and Design of Algorithms CSEN703",
      "percentage": "41.25"
   },
   ...
]
=======
#### Coursework 

`GET http://guc-api.herokuapp.com/api/coursework`

Response:
```
{  
   "error": null,
   "data": [  
      {  
         "code": "CSEN701",
         "name": "Embedded System Architecture",
         "grades": [  
            {  
               "module": "Assignment 1",
               "point": "9.75",
               "maxPoint": "10"
            },
            ...
         ]
      },
      ...
   ]
}
```

***

#### Midterms 

`GET http://guc-api.herokuapp.com/api/midterms`

Response:
```
{  
   "error": null,
   "data": [  
      {  
         "name": "MET Computer Science 7th Semester - Analysis and Design of Algorithms CSEN703",
         "percentage": "41.25"
      },
      ...
   ]
}
>>>>>>> 6b64e1c716e8fb8e1a2ffceac7ac9a52dbe004ee
```

***

<<<<<<< HEAD
* `GET http://guc-api.herokuapp.com/api/attendance`

Response:
```
[  
   {  
      "name": "Computer Graphics",
      "level": "1"
   },
   ...
]
=======
#### Attendance 

`GET http://guc-api.herokuapp.com/api/attendance`

Response:
```
{  
   "error": null,
   "data": [  
      {  
         "name": "Computer Graphics",
         "level": "1"
      },
      ...
   ]
}
>>>>>>> 6b64e1c716e8fb8e1a2ffceac7ac9a52dbe004ee
```

## Limitations

The GUC servers go down quite often. Transitively, our API cannot serve anything during that time.

## License

This project is licensed under the MIT License.
