# 202022 Open folder with Editor Programs : VSCode, Typora, Iterm2

## Final Result

1. Right Click to open folder with certain programs: Iterm2, Typora, VSC etc... 

![Screen Shot 2020-02-22 at 1.32.43 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.32.43 PM.png)

2. For Macbook Pros with touch bars, you can open folder with programs with one click. 

<video src="/Users/noopy/_gaemin/200222 콩의날/KakaoTalk_Video_2020-02-22-13-33-02.mp4"></video>



## How

1. Spotlight(CMD + Space) to find Automator. 

![Screen Shot 2020-02-22 at 1.39.35 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.39.35 PM.png)

2. Choose Quick Action

![Screen Shot 2020-02-22 at 1.25.43 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.25.43 PM.png)

3. You'll get this screen after selecting quick action

![Screen Shot 2020-02-22 at 1.25.49 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.25.49 PM.png)

4. On the left side of panel, search for "Run Shell Script"

![Screen Shot 2020-02-22 at 1.26.04 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.26.04 PM.png)

5. Then, on the right side of panel will look like this. Now We are ready to customize this quickaction one-by-one.

![Screen Shot 2020-02-22 at 1.26.12 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.26.12 PM.png)

6. Workflow receives current "files or folders"

![Screen Shot 2020-02-22 at 1.26.21 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.26.21 PM.png)

7. Workflow receives current "files or folders" in "Finder"

![Screen Shot 2020-02-22 at 1.26.27 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.26.27 PM.png)

8. (optional) Choose Icon which intuitively displays the action for you.

![Screen Shot 2020-02-22 at 1.26.37 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 1.26.37 PM.png)

9. Select shell as "/bin/bash" and write the script(AppleScript) as following:

![Screen Shot 2020-02-22 at 12.32.35 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 12.32.35 PM.png)

For VSCode: 

```shell
for f in "$@"; do
    open -a 'Visual Studio Code' "$f"
done
```

For iTerm:

```shell
for f in "$@"; do
    open -a iTerm "$f"
done
```

For Typora: 

```shell
for f in "$@"; do
    open -a typora "$f"
done
```

10. Pass input "as arguments"

![Screen Shot 2020-02-22 at 12.27.20 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 12.27.20 PM.png)

11. After the process 1 ~ 10, it should look like the following:

![Screen Shot 2020-02-22 at 12.25.23 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 12.25.23 PM.png)

12. CMD+S to save the quickaction and name the quick action.

13. Quickactions can be archived on Services folders. You can rename/delete/edit your quickactions here. 

![Screen Shot 2020-02-22 at 12.44.27 PM](/Users/noopy/_gaemin/200222 콩의날/Screen Shot 2020-02-22 at 12.44.27 PM.png)

## Version

- Mac OS Cattalina ver. 10.15.3
- Macbook Pro 16 inch model

## Reference

- [How to add a right click option in folder to open the folder with an application like VS Code](https://apple.stackexchange.com/questions/238948/osx-how-to-add-a-right-click-option-in-folder-to-open-the-folder-with-an-applic)

- [Automator Specifications](http://www.macosxautomation.com/automator/services/index.html)

