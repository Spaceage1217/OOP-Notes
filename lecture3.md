# lecture 3
## How to write to a file?
  - You can use the print writer `import java.io.FileWriter;`
    `FileWriter fw = new FileWriter("exampleFileout.txt, true");`
      > The true means we want it to append. If no file is there it will create
        the file.

    `PrintWriter outfile = newPrintWrite(fw)`
    `outFIle.println("...");`
    `outFile.close();`

## How to read from a file?
 `File reader fr = new FileReader("myfile.txt");`
 `Scanner inFile = new Scanner(fr)`;
 `String line = inFile.nextLine();`
 `String[] words = line.split(" ");`
  > This will split the words in the string so you can grab words by index
    words[0] will print out the first word in the string and words[1] the second
    and so on.

## How to format a string?
  - `string.format()` can be used to format strings
     check format slides for more info on how this is done.

## What is Serilization?
  - To serialize an object means to convert its state to a byte stream so that
    the byte can be reverted back into a copy of the object.
    `java.io.serializable` needs to be imported.
    All the fields in the object class must be serializable in order to write it
    to a sterilized file.
    `FileInputStream fis = new FileInputStream(myFile.ser);`
    `FileOutputStream ous = new FileOutputStream(fis);`

## Common Errors?
 -  Make sure you specify the class you want to use.
    Common names like `MAX_VALUE` are properties of man sub classes
    If you don't specify the class it belongs to java will throw an exception
    saying that `MAX_VALUE` is ambiguous.

 -  Spelling errors.
 -  uninitialized references like `String name;` that are not primitive
    data types will throw an exception when referenced because they unlike primitive
    data types are not assigned a default value
## Exceptions
  - *CHECKED exception* is a type of exception that must be either
    caught or declared in the method in which it is thrown.
  - *UNCHECKED exception* exceptions under Error and RuntimeException classes.
