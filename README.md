# What is that?
SLywnow basic is main library for any SLywnow's assets, like SLM, AutoLang e.tc. To use it type `using SLywnow` in your script. Asset also include [ZipUtil](https://github.com/tsubaki/UnityZip "ZipUtil").

# Save system
### How it works
SaveSystemAlt is my alternative to PlayerPerfs, that have no limits of size, have multifiles system, have GUI inside Unity and can save Arrays and Lists.

### Usage

`StartWork(int i=0)` - run SaveSystemAlt by some index (different indexes mean different save files)

`UseDebug(bool value)` - show debug messages

`bool IsWorking()` - is SaveSystemAlt working?

`SetString(string key, string value)` - save some string with some key in current session, to write it into file use `SaveUpdatesNotClose()` or `StopWorkAndClose()`

`SetInt(string key, int value)` - save some int with some key in current session, to write it into file use `SaveUpdatesNotClose()` or `StopWorkAndClose()`

`SetFloat(string key, float value)` - save some float with some key in current session, to write it into file use `SaveUpdatesNotClose()` or `StopWorkAndClose()`

`SetBool(string key, bool value)` - save some bool with some key in current session, to write it into file use `SaveUpdatesNotClose()` or `StopWorkAndClose()`

`SetArray<T>(string key, T[] array)` - save some array of any types with some key in current session, to write it into file use `SaveUpdatesNotClose()` or `StopWorkAndClose()`

`string GetString(string key, string def=null,bool fromanytype=false)` - return string from key, if key not found will return *def* value, use *fromanytype* to get value from any types, not only from strings

`int GetInt(string key, int def = 0)` - return int from key, if key not found will return *def* value

`float GetFloat(string key, float def = 0)` - return float from key, if key not found will return *def* value

`bool GetBool(string key, bool def = false)` - return bool from key, if key not found will return *def* value

`T[] GetArray<T>(string key)` - return array of any type from key, if key not found will return *def* value

`SetValueToUndefined(string key)` - change key type to Undefined, Undefined type can be reads/writes from any types (by converted to string)

`SetValueToSomeType(string key, SaveSystemSL.SSLTpe type)` - change value type to another

`bool HasKey(string key)` - is key exist in current session?

`RenameKey(string key, string newName)` - rename some key in current session

`DeleteKey(string key)` - delete some key in current session

`DeleteAll(string key, bool withFile = false)` - delete all keys in current session

`int IsIndex()` - return current session's index (from StartWork)

`StopWorkAndClose()` - stop current session and write all changes to file

`SaveUpdatesNotClose()` - write all changes to file but not stop current session

`OutputSSAData GetData(string key)` - convert some key's data to OutputSSAData class. Use it to move keys between indexes

`WriteData(OutputSSAData input)` - add some key from OutputSSAData to current session. Use it to move keys between indexes

### GUI
To open GUI press SLywnow/Save System Alt Editor. This editor works only in non-play mode.

![](https://i.imgur.com/iB1tGtw.png)
1. Index number, press "Open" to load this 
2. Search field
3. Name and type of key
4. Value of key
5. Delete key
6. Add new key
7. Save all changes 
8. Show/Hide options
9. Show labels of keys as input (only for copy, you can't edit them here)
10. Set custom CultureInfo, leave it empty for InvariantCulture. Use it if your CultureInfo is different or if you use some other CultureInfo in the game
11. Save and hide options

# Time savers
### FilesSet

##### LoadByte 
`byte[] LoadByte(string path, string name, string format, bool datapath = false)` - 

`byte[] LoadByte(string path, bool datapath = false)` - 

##### SaveStream 
`SaveStream(string path, string name, string format, string[] saves, bool datapath = false, bool add = false)` - 

`SaveStream(string path, string[] saves, bool datapath = false, bool add = false)` - 

`SaveStream(string path, string name, string format, string save, bool datapath = false, bool add = false)` - 

`SaveStream(string path, string save, bool datapath = false, bool add = false)` - 

##### LoadStream
`string LoadStream(string path, string name, string format, bool datapath = false)` - 

`string LoadStream(string path, bool datapath = false)` - 

`string LoadStream(string path, string name, string format, bool datapath = false, bool onlyoneline = false)` - 

`string LoadStream(string path, bool datapath = false, bool onlyoneline = false)` - 

##### LoadSprite
`Sprite LoadSprite(string path, string name, string format, bool datapath = false)` - 

`Sprite LoadSprite(string path, bool datapath = false)` - 


`SaveTexture(Texture2D input, string path, TextureType format, bool datapath = false)` - 

##### CheckFile
`bool CheckFile(string path, string name, string format, bool datapath = false)` - 

`bool CheckFile(string path, bool datapath = false)` - 

`bool CheckDirectory(string path, bool datapath = false)` - 

`DelStream(string path, string name, string format, bool datapath = false, bool dirtoo = false, bool forse = false)` - 

`DelStream(string path, bool datapath = false, bool dirtoo = false, bool forse = false)` - 

`string[] GetFilesFromdirectories(string path, string format, bool datapath = false, TypeOfGet type = TypeOfGet.Files)` - 

`CreateDirectory(string path, bool datapath = false)` - 

`RenameFile(string path, string oldName, string newName)` - 

`CopyFullDirectory(string sourceDirectory, string targetDirectory)` - 

`string[] ConcatArray(string[] array1, string[] array2)` - 

### FastFind

`GameObject InCords(Vector3 position, bool first, string tag = null, string[] blocktags = null)` - 

`GameObject[] AllInCords(Vector3 position, string tag = null, string[] blocktags = null)` - 

`string GetDefaultPath()` - 

`Transform FindChild(Transform parent, string name)` - 

### EasyDo

`Texture2D byteToTexture(byte[] input)` - 

`List<List<T>> RemoveIndex<T>(List<List<T>> tomove, List<int> indexs, int index, int newplace)` - 

`List<List<T>> MoveIndex<T>(List<List<T>> tomove, List<int> indexs, int index, int newplace)` - 

`CreateIndex(out List<int> output, List<int> input, int min = 100000, int max = 999999)` - 

`string[] UIMultiLineToStringArray(string input, string enter = "\n")` - 

`string StringArrayToUIMultiLine(string[] input, string enter = "\n")` - 

`Color MoveToColor(Color from, Color to, float speed, byte r = 255, byte g = 255, byte b = 255)` - 

`Color MoveToColorWithAlpha(Color from, Color to, float speed, byte r = 255, byte g = 255, byte b = 255, byte a = 255)` - 

`Color SetPositionColor(Color from, Color to, float position)` - 

`Texture GetWWWTexture(string url, bool unlimited = false, float maxtime = 1000f)` - 

`AudioClip GetWWWAudio(string url, bool unlimited = false, float maxtime = 1000f)` - 

`string GetWWWString(string url, bool unlimited = false, float maxtime=1000f)` - 

`byte[] GetWWWBytes(string url, bool unlimited = false, float maxtime = 1000f)` - 

`T[] JSONtoArray<T>(string json)` - 

`Shuffle<T>(this List<T> list)` - 

`Swap<T>(this List<T> list, int i, int j)` - 

# JSON works
### FastJSONTests

`DateTime getTime(string from = "http://worldtimeapi.org/api/timezone/Europe/Moscow")` - 

`string getIp(string from = "http://worldtimeapi.org/api/timezone/Europe/Moscow")` - 

### JsonHelper

`T[] FromJson<T>(string json)` - 

`string ToJson<T>(T[] array)` - 

`string ToJson<T>(T[] array, bool prettyPrint)` - 

`Move<T>(this List<T> list, int i, int j)` - 

`List<T> Clone<T>(this List<T> list)` - 

` Swap<T>(this List<T> list, int i, int j)` - 

# UI works
### UIEditor

`Sprite GetSpriteWithColor(Color color, int width = 1, int height = 1, float pivotX = 0.5f, float pivotY = 0.5f)` - 

`Texture2D GetTextureWithColor(Color color, int width = 1, int height = 1)` - 

`Sprite GetSpriteWithGradient(Gradient gradient, bool Xdirection, int width = 1, int height = 1, float pivotX = 0.5f, float pivotY = 0.5f)` - 

`Sprite GetSpriteWithGradient2D(Gradient gradientX, Gradient gradientY, int width = 1, int height = 1, float pivotX = 0.5f, float pivotY = 0.5f)` - 

`FillDropDownByTextList(out Dropdown dropdown, List<string> strings, Dropdown enter)` - 

`FillDropDownBySpriteList(out Dropdown dropdown, List<Sprite> sprites, Dropdown enter)` - 

`FillDropDownBySpriteAndTextList(out Dropdown dropdown, List<Sprite> sprites, List<string> strings, Dropdown enter)` - 

`FillDropDownByColorList(out Dropdown dropdown, List<Color> colors, Dropdown enter)` - 

`FillDropDownByColorAndTextList(out Dropdown dropdown, List<Color> colors, List<string> strings, Dropdown enter)` - 

`string GetStringUIEvent(string input, int pos, char space, string def = null)` - 

`int GetIntUIEvent(string input, int pos, char space, int def = 0)` - 

`float GetFloatUIEvent(string input, int pos, char space, float def = 0)` - 

`bool GetBoolUIEvent(string input, int pos, char space, bool def = false)` - 

`SetPositionInHierarchy(Transform parent, GameObject moved, PositionInHierarchyVector vectors, bool movetoparent, bool usesizes = true)` - 

# Attributes

### Button Attributes

### Show/Hide Attributes