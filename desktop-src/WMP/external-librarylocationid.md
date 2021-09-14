---
title: External.libraryLocationID
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External.libraryLocationID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241941"
---
# <a name="externallibrarylocationid"></a>External.libraryLocationID

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad libraryLocationID** recupera el identificador del elemento multimedia específico que se muestra actualmente en la vista del reproductor.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

Esta propiedad funciona en combinación con la [propiedad External.libraryLocationType.](external-librarylocationtype.md) Por ejemplo, suponga **que libraryLocationType** es igual a CPAlbumID y **libraryLocationID** es igual a 3. Esto significa que la vista actual Reproductor de Windows Media muestra el álbum que tiene un identificador de 3. Para obtener más información sobre cómo Reproductor de Windows Media las vistas del contenido de la tienda en línea, vea [Ubicación y elemento seleccionado.](location-and-selected-item.md)

Algunas vistas de Reproductor de Windows Media están asociadas a un elemento multimedia determinado. Por ejemplo, si la vista actual representa un álbum individual, **libraryLocationType** es igual a CPAlbumID y **libraryLocationID** es el identificador del álbum. Otras vistas no están asociadas a ningún elemento multimedia determinado. Por ejemplo, si la vista actual representa todos los álbumes, **libraryLocationType** es igual a AllCPAlbumIDs, pero no hay ningún valor significativo que se pueda asignar a **libraryLocationID.** En los casos en los que la propiedad **libraryLocationID** no tiene ningún valor significativo, es igual a la cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





