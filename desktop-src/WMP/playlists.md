---
title: Listas
description: Listas
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media modelo de objetos, listas de reproducción
- modelo de objetos, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- Reproductor de Windows Media Móvil, listas de reproducción
- playlists,migration
- Windows Listas de reproducción de metarchivo multimedia, migración
- listas de reproducción de metarchivo, migración
- guía de migración, listas de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0933a5525d2085185ddf151da3c4765040305a22
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883231"
---
# <a name="playlists"></a>Listas

El Reproductor de Windows Media de objetos de control de ActiveX 6.4 incluye cuatro métodos y una propiedad para trabajar con listas de reproducción Windows metarchivo multimedia:

-   *Player6*. **GetCurrentEntry**
-   *Player6*. **SetCurrentEntry**
-   *Player6*. **GetMediaParameter**
-   *Player6*. **GetMediaParameterName**
-   *Player6*. **EntryCount**.

Juntos, proporcionan una funcionalidad limitada para navegar por un metarchivo de lista de reproducción con una extensión de nombre de archivo .asx y recuperar información sobre las entradas contenidas en la lista de reproducción.

Reproductor de Windows Media 7 introdujo "Media Library". La biblioteca permite a los usuarios organizar su contenido multimedia digital, así como crear listas de reproducción personalizadas que se pueden administrar desde la interfaz gráfica de usuario del reproductor. El modelo de objetos de control ActiveX de Reproductor de Windows Media 7 o posterior proporciona compatibilidad para trabajar con listas de reproducción de biblioteca, así como listas de reproducción contenidas en metarchivos multimedia de Windows con una extensión de nombre de archivo .asx.

> [!Note]  
> Por motivos de seguridad, el usuario debe conceder derechos de acceso a la biblioteca para que el programa pueda manipular su contenido. Los derechos de acceso solo se pueden solicitar y conceder a través Reproductor de Windows Media modelo de objetos de la serie 9 o posterior. Para obtener más información sobre los derechos de acceso, vea [Acceso a la biblioteca](library-access.md).

 

El Reproductor de Windows Media de objetos 7 o posterior incluye tres objetos para controlar listas de reproducción. El **objeto PlaylistCollection** proporciona funcionalidad para organizar listas de reproducción; representa toda la colección de listas de reproducción de la biblioteca del usuario. El **objeto PlaylistArray** proporciona una manera de recuperar una lista de reproducción específica del objeto **PlaylistCollection** mediante un número de índice; Dos de los métodos **del objeto PlaylistCollection** recuperan **un objeto PlaylistArray.** El **objeto Playlist** proporciona las propiedades y los métodos necesarios para manipular elementos multimedia contenidos en una sola lista de reproducción.

Por ejemplo, como cada lista de reproducción de la biblioteca tiene un nombre único, puede recuperar una lista de reproducción de la biblioteca mediante *PlaylistCollection*. **Método getByName:**


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



Con más frecuencia, querrá trabajar con la lista de reproducción actual. Aunque es posible usar varios objetos de lista de reproducción, el reproductor solo puede recuperar *uno.* **Propiedad currentPlaylist** en un momento dado: la que Reproductor de Windows Media está procesando en ese momento.

Cuando Reproductor de Windows Media 7 o posterior reproduce un metarchivo multimedia de Windows con una extensión de nombre de archivo .asx, primero crea un objeto **Lista de** reproducción. A continuación, rellena el objeto con la información de la lista de reproducción .asx y, a continuación, hace que ese objeto **de** lista de reproducción sea la lista de reproducción actual. Esto significa que puede usar las propiedades y los métodos asociados al objeto **Lista** de reproducción para manipular listas de reproducción .asx exactamente como controlaría las listas de reproducción de la biblioteca. Por ejemplo, para recuperar el número de entradas de una lista de reproducción .asx mediante el modelo de objetos de la versión 6.4, use *player6*. **Propiedad EntryCount:**


```C++
var entrycount = WMP64.EntryCount;

```



Cuando se usa el Reproductor de Windows Media objeto 7 o posterior, se usa la lista de *reproducción*. **count,** propiedad:


```C++
var entrycount = WMP9.currentPlaylist.count;

```



Al usar el control de la versión 6.4, puede usar *player6*. **Método GetCurrentEntry** para recuperar el índice de la entrada actual en una lista de reproducción .asx:


```C++
var entrynum = WMP64.GetCurrentEntry();

```



Puede lograr el mismo resultado mediante el uso de la Reproductor de Windows Media modelo de objetos 7 o posterior en el script. En el ejemplo JScript siguiente se compara el objeto multimedia actual con cada elemento de la lista de reproducción. Cuando *media*. **isIdentical devuelve** true, un cuadro de mensaje muestra el índice del elemento multimedia actual.


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



Para especificar el índice de la entrada actual en una lista de reproducción .asx, use *Player6*. **SetCurrentEntry**. Los índices de entrada de lista de reproducción de la versión 6.4 comienzan con 1, por lo que para que la segunda entrada de una lista de reproducción de metarchivo sea la actual, use la sintaxis siguiente:


```C++
WMP6.SetCurrentEntry(2);

```



Los índices de entrada de lista de reproducción se basan en cero Reproductor de Windows Media 7 o posterior; para convertir la segunda entrada en una lista de reproducción de metarchivo en la actual, al usar el modelo de objetos Reproductor de Windows Media 7 o posterior, use la sintaxis siguiente:


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



En el ejemplo JScript siguiente se muestra una función que acepta un número de índice como parámetro y, a continuación, hace que la entrada de lista de reproducción correspondiente al índice sea el elemento multimedia actual:


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



Windows Los metarchivos multimedia pueden contener elementos de parámetro personalizados, que se especifican mediante la **&lt; etiqueta PARAM. &gt;** Cuando se usa el modelo de objetos de la versión 6.4, puede recuperar el nombre de un parámetro determinado con *Player6*. **Método GetMediaParameterName.** En el ejemplo JScript siguiente se recupera el nombre del primer parámetro de la primera entrada de una lista de reproducción .asx:


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



De forma similar, puede recuperar el valor asociado al parámetro mediante *Player6*. **GetMediaParameter**:


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



En el ejemplo JScript siguiente se usa el modelo de objetos Reproductor de Windows Media 7 o posterior para recuperar el nombre y el valor del parámetro de la primera entrada de una lista de reproducción .asx:


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



Puede usar *PlaylistCollection*. **Método importPlaylist** para agregar una lista de reproducción .asx a la biblioteca. Una vez importado, la lista de reproducción de metarchivo se convierte en una lista de reproducción de biblioteca, por lo que puede manipularla con todas las propiedades y métodos a su disposición. El usuario debe conceder derechos de acceso completos a la biblioteca para que la aplicación pueda usar el **método importPlaylist.**

Puede usar *PlaylistCollection*. **getByName para** probar si existe una lista de reproducción. Este método siempre devuelve un objeto **PlaylistArray** válido. Si la matriz de lista de reproducción recuperada contiene exactamente una lista de reproducción, existe una lista de reproducción con ese nombre en la biblioteca. De lo contrario, la matriz de listas de reproducción no contendrá ningún objeto de lista de reproducción; esto significa que no hay ninguna lista de reproducción en la biblioteca con el nombre pasado como argumento al **método getByName.** En el JScript ejemplo siguiente se muestra esto:


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Guía de migración de modelos de objetos**](object-model-migration-guide.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> </dl>

 

 




