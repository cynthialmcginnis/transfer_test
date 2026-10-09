# The Transfer Test

A browser exercise about what happens when a prediction model is moved from the site where it was built to a new one.

Built by Cynthia McGinnis.

## What it does

1. You pick a setting: a clinic, a maintenance shop, or an education office.
2. You test a vendor's model at Site A, where it was trained. It scores well.
3. You move the same model to Site B. The score drops.
4. You look inside the model and find the shortcut: an input that predicted the outcome at Site A for a reason unrelated to the task.
5. You try fixes within a budget of 6 effort points: leave out an input, add local records, send close calls to a person, or move the cutoff.
6. You decide: adopt, adapt, or stop. The page builds a summary you can copy.

## How to use it

Open `index.html` in a browser. There is nothing to install and nothing is sent anywhere. To host it, turn on GitHub Pages for this repository and share the link.

## How it works

The page generates its own records from your last name and the setting, so two people get different data. It trains a small logistic regression model in the browser. The sorting score is the area under the ROC curve. All records are simulated.

## What it simplifies

The exercise assumes that acting on a flag prevents the outcome and that a human reviewer always gets a close call right. Real deployments are messier.
