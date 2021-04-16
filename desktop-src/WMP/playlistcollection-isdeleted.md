---
title: PlaylistCollection. isDeleted (método)
description: El método isDeleted recupera un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- método isDeleted Windows Media Player
- método isDeleted Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718815"
---
# <a name="playlistcollectionisdeleted-method"></a>PlaylistCollection. isDeleted (método)

El método **IsDeleted** recupera un valor que indica si la lista de reproducción especificada está en la carpeta elementos eliminados.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de reproducción* \[ de\]
</dt> <dd>

Objeto de **lista de reproducción** que se va a buscar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

**Windows Media Player 10 Mobile**: este método siempre devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0, Windows Media Player versión 7,1 o Windows Media Player para Windows XP. Este método no es compatible con Windows Media Player 9 series o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 





