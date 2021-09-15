---
title: Método Player.openPlayer
description: El método openPlayer se Reproductor de Windows Media con la dirección URL especificada. | Método Player.openPlayer
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Método openPlayer Reproductor de Windows Media
- Método openPlayer Reproductor de Windows Media , Clase Player
- Clase player Reproductor de Windows Media , método openPlayer
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466013"
---
# <a name="playeropenplayer-method"></a>Método Player.openPlayer

El **método openPlayer** se Reproductor de Windows Media con la dirección URL especificada.

## <a name="syntax"></a>Sintaxis


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección URL* \[ En\]
</dt> <dd>

**Cadena** que representa la dirección URL del elemento multimedia que se reproducirá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método inicia Reproductor de Windows Media con la dirección URL especificada establecida como el elemento multimedia actual. Si el reproductor se cerró previamente en modo de máscara, se abrirá con la última máscara elegida por el usuario. De lo contrario, el reproductor se abre en modo completo.

Si se llama a este método desde un control Windows Media PlayerActiveX insertado en modo remoto, su comportamiento es idéntico al *de PlayerApplication*. **Método switchToPlayerApplication.**

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





