---
title: API Reference

language_tabs:
  - Ruby

search: true
---

# Introduction

Welcome to the PollHub API! You can use our API to access PollHub API endpoints, which can get information on various Polls, their Votes, and Comments in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](http://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Poll

## Get Specific Poll Details

> Use this code:

```ruby
code here
```

> JSON response:

```json
{
    "poll": {
        "id": 5,
        "title": "Let's create a poll for testing",
        "slug": "let-s-create-a-poll-for-testing",
        "description": "Poll for testing",
        "createdAt": "2014-06-04T11:49:44.786Z",
        "views": 0,
        "totalVotes": 0,
        "totalFollowers": 0,
        "author": {
            "id": 12,
            "username": "jaleel_lowe",
            "image": null
        },
        "tags": [
            "tag 1",
            "tag 2"
        ],
        "options": [
            {
                "id": "9",
                "value": "Option 1",
                "voted": false,
                "totalVotes": 0
            },
            {
                "id": "10",
                "value": "Option 2",
                "voted": false,
                "totalVotes": 0
            }
        ]
    }
}
```

This accepts a `poll_id` as parameter and return poll details with options

### URL:

[GET]  /1/polls/:id

### Params:

id: &lt;String&gt; required



## Create Poll

> Use this code:

```ruby
code here
```

> JSON response:

```json
{
    "poll": {
        "id": 5,
        "title": "Let's create a poll for testing",
        "slug": "let-s-create-a-poll-for-testing",
        "description": "Poll for testing",
        "createdAt": "2014-06-04T11:49:44.786Z",
        "views": 0,
        "totalVotes": 0,
        "totalFollowers": 0,
        "author": {
            "id": 12,
            "username": "jaleel_lowe",
            "image": null
        },
        "tags": [
            "tag 1",
            "tag 2"
        ],
        "options": [
            {
                "id": "9",
                "value": "Option 1",
                "voted": false,
                "totalVotes": 0
            },
            {
                "id": "10",
                "value": "Option 2",
                "voted": false,
                "totalVotes": 0
            }
        ]
    }
}
```

### URL:

[POST]  /1/polls

### Params:

title: &lt;String&gt; required,

description: &lt;String&gt; optional,

tags: &lt;String&gt; optional # common separated values in string as tags.

options: [&lt;String&gt; required, &lt;String&gt; required] required,

#Comments

## Get specific comment details

> Use this code:

```ruby
code here
```

> JSON response:

```json
{
  "comment":
  {
    "id":1,
    "text":"Smart.. :)",
    "createdAt":"2014-06-17T11:58:33.701Z",
    "createdAtInWords":"11 days ago",
    "author":
    {
      "id":2,
      "username":"AfreenMunshi",
      "image":"AfreenMunshi.jpeg"
    }
  }
}
```

This accepts a `poll_id` and a `comment_id` as parameter and return comment details

### URL:

[GET]  /1/polls/:poll_id/comments/:id

### Params:

poll_id: &lt;String&gt; required

id: &lt;String&gt; required

## Create a comment

> Use this code:

```ruby
code here
```

> JSON response:

```json
{
    "comments":[{
        "id":17,
        "text":"how are you",
        "createdAt":"2014-07-04T00:49:19.161Z",
        "createdAtInWords":"1 minute ago",
        "author":{
            "id":7,
            "username":"Munshi.Afreen",
            "image":"Munshi.Afreen.jpeg"
        }
    }]
}
```


### URL:

[POST]  /1/polls/:poll_id/comments

### Params:

text: &lt;String&gt; required

poll_id: &lt;String&gt; required

