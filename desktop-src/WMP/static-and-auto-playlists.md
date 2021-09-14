---
title: Listas de reproducción estáticas y automáticas
description: Listas de reproducción estáticas y automáticas
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media de objetos, listas de reproducción
- object model,playlists
- Reproductor de Windows Media Móvil, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- ActiveX control,listas de reproducción
- playlists,static
- listas de reproducción de metarchivo, static
- Windows Listas de reproducción de metarchivo multimedia,static
- listas de reproducción estáticas
- listas de reproducción automáticas
- listas de reproducción, auto
- listas de reproducción de metarchivo, auto
- Windows Listas de reproducción de metarchivo multimedia, auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241724"
---
# <a name="static-and-auto-playlists"></a>Listas de reproducción estáticas y automáticas

Hay dos tipos de listas de reproducción:

-   Listas de reproducción estáticas, que incluyen elementos multimedia específicos
-   Listas de reproducción automáticas, que buscan en la biblioteca cada vez que se abren y pueden contener elementos multimedia diferentes en momentos diferentes. Una lista de reproducción automática es el resultado de una consulta de base de datos.

Para importar una lista de reproducción estática desde un metarchivo, llame primero al *reproductor*. **newPlaylist para** crear un objeto **Playlist** basado en los datos del metarchivo y, a continuación, pasar ese objeto a *PlaylistCollection*. **importPlaylist para** agregar la lista de reproducción a la biblioteca.

Para importar una lista de reproducción automática desde un metarchivo, use *MediaCollection*. **agregue**. Para obtener más información, vea [Listas de reproducción y el objeto MediaCollection](playlists-and-the-mediacollection-object.md).

Para importar una lista de reproducción estática desde un metarchivo de lista de reproducción automática, use el *reproductor*. **newPlaylist** y *PlaylistCollection*. **importPlaylist como** se describió anteriormente. La lista de reproducción automática se ejecutará una vez y se creará una lista de reproducción estática en función del resultado de esa ejecución.

No se admite el uso de una lista de reproducción automática para consultar la biblioteca del usuario en las páginas web a las que los usuarios acceden a través de Internet.

En el siguiente código de ejemplo de C# se muestra cómo importar un metarchivo de lista de reproducción automática como una lista de reproducción estática. Para ejecutar este ejemplo, cree una lista de reproducción automática mediante la interfaz de usuario de la biblioteca y, a continuación, incluya la ruta de acceso correcta al metarchivo de lista de reproducción automática en este código.


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

 

 




