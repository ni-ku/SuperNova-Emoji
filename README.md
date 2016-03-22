
## SuperNova-Emoji

[SuperNova-Emoji](https://github.com/hani-momanii/SuperNova-Emoji) is a library to implement and render emojis.


## Java Usage

To use default colors : 
EmojIconActions(Context ctx,View rootView,EmojiconEditText emojiconEditText,ImageView emojiButton)
```
EmojIconActions  emojIcon=new EmojIconActions(this,rootView,emojiconEditText,emojiButton);
emojIcon.ShowEmojIcon();
```

![image](https://github.com/hani-momanii/SuperNova-Emoji/blob/master/ios.png)


To use custom color :
EmojIconActions(Context ctx,View rootView,EmojiconEditText emojiconEditText,ImageView emojiButton,String iconPressedColor,String tabsColor,String backgroundColor)
```
EmojIconActions  emojIcon=new EmojIconActions(this,rootView,emojiconEditText,emojiButton,"#495C66","#DCE1E2","#E6EBEF");
emojIcon.ShowEmojIcon();
```
![image](https://github.com/hani-momanii/SuperNova-Emoji/blob/master/color.png)



To Listen to keyboard status 
```
emojIcon.setKeyboardListener(new EmojIconActions.KeyboardListener() {
@Override
public void onKeyboardOpen() {
    Log.e("Keyboard","open");
  }

@Override
public void onKeyboardClose() {
  Log.e("Keyboard","close");
}
});
```
To use the device default emoji
```
emojIcon.setUseSystemEmoji(true);
emojiconEditText.setUseSystemEmoji(true);
```
![image](https://github.com/hani-momanii/SuperNova-Emoji/blob/master/def.png)



## XML Usage

```
<hani.momanii.supernova_emoji_library.Helper.EmojiconEditText
        android:id="@+id/emojicon_edit_text"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        emojicon:emojiconSize="28sp" />
        
        
<hani.momanii.supernova_emoji_library.Helper.EmojiconTextView
        android:id="@+id/emojicon_text_view"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" 
        emojicon:emojiconSize="28sp"/>

```



## Usage

* `EmojiconTextView`: a `TextView` which can render emojis.
* `EmojiconEditText`: a `EditText` which can render emojis.
* `EmojiconMultiAutoCompleteTextView`: a `MultiAutoCompleteTextView` which can render emojis.

## Building in IntelliJ

Via Gradle:

```

repositories {
    maven { url "https://dl.bintray.com/hani-momanii/maven"}
}
  compile 'hani.momanii.supernova_emoji_library:supernova-emoji-library:0.0.2'
```

## Acknowledgements

Based on Hieu Rocker's [library Emojicon Github](https://github.com/rockerhieu/emojicon/).

Based on Ankushsachdeva  [library Emojicon Github](https://github.com/ankushsachdeva/emojicon/).

Emojicon is using emojis graphics from [emoji-cheat-sheet.com](https://github.com/arvida/emoji-cheat-sheet.com/tree/master/public/graphics/emojis).

## License

* [Apache Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

```
Copyright 2016 Hani Al-Momani

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
