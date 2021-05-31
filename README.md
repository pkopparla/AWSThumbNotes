# AWSThumbNotes
Further notes on the AWS thumbnail tutorial

This is the tutorial: https://docs.aws.amazon.com/lambda/latest/dg/with-s3-tutorial.html

<h2> Setting up the python environment </h2>

I followed the instruction for the python 3.8 version, but my system has python 3.9 already set up.
Used this guide to configure the correct version using pyenv: https://opensource.com/article/20/4/pyenv

In summary:
1. `$ brew install pyenv`
2. Include the pyenv path control in zsh file: `$ eval "$(pyenv init -)"` in ~/.zshrc
3. Add the following lines to ~/.zprofile and restart terminal


`export PYENV_ROOT="$HOME/.pyenv"`

`export PATH="$PYENV_ROOT/bin:$PATH"`

`eval "$(pyenv init --path)"`

4. This should set the correct python paths etc. Then set the default by using `pyenv global 3.8.x`

<h2> Making the zip archive </h2>

The other confusing part is creating the zip archive to set up the Lambda function. After running the build command
there is a hidden folder called `.aws-sam` which holds the build contents, dependencies etc. Go into the CreateThumbnail folder there,
select all files within and just click `compress` in the right-click menu. That creates the zip file, not sure if there's a better way.
