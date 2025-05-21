# Kayla Soraya Djakaria - 2306256381

### 1.2. Understanding how it works.
![Timer Diagram](/images/image.png)

From the picture above, the line 'hey hey' is printed before 'howdy' and 'done' because `spawner.spawn()` only schedules async block rather than driving it to completion, execution falls straight through to the next line in main(), which prints 'hey hey' immediately. After that, the executor begin polling the spawned task—first printing 'howdy!' and then, after the two-second timer, print 'done!'.