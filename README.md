# AndroidActivityMap
![alt text](https://github.com/ammarptn/AndroidActivityMap/blob/master/image/Screenshot%202020-07-11%20at%2011.58.42%20PM.png?raw=true)

AndroidActivityMap is a executable jar file to help you generate the Activity/fragment map of your Android project
  - Increase navigation ability of your Android project
  - provide better vision of your application flow
  - Help you plan UI testing more efficacy
  - support kotlin/Java project
  - fast

# Features
  - Auto generate Activity/fragment map of your Android project
  - Activity/fragment shortcut

# Requirement
- Android studio
- IDEA Mindmap (https://plugins.jetbrains.com/plugin/8045-idea-mind-map)
- Java Runtime Environment (JRE).

# How to use
Step 1: place AndroidActivityMapGenerator.jar at same location of your AndroidManifact.xml

Step 2 : make AndroidActivityMapGenerator.jar executable
```sh
$ chmod +x AndroidActivityMapGenerator.jar
```

Step 3 : execute the jar file
```sh
$ java -jar AndroidActivityMapGenerator.jar
```

After that it will generate Activity graph inside graphResult folder

Open Android Studio and open graph.mmd

# How to handle Infinity loop

Some of activity might have two way relations(something like Activity A can launch Activity B and Activity B  can launch Activity A). This will create an infinity loop and cause chaos while generating the activity/fragment map.

The AndroidActivityMapGenerator will stop and show you an error if it detects an infinity loop.

All you have to do is write one line of comment that indicates which activity/fragment that you want to ignore.





License
----

MIT
