# Contributing

Thank you for helping! This guide explains how to add a new learning resource. You don't need to be a developer to follow it.

## Before you start

A resource can be added if it:

- is a single HTML file that opens in a browser, with no install step and no account
- has been tried from start to finish by you, with its answers checked
- contains no real personal data, such as children's names, photos, or contact details
- does not track users or send their data anywhere
- is your own work, and you are happy to share it under [CC BY 4.0](LICENSE)

## Where your resource goes

Resources are stored by age level, then by subject:

```
Ages-8-9/
└── Math/
    └── Problem-Detectives.html
```

Use the same pattern for your file: `Ages-X-Y/Subject/Resource-Name.html`

| Part | Rule | Examples |
| --- | --- | --- |
| Age level | `Ages-` followed by the age range | `Ages-8-9`, `Ages-10-11` |
| Subject | Starts with a capital letter, with hyphens instead of spaces | `Math`, `Science`, `Foreign-Languages` |
| File name | Each word starts with a capital letter, with hyphens instead of spaces, ending in `.html` | `Times-Tables.html` |

Use an existing age level or subject folder if one fits. If none does, create a new one using the same rules.

## Add your resource

Always work in a new branch, never directly on `main`. Name the branch after what you are adding: `add/age-subject-resource`, for example `add/8-9-math-fractions-game`.

### In your browser

1. Open the [repository](https://github.com/Julia-IO/ai-built-learning-resources) and select **Fork** to make your own copy.
2. In your copy, open the branch menu (it says `main`), type your branch name, and select **Create branch**.
3. Add your file:
   - **If the folder already exists:** open it, then select **Add file** > **Upload files**.
   - **If you need a new folder:** on your computer, create the folders with your file inside, for example `Ages-10-11/Science/Water-Cycle.html`. In the top level of your copy, select **Add file** > **Upload files**, then drag in the `Ages-10-11` folder.
4. Commit the upload to your new branch.
5. Open `README.md`, select the pencil icon, and [update the resource table](#update-the-readme). Commit to the same branch.
6. Select **Contribute** > **Open pull request**.

### From the command line

Fork the repository first, then run these commands, replacing `YOUR-USERNAME` and the example names:

```bash
git clone https://github.com/YOUR-USERNAME/ai-built-learning-resources.git
cd ai-built-learning-resources
git switch -c add/8-9-math-fractions-game
mkdir -p Ages-8-9/Math
cp /path/to/your/Fractions-Game.html Ages-8-9/Math/
# Update README.md (see the next section)
git add Ages-8-9/Math/Fractions-Game.html README.md
git commit -m "Add Fractions Game for ages 8-9"
git push -u origin add/8-9-math-fractions-game
```

Then open the link that Git prints to create your pull request.

## Update the README

Add one row for your resource under the right age level and subject in `README.md`:

```markdown
| Fractions Game | Comparing fractions | How it works, in one or two sentences. | [Open it](https://julia-io.github.io/ai-built-learning-resources/Ages-8-9/Math/Fractions-Game.html) |
```

The link will start working once your pull request is merged.

If the age level or subject is new, add a heading and a table in the same format as the existing ones. Keep age levels in order, from youngest to oldest.

## Open your pull request

Target the `main` branch, and include:

- the age group and subject
- what children practise, and how the resource works
- which AI tools you used to build it
- how you tested it

We will review it and try the resource out. We may suggest changes before merging.

## Other ways to help

To report a mistake or suggest an idea without adding a resource, please [open an issue](https://github.com/Julia-IO/ai-built-learning-resources/issues).
