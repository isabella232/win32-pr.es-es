---
title: External.libraryLocationType
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External.libraryLocationType Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241934"
---
# <a name="externallibrarylocationtype"></a>External.libraryLocationType

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad libraryLocationType** recupera una constante [de](library-location-constants.md) ubicación de biblioteca que indica el tipo de la vista actual en Reproductor de Windows Media.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura** que contiene una de las constantes de ubicación de la biblioteca.

## <a name="remarks"></a>Observaciones

Esta propiedad funciona en combinación con la [propiedad External.libraryLocationID.](external-librarylocationid.md) Por ejemplo, suponga **que libraryLocationType** es igual a CPAlbumID y **libraryLocationID** es igual a 3. Esto significa que la vista actual Reproductor de Windows Media muestra el álbum que tiene un identificador de 3. Para obtener más información sobre cómo Reproductor de Windows Media las vistas del contenido de la tienda en línea, vea [Ubicación y elemento seleccionado.](location-and-selected-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





