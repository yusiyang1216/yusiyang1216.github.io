---
title: xcode修改快捷键
date: 2016-08-03 16:24:51
tags: ios
---

[http://blog.csdn.net/meegomeego/article/details/12971089](http://blog.csdn.net/meegomeego/article/details/12971089)

修改以下文件
/Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Resources/IDETextKeyBindingSet.plist

---
Deletions中添加：

```xml
<key>Delete Current Line</key>
<string>selectLine:, delete:</string>
```

Insertions and Indentations中添加：

```xml
<key>Insert NewLine Wherever</key>
<string>moveToEndOfLine:, insertNewline:</string>
<key>Duplicate Current Line</key>
<string>selectLine:, copy:, moveToEndOfLine:, insertNewline:, paste:, deleteBackward:</string>
<key>Copy Current Line</key>
<string>selectLine:, copy:</string>
<key>Paste Current Line</key>
<string>paste:</string>
```
Selection中添加：

```xml
<key>Move to Beginning Word of Line</key>
<string>moveToBeginningOfLine:, moveWordRight:, moveWordLeft:</string>
```
---

| 名称                            | 快捷键       |
|:-------------------------------|:------------|
| Delete Current Line            | Ctrl+D      |
| Insert NewLine Wherever        | Shift+Enter |
| Duplicate Current Line         | Ctrl+Alt+下 |
| Copy Current Line              | Ctrl+C      |
| Paste Current Line             | Ctrl+V      |
| Move to Beginning Word of Line | Home        |

---
移动代码上下行

{% asset_img F008AB67-1357-4433-921B-F6A59817ACEB.png [This is an example image] %}

---
xcode7.3已经加入了删除行的功能。

{% asset_img CC1F94DC-26E0-432F-A548-F881EBDEC8BF.png This is an example image %}

