![github.png](http://upload-images.jianshu.io/upload_images/2040047-113772827550d86c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### [中文版](http://www.jianshu.com/p/489ca49e9a99)

This project is a GitHub trending API power by Python Tornado.
It was deployed on Heroku.
***

### All the requests main adrress is this:https://trendings.herokuapp.com。
#### Get the trending repository
+ request address like this:
> /api/repo/<lang>/?since=weekly    GET
+ lang:optional，the language of the trending repository.
+ since,optional，get method parameter，default is daily,ohters is weekly,monthly.
for example request this address:
https://trendings.herokuapp.com/api/repo/java/?since=weekly

 return:
```
{
  //trending repositories,only 25 items
  "items": [
    {
      //the avatar link of contributors
      "avatars": [
        "https://avatars0.githubusercontent.com/u/16903644?v=3&s=40",
        "https://avatars2.githubusercontent.com/u/8622362?v=3&s=40",
        "https://avatars0.githubusercontent.com/u/10773353?v=3&s=40",
        "https://avatars3.githubusercontent.com/u/6392550?v=3&s=40",
        "https://avatars1.githubusercontent.com/u/3837836?v=3&s=40"
      ],
      //repository link
      "repo_link": "https://github.com/kdn251/interviews",
      //repository desctiption
      "desc": "Everything you need to know to get the job.",
      //repository name
      "repo": "/kdn251/interviews",
      //the repository starts count by far
      "starts": "5,772",
       //the repository forks count by far
      "forks": "539",
      //the language of repository
      "lang": "Java",
      //the repository stars count for tody or this week or this month
      "added_starts": "4,591 stars this week"
    },
    .
    .
    .
  ]
}
```

#### Get the trending developers
+ request address like this:
> /api/dev/<lang>/?since=weekly GET

+ lang:optional，maybe is the language of the trending developers using.
+ since,optional，get method parameter，default is daily,ohters is weekly,monthly.

for example request this address:
https://trendings.herokuapp.com/api/dev/java/?since=weekly

 return：
```
{
  //the trending developers,only 25 items
  "items": [
    {
     //the trending repository of this developer
      "target_link": "https://github.com/google/guava",
      //the username in GitHub of this developer
      "user": "google",
      //the main page in GitHub of this developer
      "user_link": "https://github.com/google",
        //the full name of this developer
      "full_name": "(Google)",
      //the trending repository description of this developer
      "target_desc": "Google Core Libraries for Java",
      //maybe is the trending repository of this developer
      "target": "guava"
    },
    .
    .
    .
]
}
```