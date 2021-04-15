---
title: Player. newMedia (método)
description: El método newMedia crea un nuevo objeto multimedia.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- método newMedia de Windows Media Player
- método newMedia Windows Media Player, clase Player
- Clase Player Media Player Windows, método newMedia
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709167"
---
# <a name="playernewmedia-method"></a>Player. newMedia (método)

El método **newMedia** crea un nuevo objeto **multimedia** .

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección URL* \[ de\]
</dt> <dd>

**Cadena** que contiene la dirección URL del archivo multimedia digital con el que se va a crear el objeto **multimedia** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **multimedia** .

## <a name="remarks"></a>Observaciones

El parámetro de *dirección URL* no debe ser una cadena vacía ni null.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





