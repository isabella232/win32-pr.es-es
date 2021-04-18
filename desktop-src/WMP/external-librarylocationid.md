---
title: External. libraryLocationID
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Media Player de Windows externa. libraryLocationID
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698596"
---
# <a name="externallibrarylocationid"></a>External. libraryLocationID

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **libraryLocationID** recupera el identificador del elemento multimedia específico que se muestra actualmente en la vista del reproductor.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Esta propiedad funciona en combinación con la propiedad [external. libraryLocationType](external-librarylocationtype.md) . Por ejemplo, supongamos que **libraryLocationType** es igual a CPAlbumID y **libraryLocationID** es igual a 3. Esto significa que la vista actual de Windows Media Player muestra el álbum que tiene un identificador de 3. Para obtener más información acerca de cómo Windows Media Player caracteriza las vistas del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).

Algunas vistas de Windows Media Player están asociadas a un elemento multimedia determinado. Por ejemplo, si la vista actual representa un álbum individual, **libraryLocationType** es igual a CPAlbumID y **LIBRARYLOCATIONID** es el identificador del álbum. Otras vistas no están asociadas a ningún elemento multimedia determinado. Por ejemplo, si la vista actual representa todos los álbumes, **libraryLocationType** es igual a AllCPAlbumIDs, pero no hay ningún valor significativo que se pueda asignar a **libraryLocationID**. En los casos en los que la propiedad **libraryLocationID** no tiene ningún valor significativo, es igual a la cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





