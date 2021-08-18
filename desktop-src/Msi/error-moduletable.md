---
description: La propiedad ModuleTable de solo lectura devuelve el nombre de la tabla del módulo que produjo el error.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Propiedad Error.ModuleTable (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 47cd9bab5c12230a048da04e60169e1ad21195df2304642f6b656983539f3b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947077"
---
# <a name="errormoduletable-property"></a>Error.ModuleTable, propiedad

La propiedad **ModuleTable de** solo lectura devuelve el nombre de la tabla del módulo que produjo el error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a la [**propiedad Type**](error-type.md) del [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Consulte get ModuleTable function (Obtener [**\_ función ModuleTable).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

