---
title: Evento Player.MediaCollectionMediaRemoved
description: El evento MediaCollectionMediaRemoved tiene lugar cuando se quita un elemento multimedia de la biblioteca local. | Evento Player.MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Evento MediaCollectionMediaRemoved Reproductor de Windows Media
- Evento MediaCollectionMediaRemoved Reproductor de Windows Media clase , Player
- Clase player Reproductor de Windows Media evento , MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070971"
---
# <a name="playermediacollectionmediaremoved-event"></a>Evento Player.MediaCollectionMediaRemoved

El evento MediaCollectionMediaRemoved tiene lugar cuando se quita un elemento multimedia de la biblioteca local.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdispMedia* 
</dt> <dd>

**Objeto** multimedia que se quitó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

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

 

 





