# Web Developer Exercise

This is the exercise for the Web Developer position at LOGIC. The objective of this exercise is to create a web application in the programming language of your choice.

## How to submit

1. Create a new **private** repository using this template[^1].
2. Add the following GitHub users as collaborators: @akalipetis, @parisk.
3. Create a new branch for your implementation[^2].
4. Implement the exercise in your new branch.
5. Create a Pull Request with your implementation[^3] and add @parisk as a reviewer[^4].

## Effort

You should spend **no more than 4 hours** working on this exercise. We will by no means police you, but we do trust you to respect and comply with this constraint.

## Deadline

You should submit your Pull Request no later than **7 calendar days** after you receive the email from us inviting you to participate in it.

## Requirements

Your submission should:

- [ ] Implement the spec
- [ ] Document the implementation

## Stretch goals

In case you finish your implementation early, you can:

- [ ] Dockerize your repository
- [ ] Implement at least one automated test (e.g. unit test)

## Spec

This is the functionality of the web application we expect you to create. It should include an HTML page and an API endpoint.

### Home page (`/`)

- This is the page the user sees, when they open the web application
- This page contains a form with:
  - A text area
  - A submit button
  - An empty div element for results
- When the form is submitted:
  - The submit button should be disabled and it's text should be set to `Loading...`.
  - The value text area should be submitted to the `/api/sort/` endpoint as a JSON list (each line in the text area corresponds to a JSON list element).
- When the API endpoint responds:
  - The button should be enabled again, with the original text.
  - The sorted results should be displayed the div element for the results.

### Sorting API endpoint (`/api/sort/`)

- This endpoint should receive and array of strings, sort them and return them back
- The sorting algorithm should be Quicksort[^5] (do not use any libraries or built-in functions for sorting)
- The API endpoint should validate that the correct data (array of strings) has been submitted, otherwise it should return a 400 status code

## Documentation

Your submission should be brief, yet clearly documented. In particular:

- **README**: The current README file should be replaced with one containing information only about what this web application does and how to run it.
- **Code**: Each function you write should be documented about what it does and how it works.

## Example

If the user enters the text below:

```
banana
apple
orange
```

The following JSON request should be made:

```
POST /api/sort/

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

## License

All code included here is [MIT licensed](./LICENSE).

[^1]: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template
[^2]: https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
[^3]: https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request
[^4]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review
[^5]: https://en.wikipedia.org/wiki/Quicksort