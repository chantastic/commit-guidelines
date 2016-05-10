# Commit Guidelines
Mostly reasonable guidelines for commit messages.

## Commit Message Format
Commit messages consist of a [message](#message), [description](#description)
and [related](#related).

```
<message>

<description>

<related>
```

A [message](#message) consists of a [type](#type), [scope](#scope), and
[subject](#subject).

No line should be longer than 80 characters long, for optimal github viewing.

## Message
```
<type>(<scope>): <subject>
```

Examples: `refactor(plans#show): remove 1 of 4 templating languages`

### Type
* `feat`: New feature
* `fix`: Bug fix
* `format`: Change not affecting the **meaning** of code (white-space, formatting, etc)
* `docs`: Documentation-**only** change
* `style`: Stylesheet-**only** change
* `refactor`: Change that neither fixes a bug or adds a feature
* `perf`: Change that improves performance
* `test`: Addition of a missing test
* `chore`: Changes to the build process or auxiliary tools and libraries

### Scope
The scope could be anything specifying the site of the commit change. For
example `plans#show`, `PlanPerson`, `LiveChatMessageList`, `.tab-list`, etc...

### Subject
The subject contains a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't use capitalize first letters
* don't use trailing punctuation (.)

### Description
Just as in the [subject](#subject), use the imperative, present tense: "change"
not "changed" nor "changes" The body should include the motivation for the
change.

### Related
The footer should contain any information about **Breaking Changes** and is the
place to reference Trello cards, or GitHub issues that the commit **Closes**.

### Attribution
This guide is ~~pirated from~~ inspired by Angular's excellent
[CONTRIBUTING.md](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#-git-commit-guidelines).

A detailed explanation can be found in this [document][commit-message-format].

[commit-message-format]: https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#

## `fixup` commits

You're stuff's on staging but you're making small, progressive tweeks. `fixup` is your friend.

Fixup commits are associated with commit you've already made. They allow you to make commits without inserting additional messages. They can also be automatically squashed, for those civilized developers.

Here's how it works. `commit` takes `--fixup` as on option. When used, you'll have to provide the SHA of the commit your is fixing up. Like so:

```bash
git commit --fixup a9b8c7

# aliases also work but get confusing after your first fix

git commit --fixup head
```

You probably don't memorize your recent commit SHAs. You can use the syntax below as a backword search. This fixup commit will attach to the most recent commit, where "style" is in the message:

```bash
git commit --fixup :/style
```
