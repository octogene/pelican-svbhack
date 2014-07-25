To translate the theme you will need to use pybabel.

1. Extract the strings:

.. code-block:: bash

	pybabel -v extract --mapping babel.cfg --output messages.pot ./

2. Initialize your language file:

	For this example we're creating a french translation. Change the locale code after the  '--locale' option depending on your target language.

.. code-block:: bash

	pybabel init --input-file messages.pot --output-dir translations/ --locale fr --domain messages

3. Translate it with any text editor by replacing empty string msgtr with your translation.

4. Compile it:

.. code-block:: bash
	
	pybabel compile --directory translations/ --domain messages

5. If you update the theme and add new strings, redo step 1 and update your language file and next :

.. code-block:: bash

	pybabel update --input-file messages.pot --output-dir translations/ --domain messages
