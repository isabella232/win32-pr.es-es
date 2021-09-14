---
description: El método CloseModule del objeto Merge cierra el módulo de combinación Windows installer actualmente abierto.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Método Merge.CloseModule (Mergemod.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074399"
---
# <a name="mergeclosemodule-method"></a>Método Merge.CloseModule

El **método CloseModule** del [**objeto Merge**](merge-object.md) cierra el módulo de combinación Windows Installer actualmente abierto.

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

Vea [**CloseModule function (Función CloseModule).**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
