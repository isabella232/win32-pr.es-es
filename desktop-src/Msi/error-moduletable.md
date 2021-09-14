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
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158458"
---
# <a name="errormoduletable-property"></a>Propiedad Error.ModuleTable

La propiedad **ModuleTable de** solo lectura devuelve el nombre de la tabla del módulo que produjo el error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a la [**propiedad Type**](error-type.md) del [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Consulte get ModuleTable function (Obtener [**\_ función ModuleTable).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

