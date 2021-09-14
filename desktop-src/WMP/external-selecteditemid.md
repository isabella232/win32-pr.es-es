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
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241844"
---
# <a name="externalselecteditemid"></a>External.selectedItemID

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad selectedItemID** recupera el identificador del elemento multimedia que está seleccionado actualmente en Reproductor de Windows Media.

## <a name="syntax"></a>Sintaxis

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

Esta propiedad se usa en combinación con la [propiedad External.selectedItemType.](external-selecteditemtype.md) Por ejemplo, si **selectedItemType** es igual a CPTrackID, **selectedItemID** es el identificador de la pista seleccionada. Para obtener más información sobre cómo Reproductor de Windows Media las vistas del contenido de la tienda en línea, vea [Ubicación y elemento seleccionado.](location-and-selected-item.md)

Algunas vistas de Reproductor de Windows Media tienen un elemento multimedia determinado que está seleccionado. Por ejemplo, suponga que la vista actual representa un álbum. Un álbum es un contenedor de pistas, por lo que **selectedItemType** es igual a CPTrackID y **selectedItemID** es el identificador de la pista seleccionada. Otras vistas no tienen un elemento multimedia seleccionado. Por ejemplo, si el usuario hace clic en el nodo raíz de la tienda en línea en el control de vista de árbol, Reproductor de Windows Media muestra una página de detección proporcionada por el almacén en línea. El reproductor no muestra ningún contenedor de elementos multimedia en la interfaz de usuario del reproductor. En ese caso, **selectedItemType es** igual a UnknownLocation y **selectedItemID** es igual a la cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





