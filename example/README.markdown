run the following command in your shell:

    $ coffee ../simple-coffee-dependencies.coffee -F first_file.coffee > output.coffee

you should get a file named **output.coffee** which must contain following:

    alert "i am file 2"
    
    alert "i am file 3"

    # nothing to require

    alert "i am file 4"

    alert "i am file 1"

