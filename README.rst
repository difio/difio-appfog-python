Difio registration agent for AppFog / Python applications.

It compiles a list of locally installed Python packages and sends it to
<http://www.dif.io>.


Installing on your AppFog application
----------------------------------------

Create an account at <http://www.dif.io>

Create a Python application on AppFog

Add a dependency in your requirements.txt file

::

    echo "difio-appfog-python" >> requirements.txt

Configure your Difio user ID

::

    af env-add <appname> DIFIO_USER_ID=YourUserID

Because AppFog doesn't support post deploy hooks you have NO WAY to enable the
registration script. :(

Then push your application to AppFog

::

    af update <appname>

That's it, you can now check your application statistics at
<http://www.dif.io>
