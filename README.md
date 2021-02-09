# Junior Web Developer Exercise

This is the exercise for the Junior Web Developer position at LOGIC. The objective of this exercise is to create a web application.

## Spec

This is full functionality of the web application we expect you to create.

### Home Page

* This is what appears, when the user first opens the web application
* This page contains a form including a text area and a submit button, and an empty div element.
* When the form is submitted, each line of the text area should be submitted to the `/api/sort` endpoint (defined below) and when the results are back, the sorted input should be displayed the div element, described above.
* When the form is submitted, the button should be disabled and a loading text should be displayed until the results are back.
* When the results are back, the button should be enabled again, with the original text.

### Sorting API endpoint (`/api/sort`)

* This endpoint should receive and array of strings, sort them and return them back
* The sorting algorithm should be [Quicksort](https://en.wikipedia.org/wiki/Quicksort) (do not use any libraries or built-in functions for sorting)
* The API endpoint should validate that the correct data (array of strings) has been submitted, otherwise it should return a 400 status code

### Documentation

There should be brief (just a few words on each case), yet clear documentation of:

* How to run your application
* How each function you wrote works

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

1. [Clone the repository locally](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)
2. [Create a new repository at Github](https://docs.github.com/en/github/getting-started-with-github/create-a-repo) (either private, or public)
3. [If you created a private repository, add @akalipetis and @parisk as collaborators](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository)
4. [Change the local repository `origin` remote URL to your own repository](https://docs.github.com/en/github/using-git/changing-a-remotes-url)
5. [Create a new branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
6. Implement the exercise in your new branch
7. [Create a Pull Request with your changes](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) in your own repository (**NOT** in this repository) and send it over to us
