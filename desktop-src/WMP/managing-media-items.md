---
title: Administrar elementos multimedia
description: Administrar elementos multimedia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, administrar elementos multimedia
- Biblioteca, administrar elementos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148857"
---
# <a name="managing-media-items"></a>Administrar elementos multimedia

Un objeto **multimedia** representa un elemento multimedia. Tiene propiedades y métodos que puede usar para recuperar información y mostrarla al usuario, o para realizar diferentes acciones en función del valor que recupere.

Gran parte del trabajo con objetos **multimedia** implica metadatos sobre el contenido del elemento multimedia, denominados atributos. El tema [atributos de elemento multimedia](media-item-attributes.md) describe cómo leer y cambiar los valores de atributo. Además de este tema, consulte las instrucciones de uso de los [metadatos de Windows Media](/previous-versions/ms867702(v=msdn.10)) en el sitio web de Microsoft para obtener más información sobre los atributos y su uso.

El objeto **multimedia** tiene propiedades y métodos que recuperan algunos atributos directamente, como el nombre o la duración del elemento. En el caso de los elementos de vídeo, puede recuperar el alto y el ancho de la imagen, y puede recuperar la información del marcador basándose en el nombre o el índice de un marcador. También puede determinar si un elemento multimedia determinado se incluye en una lista de reproducción determinada.

## <a name="retrieving-a-media-object"></a>Recuperación de un objeto multimedia

Puede obtener acceso rápidamente al elemento multimedia actual mediante el *reproductor*. propiedad **currentMedia** .

A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente ejemplo de C# se recupera un objeto **multimedia** que representa el elemento actual.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital mediante el *reproductor*. método **newMedia** . Pasa el método a la ruta de acceso URL a un archivo multimedia digital y devuelve una referencia al nuevo objeto **multimedia** . El método no agrega el nuevo objeto a la biblioteca directamente. Sin embargo, puede pasar el objeto a la *lista de reproducción*. método **appendItem** o la *lista de reproducción*. método **insertItem** .

En el siguiente ejemplo de C# se crea un objeto **multimedia** basado en uno de los ejemplos de medios digitales instalados con el SDK de Windows Media Player.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Debe incluir dos barras diagonales inversas ( \) o usar el carácter @ en C#) en una cadena para representar un carácter de barra diagonal inversa real. Esto se debe a que C# usa un solo carácter de barra diagonal inversa para definir una secuencia de escape.

 

Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital y agregarlo a la biblioteca en un solo paso mediante el *MediaCollection*. **agregue** el método. Como el *reproductor*. método **newMedia** , el método **Add** toma una ruta de acceso a un archivo multimedia digital.

En el siguiente ejemplo de C# se crea un objeto **multimedia** basado en uno de los archivos de ejemplo del SDK y se agrega ese objeto a la biblioteca.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Puede recuperar un objeto **multimedia** que representa un elemento multimedia en una lista de reproducción mediante la *lista de reproducción*. método **Item** . En el siguiente ejemplo de C# se recupera el sexto elemento multimedia de la lista de reproducción actual.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




