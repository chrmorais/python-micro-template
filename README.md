python-micro-template
=====================

Take python itself as template language

Borrowed from jquery micro template(http://code.google.com/p/jquery-micro-template/)

# Usage example(kivy): #

    import python_micro_template
    ...
    kvml=open('example_kivy_scrollview.kvml', 'r').read()
    kvml=python_micro_template.tpl.parse(kvml)
    grid=Builder.load_string(kvml)
    ...

# Template example(kvml): #

    <:for i in range(30):#{#:>
    Button:
        text: '<:=i:><:for j in range(6):#{#:><:=j:><:#}#:>'
        size: 480, 40
        size_hint: None, None
    <:#}#:>
