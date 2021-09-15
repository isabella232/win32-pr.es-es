---
title: Método PlaylistCollection.isDeleted
description: El método isDeleted recupera un valor que indica si la lista de reproducción especificada está en la carpeta de elementos eliminados.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- Método isDeleted Reproductor de Windows Media
- Método isDeleted Reproductor de Windows Media , clase PlaylistCollection
- Clase PlaylistCollection Reproductor de Windows Media método , isDeleted
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466141"
---
# <a name="playlistcollectionisdeleted-method"></a>Método PlaylistCollection.isDeleted

El **método isDeleted** recupera un valor que indica si la lista de reproducción especificada está en la carpeta de elementos eliminados.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de reproducción* \[ En\]
</dt> <dd>

Objeto **De lista** de reproducción que se va a buscar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

**Reproductor de Windows Media 10 Mobile:** este método siempre devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0, Reproductor de Windows Media versión 7.1 o Reproductor de Windows Media para Windows XP. Este método no se admite para Reproductor de Windows Media serie 9 o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 





