---
title: Player.enabled
description: La propiedad enabled especifica o recupera un valor que indica si el control Reproductor de Windows Media está habilitado.
ms.assetid: 65fea4d2-3330-4cce-bdaf-fae00304271a
keywords:
- Player.enabled Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242408"
---
# <a name="playerenabled"></a>Player.enabled

La **propiedad enabled** especifica o recupera un valor que indica si el control Reproductor de Windows Media está habilitado.

## <a name="syntax"></a>Sintaxis

*player* . **habilitado**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Value | Descripción                                           |
|-------|-------------------------------------------------------|
| true  | Predeterminada. El control Reproductor de Windows Media está habilitado. |
| false | El control Reproductor de Windows Media está deshabilitado.         |



 

## <a name="remarks"></a>Observaciones

Si **enabled** es igual a false, durante la reproducción a pantalla Reproductor de Windows Media oculta los controles de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





