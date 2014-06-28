---
title: API Reference

language_tabs:
  - ruby

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the PollHub API! You can use our API to access PollHub API endpoints, which can get information on various Polls, their Votes, and Comments in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](http://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Poll

## Get Specific Poll Details

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

> The above command returns JSON structured like this:

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

[GET] /1/polls/:id

### Params:

id: (String) required

