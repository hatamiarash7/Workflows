# Workflows

Some reusable workflows for Your projects. You can read more about them [here](https://docs.github.com/en/actions/using-workflows/reusing-workflows)

## How to use

Just call any workflow you want in your action :

```yaml
name: Your workflow

on:
  push:
    branches:
      - main

jobs:
  example-workflow:
    uses: hatamiarash7/Workflows/.github/workflows/example@main
```

## Note ❗

**Reusable workflows can’t be stacked on top of one another**. You can only have a reusable workflow call another reusable workflow, but you can’t have it reference more than one.

## Reusable workflows vs. composite actions

For the uninitiated, [composite actions](https://github.blog/changelog/2021-08-25-github-actions-reduce-duplication-with-action-composition/) enable you to combine multiple actions into a single action that you can then insert into any workflow. This means you can refactor long YAML workflow files into much smaller files—and you can also save yourself a fair amount of copying and pasting. Plus, if something like your credentials change, you won’t have to update an entire YAML file.

In practice, there are kinds of problems you can solve with either reusable workflows or a composite workflow. Both approaches have individual strengths and weaknesses. 80% of the time you can probably use either one. But 20% of the time, you’ll need to use one or the other.

For example, if your job needs to run on a specific runner or machine, you need to use reusable workflows. Composite actions don’t specify this type of thing. Composite actions are intended to be more isolated and generic.

## Key differences between reusable workflows and composite actions

| Reusable workflows                                 | Composite actions                                                |
| -------------------------------------------------- | ---------------------------------------------------------------- |
| Cannot call another reusable workflow              | Can be nested to have up to 10 composite actions in one workflow |
| Can use secrets                                    | Cannot use secrets                                               |
| Can use `if: conditionals`                         | Cannot use `if: conditionals`                                    |
| Can be stored as normal YAML files in your project | Requires individual folders for each composite action            |
| Can use multiple jobs                              | Cannot use multiple jobs                                         |
| Each step is logged in real-time                   | Logged as one step even if it contains multiple steps            |

With reusable workflows, you can have multiple jobs and that gives you a lot of more granular control—and power. They allow you to specify any number of things and customize them more to your liking.

Reusable workflows also don’t require individual folders for each workflow like composite actions do. This can make using reusable workflows simpler since you can avoid nesting a bunch of different folders like you’d need to do with composite actions.

---

## Support

[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/bc1qmmh6vt366yzjt3grjxjjqynrrxs3frun8gnxrz)](https://en.cryptobadges.io/donate/bc1qmmh6vt366yzjt3grjxjjqynrrxs3frun8gnxrz) [![Donate with Ethereum](https://en.cryptobadges.io/badge/micro/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)](https://en.cryptobadges.io/donate/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request 😃

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them.
