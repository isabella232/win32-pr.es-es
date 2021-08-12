---
title: Evento Player.MediaError
description: El evento MediaError tiene lugar cuando el objeto Media tiene una condición de error.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Evento MediaError Reproductor de Windows Media
- Evento MediaError Reproductor de Windows Media , clase Player
- Clase de reproductor Reproductor de Windows Media evento , MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1eb94d245f0b0a91786b2b1a7b677429cc9040d8cbb1372164bf6e7ed209d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572845"
---
# <a name="playermediaerror-event"></a>Evento Player.MediaError

El **evento MediaError** tiene lugar cuando el **objeto Media** tiene una condición de error.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaObject* 
</dt> <dd>

**Objeto** multimedia que tiene una condición de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media, y se puede acceder o pasar a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





