---
title: Player. openPlayer (método)
description: El método openPlayer abre Windows Media Player mediante la dirección URL especificada. | Player. openPlayer (método)
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- método openPlayer de Windows Media Player
- método openPlayer Windows Media Player, clase Player
- Clase Player Media Player Windows, método openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708766"
---
# <a name="playeropenplayer-method"></a>Player. openPlayer (método)

El método **openPlayer** abre Windows Media Player mediante la dirección URL especificada.

## <a name="syntax"></a>Sintaxis


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección URL* \[ de\]
</dt> <dd>

**Cadena** que representa la dirección URL del elemento multimedia que se va a reproducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método inicia Windows Media Player con la dirección URL especificada como elemento multimedia actual. Si el reproductor se cerró previamente en modo de máscara, se abrirá con la última máscara elegida por el usuario. De lo contrario, el reproductor se abre en modo completo.

Si se llama a este método desde un control PlayerActiveX de Windows Media incrustado en modo remoto, su comportamiento es idéntico al de *PlayerApplication*. método **switchToPlayerApplication** .

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





