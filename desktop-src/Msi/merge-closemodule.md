---
description: El método CloseModule del objeto Merge cierra el módulo de combinación de Windows Installer abierto actualmente.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Método Merge. CloseModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670309"
---
# <a name="mergeclosemodule-method"></a>Merge. CloseModule (método)

El método **CloseModule** del objeto [**Merge**](merge-object.md) cierra el módulo de combinación de Windows Installer abierto actualmente.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El cierre de un módulo de combinación no afectará a los errores que no se hayan recuperado.

### <a name="c"></a>C++

Consulte función [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
