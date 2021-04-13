---
title: Listas de reproducción estáticas y automáticas
description: Listas de reproducción estáticas y automáticas
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, estáticas
- listas de reproducción de metarchivo, estáticas
- Listas de reproducción de metarchivos de Windows Media, estáticas
- listas de reproducción estáticas
- listas de reproducción automáticas
- listas de reproducción, auto
- listas de reproducción de metarchivo, automática
- Listas de reproducción de metarchivos de Windows Media, automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418447"
---
# <a name="static-and-auto-playlists"></a>Listas de reproducción estáticas y automáticas

Hay dos tipos de listas de reproducción:

-   Listas de reproducción estáticas, que incluyen elementos multimedia específicos
-   Listas de reproducción automáticas, que buscan en la biblioteca cada vez que se abren y pueden contener diferentes elementos multimedia en momentos diferentes. Una lista de reproducción automática es el resultado de una consulta de base de datos.

Para importar una lista de reproducción estática desde un metarchivo, primero llame a *Player*. **reproducción** para crear un objeto de **lista de reproducción** basado en los datos del metarchivo y, a continuación, pase ese objeto a *PlaylistCollection*. **importPlaylist** para agregar la lista de reproducción a la biblioteca.

Para importar una lista de reproducción automática desde un metarchivo, use *MediaCollection*. **Agregar**. Para obtener más información, vea [listas de reproducción y el objeto MediaCollection](playlists-and-the-mediacollection-object.md).

Para importar una lista de reproducción estática de un metarchivo de lista de reproducción automática, use *Player*. **reproducción** y *PlaylistCollection*. **importPlaylist** como se describió anteriormente. La lista de reproducción automática se ejecutará una vez y se creará una lista de reproducción estática según el resultado de esa ejecución.

No se admite el uso de una lista de reproducción automática para consultar la biblioteca del usuario para las páginas web a las que los usuarios tienen acceso a través de Internet.

El siguiente código de ejemplo de C# muestra cómo importar un metarchivo de lista de reproducción automática como una lista de reproducción estática. Para ejecutar este ejemplo, cree una lista de reproducción automática mediante la interfaz de usuario de la biblioteca y, a continuación, incluya la ruta de acceso correcta al metarchivo de lista de reproducción automática en este código.


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

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> </dl>

 

 




