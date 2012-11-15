## What happened to the code?
[Amazon Web Services](http://aws.amazon.com/) is moving code hosted at GitHub to a new
GitHub organization: <http://github.com/aws>. Nothing is lost. Only moved.

## What do I do now?
Simply update the URL of the repository's origin:

	First, back up two commits:
	$ git reset --hard HEAD^^

	Next, change then URL of origin:
	$ git remote set-url origin git@github.com:aws/aws-sdk-ruby.git

	Verify it worked
	$ git remote -v
	
	Pull the latest changes
	$ git pull

	Lastly, move your local repository to the new name (without the "for")
	$ mv aws-sdk-for-ruby aws-sdk-ruby
