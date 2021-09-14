---
title: Player.newMedia (método)
description: El método newMedia crea un nuevo objeto Media.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- Método newMedia Reproductor de Windows Media
- newMedia method Reproductor de Windows Media , Player (Clase)
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
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359275"
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

## <a name="remarks"></a>Observaciones

El *parámetro URL* no debe ser una cadena vacía o null.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





