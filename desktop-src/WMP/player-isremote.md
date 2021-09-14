---
title: Player.isRemote
description: La propiedad isRemote recupera un valor que indica si el control Reproductor de Windows Media se ejecuta en modo remoto.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Player.isRemote Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c8d97ba212e032db16b43299d2a3a8a836f9b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172749"
---
# <a name="playerisremote"></a>Player.isRemote

La **propiedad isRemote** recupera un valor que indica si el control Reproductor de Windows Media se ejecuta en modo remoto.

## <a name="syntax"></a>Sintaxis

*player* . **isRemote**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de solo **lectura.**



| Value | Descripción                                   |
|-------|-----------------------------------------------|
| true  | El control Player se ejecuta en modo remoto. |
| false | El control Player se ejecuta en modo local.  |



 

## <a name="remarks"></a>Observaciones

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





