# StackExchange duplicates
This is small util that parses dump from one of StackExchange websites and
finds questions with biggest amout of duplicates.

It can be useful in analytics: such questions define most interesting top_duplicated_posts
in community.

![Result image](http://i.imgur.com/fe3niPT.png)

## Install
Unfortunately, program don't support Python 2. It's tested only in Python 3.

```bash
git clone https://github.com/sevazhidkov/stackexchange-duplicates.git
cd stackexchange-duplicates
pip install -r requirements.txt # could be "pip3 install -r requirements.txt"
```

## Run
You need to run 'start.py' with special parameters.

Example:
```bash
python3 start.py --posts /Users/vsevolosij/Downloads/dba.stackexchange.com/Posts.xml --postsLinks /Users/vsevolosij/Downloads/dba.stackexchange.com/PostLinks.xml  --postsNum 50
```
It exports most duplicated posts to HTML file in current directory and limits
number of posts to 50. You can see all parameters below.

## Parameters

| Parameter name      | Description                                         | Example                                                                      | Default               |
|---------------------|-----------------------------------------------------|------------------------------------------------------------------------------|-----------------------|
| posts               | Path to Posts.xml file from StackExchange dump      | --posts /Users/vsevolosij/Downloads/dba.stackexchange.com/Posts.xml          | ./Posts.xml           |
| postsLinks          | Path to PostsLinks.xml file from StackExchange dump | --postsLinks /Users/vsevolosij/Downloads/dba.stackexchange.com/PostLinks.xml | ./PostsLinks.xml      |
| postsNum            | Num of posts in result                              | --postsNum 50                                                                | 100                   |
| exportFile          | Path to export file                                 | --exportFile /var/www/index.html                                             | ./result.html         |
| exportType          | Type of export file. Could be 'json', 'html'        | --exportType json                                                            | html                  |
| stackexchangeDomain | Domain of StackExchange site                        | --stackexchangeDomain math.stackexchange.com                                 | dba.stackexchange.com |
