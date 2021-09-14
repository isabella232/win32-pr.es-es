---
title: Usar listas de reproducción automáticas para organizar el contenido en la biblioteca
description: Usar listas de reproducción automáticas para organizar el contenido en la biblioteca
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Reproductor de Windows Media en línea, listas de reproducción automáticas
- tiendas en línea, listas de reproducción automáticas
- tiendas en línea de tipo 1, listas de reproducción automáticas
- tiendas en línea de tipo 2, listas de reproducción automáticas
- Reproductor de Windows Media en línea, organización del contenido de la biblioteca
- tiendas en línea, organización del contenido de la biblioteca
- tiendas en línea de tipo 1, organización del contenido de la biblioteca
- tiendas en línea de tipo 2, organización del contenido de la biblioteca
- Reproductor de Windows Media en línea, organización de contenido de biblioteca
- tiendas en línea, organización de contenido de biblioteca
- tiendas en línea de tipo 1, organización de contenido de biblioteca
- tiendas en línea de tipo 2, organización de contenido de biblioteca
- library,organización de contenido
- organizar el contenido de la biblioteca
- listas de reproducción automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070852"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Usar listas de reproducción automáticas para organizar el contenido en la biblioteca

Puede usar listas de reproducción automáticas para organizar el contenido premium que proporcione. Por ejemplo, podría usar Reproductor de Windows Media para crear una lista de reproducción automática que contenga solo el contenido proporcionado con una clasificación de usuario de al menos cuatro estrellas. A continuación, puede agregar la lista de reproducción automática a la biblioteca de Reproductor de Windows Media para que se muestre en el nodo Purchased Música en el nodo del distribuidor de contenido.

Para ello, realice los pasos siguientes:

1.  Cree la lista de reproducción automática.
2.  Con Windows Explorer, vaya a la lista de reproducción automática y recupere el archivo .wpl.
3.  Con el Reproductor de Windows Media de objetos, agregue la lista de reproducción automática a la biblioteca.
4.  Establezca el **atributo WM/ContentDistributor de la** lista de reproducción en el nombre de la clave del distribuidor de contenido.
5.  Establezca el **atributo SyncOnly** de la lista de reproducción en true.

En el JScript ejemplo siguiente se muestra una función que agrega una lista de reproducción automática denominada "Favoritos aciertos" al nodo Proseware de la biblioteca:


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la integración de bibliotecas](download-manager-overview.md)
</dt> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Listas de reproducción estáticas y automáticas**](static-and-auto-playlists.md)
</dt> <dt>

[**Atributo SyncOnly**](synconly-attribute.md)
</dt> <dt>

[**Atributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




