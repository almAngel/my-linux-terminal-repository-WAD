#**Chapter 3 Exercises:**

1. *Show all the* **jpg** *pictures in the current directory.*

``ls *.jpg``

2. *Display all the files in the directory* `/usr/bin` *starting with letter* **j**.

``ls /usr/bin/j*``

3. *Show all the files in the directory* `/usr/bin` *starting with the letter* **k**, *with an* **a**
*in the 3 rd place.*

``ls /usr/bin/k?a*``

4. *Show all the files in the directory* ``/bin`` *ending with* **n**.

``ls /bin/*n``

5. *Display all the files in the directory* ``/etc`` *and all the files in every subdirectory
recursively*.

``ls -R /etc/``

6. *In your home directory, create another directory named test*. *Copy the file* **gzip** *from
the directory* ``/bin`` *to test*. *Create a duplicate of* **gzip** *named* **gzip2** *inside test*.

``mkdir test``

``cp /bin/gzip test/``

``cp test/gzip test/gzip2``

7. *Change the name of the directory* **test** *to* **test2**. *Create* **test3** *at the same level in
the directory tree as* **test2** *and move all the files from* **test2** *to* **test3**. *Delete* **test2**.

``mv test test2``

``mkdir test3``

``cp test2/* test3/``

``rm -R test2``

8. *Create an empty file named* **“*?Hello all?*”**. *Can you? Is it a good idea to name a file
this way? Explain your answer*.

``touch *?Hello all?*`` 

You can create it, but doing ``touch *?Hello all?*`` you are creating two different files,
named: ``*?Hello`` and ``all?*``, if you want to create a file with this exact name you need to
put one valid character instead of a blank space between the two words. Also, ``*`` and ``?``
characters are wildcards. Conclusion: Wildcards do not work when creating files.

9. *Create a directory named* ``multimedia_test`` *and copy all the content from the
directory* ``multimedia`` *into it*. *Then, create two files in* ``multimedia/video/``*, one
named* **films.txt** *and another named* **actors.txt**. *Edit the file* **films.txt** *and write
the title of your favourite movie*. *Then, create another file in* ``multimedia_test/video/``*,
also named* **films.txt**. *Edit this file and now write the titles of your five favourite movies.
Copy of all the content of* ``multimedia`` *into* ``multimedia_test`` *ensuring that
only most recently modified versions of files remain*.*To check that
everything is ok, check if* ``multimedia_test/video`` *contains the empty file*
**actors.txt** *and the file* **films.txt** *contains 5 titles and not 1.*

``mkdir multimedia``

``mkdir multimedia/video/``

``mkdir multimedia_test``

``cp -R multimedia/* multimedia_test/``

``touch multimedia/video/films.txt``

``touch multimedia/video/actors.txt``

``mcedit multimedia/video/films.txt``

``touch multimedia_test/video/films.txt``

``mcedit multimedia_test/video/films.txt``

``cp -R -u multimedia/* multimedia_test/``

10. *Delete the directory* ``multimedia/pictures/others``. *The system must ask for
confirmation.*

``rm -R -I multimedia/pictures/others``

11. *Move the file* **films.txt**, *which is in* ``multimedia/video``, *to the directory above,
at the same time renaming the file to* **my_films.txt**.

``mv -t multimedia/video/films.txt multimedia/my_films.txt``
