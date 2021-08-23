---
title: External.selectedItemID
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. | External.selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External.selectedItemID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea4b93656adc3fab25ab96e41fe417bde158035c5c11a0af9be84c5d555b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648435"
---
# <a name="externalselecteditemid"></a>External.selectedItemID

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad selectedItemID** recupera el identificador del elemento multimedia que está seleccionado actualmente en Reproductor de Windows Media.

## <a name="syntax"></a>Syntax

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Comentarios

Esta propiedad se usa en combinación con la [propiedad External.selectedItemType.](external-selecteditemtype.md) Por ejemplo, si **selectedItemType es** igual a CPTrackID, **selectedItemID** es el identificador de la pista seleccionada. Para obtener más información sobre cómo Reproductor de Windows Media las vistas del contenido de la tienda en línea, vea [Ubicación y elemento seleccionado.](location-and-selected-item.md)

Algunas vistas de Reproductor de Windows Media tienen un elemento multimedia determinado que está seleccionado. Por ejemplo, supongamos que la vista actual representa un álbum. Un álbum es un contenedor de pistas, por lo que **selectedItemType** es igual a CPTrackID y **selectedItemID** es el identificador de la pista seleccionada. Otras vistas no tienen un elemento multimedia seleccionado. Por ejemplo, si el usuario hace clic en el nodo raíz de la tienda en línea en el control de vista de árbol, Reproductor de Windows Media muestra una página de detección proporcionada por el almacén en línea. El reproductor no muestra ningún contenedor de elementos multimedia en la interfaz de usuario del reproductor. En ese caso, **selectedItemType es** igual a UnknownLocation y **selectedItemID** es igual a la cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.selectedItemType**](external-selecteditemtype.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





