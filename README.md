# go-chord
[Chord distributed system](http://pdos.csail.mit.edu/papers/chord:sigcomm01/chord_sigcomm.pdf) in GO

**Note: that this was built using Windows. I do not know how it works on Linux**  
I would be happy if someone told me :)

**To run:**

1. Compile
2. Open a cmd window and run the app
3. The default port is :3410
4. Type "join" 
 - Join starts a new ring unless a port number is provided
5. Open another cmd
6. Tell it to use another port by typing "port :3411" any number preceded by a colon should work
7. Type "join :3411" or the port number of any active node
8. Repeat 5 - 7 until you have 5 or so windows
9. Start typing commands. It accepts "get [key]", "put [key] [value]", and "delete [key]"

**Alternatively:** 

1. Launch the app using "chord.exe -a=[:portnumber]" **The colon is required!**
2. Type "join [:activePortNumber]"
3. Repeat 1 and 2 a few times with different ports
4. Run commands

You can also just click the batch file I include.

Note that putting any kind of space will split the input. 

> put 1234 "hello world!" 

will create 

| Key           | Value         |
| ------------- |:-------------:|
| 1234          | "hello        |

I built the distributed system, but I had to move on before adding propper string interpretation. 
