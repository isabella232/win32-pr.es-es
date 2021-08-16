---
title: Player.newMedia (método)
description: El método newMedia crea un nuevo objeto Media.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- Método newMedia Reproductor de Windows Media
- método newMedia Reproductor de Windows Media , Clase Player
- Clase player Reproductor de Windows Media , método newMedia
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e3ad30db7ec43bcc0ee6c1470dc608ccf1625390486d9fcd0fd4bf018affdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338111"
---
# <a name="playernewmedia-method"></a>Player.newMedia (método)

El **método newMedia** crea un nuevo **objeto Media.**

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección URL* \[ En\]
</dt> <dd>

**Cadena** que contiene la dirección URL del archivo multimedia digital con el que se crea **el objeto** Multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto Media.**

## <a name="remarks"></a>Comentarios

El *parámetro URL* no debe ser una cadena vacía o null.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





