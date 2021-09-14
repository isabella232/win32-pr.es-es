---
title: Administración de elementos multimedia
description: Administración de elementos multimedia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media modelo de objetos,library
- object model,library
- Reproductor de Windows Media Mobile,library para el modelo de objetos
- Reproductor de Windows Media ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,biblioteca para el modelo de objetos
- ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media, administrar elementos multimedia
- library,managing media items
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967548"
---
# <a name="managing-media-items"></a>Administración de elementos multimedia

Un **objeto Media** representa un elemento multimedia. Tiene propiedades y métodos que puede usar para recuperar información y mostrarla al usuario, o para realizar diferentes acciones en función del valor que recupere.

Gran parte del trabajo con objetos **Multimedia** implica metadatos sobre el contenido del elemento multimedia, denominados atributos. En el tema [Atributos de elementos multimedia](media-item-attributes.md) se describe cómo leer y cambiar los valores de atributo. Además de este tema, consulte las directrices de uso de [metadatos](/previous-versions/ms867702(v=msdn.10)) de Windows multimedia en el sitio web de Microsoft para obtener más información sobre los atributos y su uso.

El **objeto** Media tiene propiedades y métodos que recuperan algunos atributos directamente, como el nombre o la duración del elemento. Para los elementos de vídeo, puede recuperar el alto y el ancho de la imagen, y puede recuperar la información de marcador en función del nombre o el índice de un marcador. También puede determinar si un elemento multimedia determinado se incluye en una lista de reproducción determinada.

## <a name="retrieving-a-media-object"></a>Recuperar un objeto multimedia

Puede acceder rápidamente al elemento multimedia actual mediante el Reproductor *de*. **propiedad currentMedia.**

A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente ejemplo de C# se recupera un **objeto Media** que representa el elemento actual.


```C++
IWMPMedia media;
media = Player.currentMedia;

```



Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital mediante el *Reproductor de*. **método newMedia.** Se pasa al método la ruta de acceso url a un archivo multimedia digital y se devuelve una referencia al nuevo **objeto** Media. El método no agrega directamente el nuevo objeto a la biblioteca. Sin embargo, puede pasar el objeto a la lista de *reproducción*. **Método appendItem** o lista *de reproducción*. **Método insertItem.**

En el siguiente ejemplo de C# se crea un **objeto Media** basado en uno de los ejemplos de medios digitales instalados con Reproductor de Windows Media SDK.


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> Debe incluir dos caracteres de barra diagonal inversa ( ) (o usar el carácter @ en C#) en una cadena para representar un carácter de barra diagonal \\ inversa real. Esto se debe a que C# usa un único carácter de barra diagonal inversa para definir una secuencia de escape.

 

Puede crear un nuevo elemento multimedia a partir de un archivo multimedia digital y agregarlo a la biblioteca en un paso mediante *MediaCollection*. **add** method. Al igual que *el reproductor*. **método newMedia,** el **método add** toma una ruta de acceso a un archivo multimedia digital.

En el siguiente ejemplo de C# se crea un **objeto Media** basado en uno de los archivos de ejemplo del SDK y se agrega ese objeto a la biblioteca.


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



Puede recuperar un objeto **Media que representa** un elemento multimedia en una lista de reproducción mediante la lista de *reproducción*. **método item.** En el siguiente ejemplo de C# se recupera el sexto elemento multimedia de la lista de reproducción actual.


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




