---
title: Usar listas de reproducción automáticas para organizar el contenido de la biblioteca
description: Usar listas de reproducción automáticas para organizar el contenido de la biblioteca
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player tiendas en línea, listas de reproducción automáticas
- tiendas en línea, listas de reproducción automáticas
- tipo 1 tiendas en línea, listas de reproducción automáticas
- tipo 2 tiendas en línea, listas de reproducción automáticas
- Windows Media Player tiendas en línea, organizar el contenido de la biblioteca
- tiendas en línea, organizar el contenido de la biblioteca
- Escriba 1 tiendas en línea, organizar el contenido de la biblioteca
- tipo 2 tiendas en línea, organizar el contenido de la biblioteca
- Windows Media Player tiendas en línea, organización de contenido de biblioteca
- tiendas en línea, organización de contenido de biblioteca
- tipo 1 almacenes en línea, organización de contenido de biblioteca
- tipo 2 tiendas en línea, organización de contenido de biblioteca
- Biblioteca, organizar contenido
- organizar el contenido de la biblioteca
- listas de reproducción automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532248"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Usar listas de reproducción automáticas para organizar el contenido de la biblioteca

Puede usar listas de reproducción automáticas para organizar el contenido premium que proporcione. Por ejemplo, puede utilizar Windows Media Player para crear una lista de reproducción automática que solo contenga el contenido que proporcionó una clasificación de usuario de al menos cuatro estrellas. A continuación, puede Agregar la lista de reproducción automática a la biblioteca en Windows Media Player para que se muestre en el nodo música comprada en el nodo distribuidor de contenido.

Para ello, siga estos pasos:

1.  Cree la lista de reproducción automática.
2.  Con el explorador de Windows, vaya a la lista de reproducción automática y recupere el archivo. wpl.
3.  Con el modelo de objetos de Media Player de Windows, agregue la lista de reproducción automática a la biblioteca.
4.  Establezca el atributo **WM/ContentDistributor** para la lista de reproducción en el nombre de clave del distribuidor de contenido.
5.  Establezca el atributo **SyncOnly** para la lista de reproducción en true.

En el código de ejemplo de JScript siguiente se muestra una función que agrega una lista de reproducción automática denominada "Favorites Favorites" al nodo de Proseware en la biblioteca:


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

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Lista de reproducción. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Listas de reproducción estáticas y automáticas**](static-and-auto-playlists.md)
</dt> <dt>

[**Atributo SyncOnly**](synconly-attribute.md)
</dt> <dt>

[**Atributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




