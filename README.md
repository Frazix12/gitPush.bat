![Banner](https://capsule-render.vercel.app/api?type=waving&color=0:24ff62,100:34a354&height=200&text=gitPush.bat&&animation=fadeIn&fontColor=ffffff&fontAlignY=34)

<p aling="center">
 <h2>🔥 An Open Source <strong>.bat</strong> File For windows To Easily Push A Git Commit</h2>
</p>
<br />
<br />

# gitPush.bat

```bat
@ECHO OFF

SET comment=Saved on %date%-%time%

IF "%~1"=="" GOTO COMMIT
SET username=%1
SET comment=%comment% by %username%

:COMMIT
ECHO %comment%
git checkout development
git add .
git commit -m "%comment%"
git push origin
```