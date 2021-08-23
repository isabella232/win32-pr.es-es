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
ms.openlocfilehash: 6afa0caf615563f4829f1a337f31521b1fb7dafd5ef6e2722f1d50c01dda1ba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616695"
---
# <a name="playerisremote"></a>Player.isRemote

La **propiedad isRemote** recupera un valor que indica si el control Reproductor de Windows Media se ejecuta en modo remoto.

## <a name="syntax"></a>Syntax

*player* . **isRemote**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de solo **lectura.**



| Value | Descripción                                   |
|-------|-----------------------------------------------|
| true  | El control Player se ejecuta en modo remoto. |
| false | El control Player se ejecuta en modo local.  |



 

## <a name="remarks"></a>Comentarios

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

 

 





