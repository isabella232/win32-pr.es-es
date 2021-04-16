---
title: Player. isRemote
description: La propiedad isRemote recupera un valor que indica si el control de Media Player de Windows se está ejecutando en modo remoto.
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- Media Player de Windows Player. isRemote
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649625"
---
# <a name="playerisremote"></a>Player. isRemote

La propiedad **isRemote** recupera un valor que indica si el control de Media Player de Windows se está ejecutando en modo remoto.

## <a name="syntax"></a>Sintaxis

*reproductor* . **isRemote**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de solo lectura.



| Value | Descripción                                   |
|-------|-----------------------------------------------|
| true  | El control Player se está ejecutando en modo remoto. |
| false | El control Player se ejecuta en modo local.  |



 

## <a name="remarks"></a>Observaciones

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





