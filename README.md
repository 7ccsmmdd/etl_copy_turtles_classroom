## An ETL Copy Transformation

Create a copy transformation for your `TurtleProgram` language. Before starting, carefully check out the Xtext grammar in this repository to make sure you are using the correct names for meta-classes and features.

You will want to write your ETL transformation in the runtime Eclipse to be able to quickly test it out yourself on an arbitrary example model. When you are done, save your ETL copy transformation in the file called `copy_turtles.etl` in the `generator` source folder in the main `turtles` project so that the auto-grading can pick it up.

Eventually, the autograding should pass and assign 10/10.

### Using the repository

There are two ways to do this activity:

1. You can check out the repository and import the projects into Eclipse, then do the activity there. Commit your changes and push them back to GitHub to trigger the autograding so you can see whether you've correctly implemented the grammar. More information about checking out and editing code in Eclipse can be found on KEATS.
2. You can do this activity in your browser.

   Due to an annoying, long-standing GitHub Classroom bug, you need a small extra step for this:

    1. Copy the URL of your repository (see the location bar of your browser).
    2. Open [this form](https://7ccsmmdd.github.io/) and paste your repository URL into the corresponding field.
    3. The URL field should fill with a long complicated URL as soon as you move out of the text field. 
    4. Click on the button at the bottom of the form to open that URL in a new tab: this is the MDENet Education Platform with the activity pre-loaded. Generate the Xtext editor, then you can open a playground view where you can create a model and an ETL transformation and try out what happens when you run the transformation. See the video on KEATS to find out how to do this. **Note that you must save your changes before switching to the generated editor or you will lose them.** Saving your changes will create a commit in your repository, which will also automatically trigger the autograding process -- the transformation is automatically put in the correct place for the autograder to pick it up, no need to copy it across in this case.

Note that the [`copy_turtles.etl`](uk.ac.kcl.inf.mdd6a.turtles/src/uk/ac/kcl/inf/mdd6a/generator/copy_turtles.etl) file has been pre-seeded with some helper operations for copying enumeration values (values for pen up/down, movement forward/backward, and turning left/right). These are needed to account for a slight difference in how the transformation is run within Eclipse and within the MDENet Education Platform. The transformation will work without these operations in Eclipse, but it will fail without them in the education platform. Using the operations in Eclipse will work, so we recommend you use the operation in any case. We haven't introduced operations in class, but you can find an example of using a similar operation (for copying colour enumeration values) [here](https://eclipse.dev/epsilon/playground/?cb9a688d). Note how in that example, the operation defined is used as if it was a member of the enumeration class: `s.color.toTargetColor()`. You can use the operations we provide here in the same way in your ETL rules.