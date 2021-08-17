---
title: Evento Player.MediaCollectionMediaAdded
description: El evento MediaCollectionMediaAdded tiene lugar cuando se agrega un elemento multimedia a la biblioteca local. | Evento Player.MediaCollectionMediaAdded
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- MediaCollectionMediaAdded event Reproductor de Windows Media
- MediaCollectionMediaAdded event Reproductor de Windows Media , Player (Clase)
- Clase player Reproductor de Windows Media evento , MediaCollectionMediaAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fef517c3d22335df6dd5dc5f62adcfd8f35dc3f2f91b08f8041c05770311993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747354"
---
# <a name="playermediacollectionmediaadded-event"></a>Evento Player.MediaCollectionMediaAdded

El evento MediaCollectionMediaAdded tiene lugar cuando se agrega un elemento multimedia a la biblioteca local.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdispMedia* 
</dt> <dd>

**Objeto** multimedia que se agregó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este evento solo se produce para la biblioteca local.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11.<br/>                                                |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





