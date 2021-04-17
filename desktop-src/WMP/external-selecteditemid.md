---
title: External. selectedItemID
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Media Player de Windows externa. selectedItemID
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698578"
---
# <a name="externalselecteditemid"></a>External. selectedItemID

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La propiedad **selectedItemID** recupera el identificador del elemento multimedia seleccionado actualmente en Windows Media Player.

## <a name="syntax"></a>Sintaxis

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Esta propiedad se usa en combinación con la propiedad [external. selectedItemType](external-selecteditemtype.md) . Por ejemplo, si **selectedItemType** es igual a CPTrackID, **SELECTEDITEMID** es el identificador de la pista seleccionada. Para obtener más información acerca de cómo Windows Media Player caracteriza las vistas del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).

Algunas vistas de Windows Media Player tienen un elemento multimedia determinado que está seleccionado. Por ejemplo, supongamos que la vista actual representa un álbum. Un álbum es un contenedor de pistas, por lo que **selectedItemType** es igual a CPTrackID y **SELECTEDITEMID** es el identificador de la pista seleccionada. Otras vistas no tienen un elemento multimedia seleccionado. Por ejemplo, si el usuario hace clic en el nodo raíz de la tienda en línea en el control de vista de árbol, Windows Media Player muestra una página de detección proporcionada por la tienda en línea. El reproductor no muestra ningún contenedor de elementos multimedia en la interfaz de usuario del reproductor. En ese caso, **selectedItemType** es igual a UnknownLocation y **selectedItemID** es igual a la cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para las tiendas en línea de tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. selectedItemType**](external-selecteditemtype.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 





