## Modules

<dl>
<dt><a href="#module_VolumeService">VolumeService</a> ⇒ <code>Object</code></dt>
<dd><p>Volume Service.</p>
</dd>
<dt><a href="#module_StorageProvider">StorageProvider</a></dt>
<dd><p>Instance.</p>
</dd>
<dt><a href="#module_UtilsConnector">UtilsConnector</a></dt>
<dd></dd>
</dl>

## Constants

<dl>
<dt><a href="#STORAGE_CONSTANTS">STORAGE_CONSTANTS</a> ⇒ <code>Object</code></dt>
<dd><p>Storage to add/get content (volume, channel, etc.).</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#bootstrapPortalConnectors">bootstrapPortalConnectors()</a></dt>
<dd><p>Global PortalConnectors.</p>
</dd>
</dl>

<a name="module_VolumeService"></a>
## VolumeService ⇒ <code>Object</code>
Volume Service.

**Returns**: <code>Object</code> - Object with volume status.  

* [VolumeService](#module_VolumeService) ⇒ <code>Object</code>
    * [~setVolume()](#module_VolumeService..setVolume) ⇒ <code>boolean</code>
    * [~toggleMute()](#module_VolumeService..toggleMute) ⇒ <code>boolean</code>

<a name="module_VolumeService..setVolume"></a>
### VolumeService~setVolume() ⇒ <code>boolean</code>
Sets volume.

**Kind**: inner method of <code>[VolumeService](#module_VolumeService)</code>  
**Returns**: <code>boolean</code> - True if volume was successful.  
**Todo**

- [ ] Need check this function.

**Example**  
```js
volumeConnector.setVolume(10);
```
<a name="module_VolumeService..toggleMute"></a>
### VolumeService~toggleMute() ⇒ <code>boolean</code>
Toggles to audio and mute.

**Kind**: inner method of <code>[VolumeService](#module_VolumeService)</code>  
**Returns**: <code>boolean</code> - True if volume was toggled.  
**Todo**

- [ ] Need check this function.

<a name="module_StorageProvider"></a>
## StorageProvider
Instance.

**Todo**

- [ ] Nao deve instanciar duas vezes aqui


* [StorageProvider](#module_StorageProvider)
    * _static_
        * [.getFilePath(filename, asTemporary)](#module_StorageProvider.getFilePath) ⇒ <code>string</code>
        * [.writeFile(filename, content, asTemporary)](#module_StorageProvider.writeFile) ⇒ <code>boolean</code>
        * [.appendFile(filename, content, asTemporary)](#module_StorageProvider.appendFile) ⇒ <code>boolean</code>
        * [.readFile(filename, asTemporary)](#module_StorageProvider.readFile) ⇒ <code>string</code>
        * [.readFileAt(filePath)](#module_StorageProvider.readFileAt) ⇒ <code>string</code>
        * [.removeFile(filename, asTemporary)](#module_StorageProvider.removeFile)
        * [.removeFileAtPath(filePath)](#module_StorageProvider.removeFileAtPath)
        * [.getType(filename, asTemporary)](#module_StorageProvider.getType) ⇒ <code>string</code>
        * [.getTypeAt(filePath)](#module_StorageProvider.getTypeAt) ⇒ <code>string</code>
        * [.fileExists(filename, asTemporary)](#module_StorageProvider.fileExists) ⇒ <code>boolean</code>
        * [.existsAtPath(filePath)](#module_StorageProvider.existsAtPath) ⇒ <code>boolean</code>
        * [.createDir(basePath, dirName)](#module_StorageProvider.createDir)
        * [.listAt(path)](#module_StorageProvider.listAt) ⇒ <code>Array</code>
        * [.saveTmpOnFlash()](#module_StorageProvider.saveTmpOnFlash)
        * [.loadFlashOnTmp()](#module_StorageProvider.loadFlashOnTmp)
    * _inner_
        * [~startTuner()](#module_StorageProvider..startTuner)
        * [~stopTuner()](#module_StorageProvider..stopTuner) ⇒ <code>boolean</code>

<a name="module_StorageProvider.getFilePath"></a>
### StorageProvider.getFilePath(filename, asTemporary) ⇒ <code>string</code>
Gets filePath where is storaged all information
 in flash memory.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>string</code> - Complete path of file.  
**Todo**

- [ ] check it.


| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Specific filename. E.g: lastVolumeLevel |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.storageProvider('lastVolumeLevel', false);
```
<a name="module_StorageProvider.writeFile"></a>
### StorageProvider.writeFile(filename, content, asTemporary) ⇒ <code>boolean</code>
Writes a new configuration file in storage.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>boolean</code> - True if file was saved.  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Filename to write. |
| content | <code>string</code> | Configuration content. |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.writeFile('lastVolumeLevel', 10, true);
```
<a name="module_StorageProvider.appendFile"></a>
### StorageProvider.appendFile(filename, content, asTemporary) ⇒ <code>boolean</code>
Appends configuration or information to an
 existing file.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>boolean</code> - True if file was saved.  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Filename to append. |
| content | <code>string</code> | Configuration content. |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.appendFile('lastVolumeLevel', 20, false);
```
<a name="module_StorageProvider.readFile"></a>
### StorageProvider.readFile(filename, asTemporary) ⇒ <code>string</code>
Reads a file without filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>string</code> - File content.  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Filename to read. |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.readFile('lastVolumeLevel', true);
```
<a name="module_StorageProvider.readFileAt"></a>
### StorageProvider.readFileAt(filePath) ⇒ <code>string</code>
Reads a file with filePath in flash memory.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>string</code> - File content.  

| Param | Type | Description |
| --- | --- | --- |
| filePath | <code>string</code> | Filepath to read. |

**Example**  
```js
storageProvider.readFileAt('/flash/var/lastVolumeLevel');
```
<a name="module_StorageProvider.removeFile"></a>
### StorageProvider.removeFile(filename, asTemporary)
Removes a specific file without filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Filename to remove. |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.removeFile('lastVolumeLevel', true);
```
<a name="module_StorageProvider.removeFileAtPath"></a>
### StorageProvider.removeFileAtPath(filePath)
Removes a specific file with filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  

| Param | Type | Description |
| --- | --- | --- |
| filePath | <code>string</code> | Filepath to remove. |

**Example**  
```js
storageProvider.removeFileAtPath('/flash/var/lastVolumeLevel');
```
<a name="module_StorageProvider.getType"></a>
### StorageProvider.getType(filename, asTemporary) ⇒ <code>string</code>
Gets file type without filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>string</code> - File type.  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Filename to get type. |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.getFilePath('lastVolumeLevel', true);
```
<a name="module_StorageProvider.getTypeAt"></a>
### StorageProvider.getTypeAt(filePath) ⇒ <code>string</code>
Gets file type with filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>string</code> - File type.  

| Param | Type | Description |
| --- | --- | --- |
| filePath | <code>string</code> | Filepath to get type. |

**Example**  
```js
storageProvider.getFilePath('/flash/var/lastVolumeLevel');
```
<a name="module_StorageProvider.fileExists"></a>
### StorageProvider.fileExists(filename, asTemporary) ⇒ <code>boolean</code>
Checks if exists a specific file without filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>boolean</code> - True if file exists.  

| Param | Type | Description |
| --- | --- | --- |
| filename | <code>string</code> | Filename to check. |
| asTemporary | <code>boolean</code> | True if should get as temporary file. |

**Example**  
```js
storageProvider.fileExists('lastVolumeLevel', true);
```
<a name="module_StorageProvider.existsAtPath"></a>
### StorageProvider.existsAtPath(filePath) ⇒ <code>boolean</code>
Checks if exists a specific file with filePath.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>boolean</code> - True if file exists.  

| Param | Type | Description |
| --- | --- | --- |
| filePath | <code>string</code> | Filepath to check. |

**Example**  
```js
storageProvider.existsAtPath('/flash/var/lastVolumeLevel');
```
<a name="module_StorageProvider.createDir"></a>
### StorageProvider.createDir(basePath, dirName)
Creates a directory.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  

| Param | Type | Description |
| --- | --- | --- |
| basePath | <code>string</code> | Path where it'll be created. |
| dirName | <code>string</code> | Directory name. |

**Example**  
```js
storageProvider.createDir('/flash/var/', 'myDirectory');
```
<a name="module_StorageProvider.listAt"></a>
### StorageProvider.listAt(path) ⇒ <code>Array</code>
Shows file list.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>Array</code> - List of files.  

| Param | Type | Description |
| --- | --- | --- |
| path | <code>string</code> | Path to list. |

**Example**  
```js
storageProvider.listAt('/flash/var/');
```
<a name="module_StorageProvider.saveTmpOnFlash"></a>
### StorageProvider.saveTmpOnFlash()
Saves on temporary flash memory.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Example**  
```js
storageProvider.saveTmpOnFlash();
```
<a name="module_StorageProvider.loadFlashOnTmp"></a>
### StorageProvider.loadFlashOnTmp()
Loads temporary flash memory.

**Kind**: static method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Example**  
```js
storageProvider.loadFlashOnTmp();
```
<a name="module_StorageProvider..startTuner"></a>
### StorageProvider~startTuner()
Starts tuner.

**Kind**: inner method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Example**  
```js
tunerConnector.startTuner();
```
<a name="module_StorageProvider..stopTuner"></a>
### StorageProvider~stopTuner() ⇒ <code>boolean</code>
Stops tuner.

**Kind**: inner method of <code>[StorageProvider](#module_StorageProvider)</code>  
**Returns**: <code>boolean</code> - True if it was stopped.  
**Example**  
```js
tunerConnector.stopTuner();
```
<a name="module_UtilsConnector"></a>
## UtilsConnector
**Todo**

- [ ] Nao deve instanciar duas vezes aqui


* [UtilsConnector](#module_UtilsConnector)
    * [init](#exp_module_UtilsConnector--init) ⏏
        * [new init()](#new_module_UtilsConnector--init_new)
        * [.getMAC()](#module_UtilsConnector--init.getMAC) ⇒ <code>string</code>
        * [.getIP()](#module_UtilsConnector--init.getIP) ⇒ <code>string</code>
        * [.isPincodePurchaseEnabled()](#module_UtilsConnector--init.isPincodePurchaseEnabled) ⇒ <code>boolean</code>
        * [.setParentalRating(parentalRating)](#module_UtilsConnector--init.setParentalRating) ⇒ <code>number</code>

<a name="exp_module_UtilsConnector--init"></a>
### init ⏏
**Kind**: Exported class  
<a name="new_module_UtilsConnector--init_new"></a>
#### new init()
Initializes the UtilsConnector.

<a name="module_UtilsConnector--init.getMAC"></a>
#### init.getMAC() ⇒ <code>string</code>
Gets MAC Adress of network.

**Kind**: static method of <code>[init](#exp_module_UtilsConnector--init)</code>  
**Returns**: <code>string</code> - MAC Address.  
**Example**  
```js
utilsConnector.getMAC();
```
<a name="module_UtilsConnector--init.getIP"></a>
#### init.getIP() ⇒ <code>string</code>
Gets IP of network.

**Kind**: static method of <code>[init](#exp_module_UtilsConnector--init)</code>  
**Returns**: <code>string</code> - Network IP.  
**Example**  
```js
utilsConnector.getIP();
```
<a name="module_UtilsConnector--init.isPincodePurchaseEnabled"></a>
#### init.isPincodePurchaseEnabled() ⇒ <code>boolean</code>
Checks if PIN Purchase is activated.

**Kind**: static method of <code>[init](#exp_module_UtilsConnector--init)</code>  
**Returns**: <code>boolean</code> - True if PIN Purchase is activated.  
**Example**  
```js
utilsConnector.isPincodePurchaseEnabled();
```
<a name="module_UtilsConnector--init.setParentalRating"></a>
#### init.setParentalRating(parentalRating) ⇒ <code>number</code>
Sets Parental Rating.

**Kind**: static method of <code>[init](#exp_module_UtilsConnector--init)</code>  
**Returns**: <code>number</code> - Parental rating value.  

| Param | Type | Description |
| --- | --- | --- |
| parentalRating | <code>number</code> | Parental rating number. |

**Example**  
```js
utilsConnector.setParentalRating();
```
<a name="STORAGE_CONSTANTS"></a>
## STORAGE_CONSTANTS ⇒ <code>Object</code>
Storage to add/get content (volume, channel, etc.).

**Kind**: global constant  
**Returns**: <code>Object</code> - BASE_PATH  
**Todo**

- [ ] Implement.


| Param | Type |
| --- | --- |
| BASE_PATH | <code>Object</code> | 

<a name="bootstrapPortalConnectors"></a>
## bootstrapPortalConnectors()
Global PortalConnectors.

**Kind**: global function  
**Todo**

- [ ] Implement documentation.

