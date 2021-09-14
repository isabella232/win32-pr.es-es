---
title: Evento Player.MediaError
description: El evento MediaError tiene lugar cuando el objeto Media tiene una condición de error.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Evento MediaError Reproductor de Windows Media
- Evento MediaError Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media , evento MediaError
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
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070969"
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

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





