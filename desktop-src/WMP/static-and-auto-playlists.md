---
title: Listas de reproducción estáticas y automáticas
description: Listas de reproducción estáticas y automáticas
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media modelo de objetos, listas de reproducción
- modelo de objetos, listas de reproducción
- Reproductor de Windows Media Móvil, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- ActiveX control,listas de reproducción
- playlists,static
- listas de reproducción de metarchivo, static
- Windows Listas de reproducción de metarchivo multimedia, estáticas
- listas de reproducción estáticas
- listas de reproducción automáticas
- playlists,auto
- listas de reproducción de metarchivo, auto
- Windows Listas de reproducción de metarchivo multimedia, automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645b3bd9ca9ddeebcce9fd6cbb905caa54717e87876be6e449ebd4d3ab64a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568787"
---
# <a name="static-and-auto-playlists"></a>Listas de reproducción estáticas y automáticas

Hay dos tipos de listas de reproducción:

-   Listas de reproducción estáticas, que incluyen elementos multimedia específicos
-   Listas de reproducción automáticas, que buscan en la biblioteca cada vez que se abren y pueden contener elementos multimedia diferentes en momentos diferentes. Una lista de reproducción automática es el resultado de una consulta de base de datos.

Para importar una lista de reproducción estática desde un metarchivo, primero llame a *Player*. **newPlaylist para** crear un objeto **Playlist** basado en los datos del metarchivo y, a continuación, pasar ese objeto a *PlaylistCollection.* **importPlaylist para** agregar la lista de reproducción a la biblioteca.

Para importar una lista de reproducción automática desde un metarchivo, use *MediaCollection*. **agregue**. Para obtener más información, vea [Listas de reproducción y el objeto MediaCollection](playlists-and-the-mediacollection-object.md).

Para importar una lista de reproducción estática desde un metarchivo de lista de reproducción automática, use *Player*. **newPlaylist y** *PlaylistCollection*. **importPlaylist como** se ha descrito anteriormente. La lista de reproducción automática se ejecutará una vez y se creará una lista de reproducción estática en función del resultado de esa ejecución.

No se admite el uso de una lista de reproducción automática para consultar la biblioteca del usuario en las páginas web a las que los usuarios acceden a través de Internet.

En el siguiente código de ejemplo de C# se muestra cómo importar un metarchivo de lista de reproducción automática como una lista de reproducción estática. Para ejecutar este ejemplo, cree una lista de reproducción automática mediante la interfaz de usuario de la biblioteca e incluya la ruta de acceso correcta al metarchivo de lista de reproducción automática en este código.


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> </dl>

 

 




