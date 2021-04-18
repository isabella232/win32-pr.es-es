---
title: Reproductor. habilitado
description: La propiedad Enabled especifica o recupera un valor que indica si el control Media Player de Windows está habilitado.
ms.assetid: 65fea4d2-3330-4cce-bdaf-fae00304271a
keywords:
- Player. Enabled Windows Media Player
topic_type:
- apiref
api_name:
- Player.enabled
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d002d1f1420d17d4b1a0b7dd3028b0f2dc0f6f7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698673"
---
# <a name="playerenabled"></a>Reproductor. habilitado

La propiedad **Enabled** especifica o recupera un valor que indica si el control Media Player de Windows está habilitado.

## <a name="syntax"></a>Sintaxis

*reproductor* . **habilitado**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de lectura/escritura.



| Value | Descripción                                           |
|-------|-------------------------------------------------------|
| true  | Predeterminada. El control Media Player de Windows está habilitado. |
| false | El control Media Player de Windows está deshabilitado.         |



 

## <a name="remarks"></a>Observaciones

Si **habilitada** es igual a false, durante las ventanas de reproducción de pantalla completa Media Player oculta los controles de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





