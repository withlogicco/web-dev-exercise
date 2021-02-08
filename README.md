# Junior Web Developer Exercise

This is the exercise for the Junior Web Developer position at LOGIC.

## Scope

We need you to create a web application in the programming language of your choice. The web application should have the following pages and API endpoints:

### `/` - home

* The home page of the web application should present the user with a form that will contain a multi-line text field and a button.
* When the button is pressed, each line of the text field should be sent over for sorting to the `/api/sort` endpoint (defined below) and when the results are back, the sorted input should be displayed in a separate `<div>` element.
* After pressing the button, it should be disabled and a loading text should be displayed until the results are back.
* When the results are back, the button should be enabled again.

### `/api/sort` - the sorting API endpoint

* This endpoint should receive and array of strings, sort them and return them back
* The sorting algorithm should be [Quicksort](https://en.wikipedia.org/wiki/Quicksort) (do not use any libraries or built-in functions for sorting)
* The API endpoint should validate that the correct data (array of strings) has been submitted, otherwise return a 400 status code

### Example

If the user enters the text below:

```
banana
apple
orange
```

The following JSON request should be made:

```
POST /api/sort

[
    "banana",
    "apple",
    "orange"
]
```

The following JSON response should be returned:

```
[
    "apple",
    "banana",
    "orange"
]
```

And the following text should be displayed when the request completes:

```
apple
banana
orange
```

## Submission process

Please follow the steps below, in order to submit the exercise

* [Clone the repository locally](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)
* [Create a new repository at Github](https://docs.github.com/en/github/getting-started-with-github/create-a-repo) (either private, or public)
* [If you created a private repository, add @akalipetis and @parisk as collaborators](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository)
* [Change the local repository `origin` remote URL to your own repository](https://docs.github.com/en/github/using-git/changing-a-remotes-url)
* [Create a new branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
* Implement the exercise in your new branch
* [Create a pull request with your changes](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) and send it over to us
