---
description: La propiedad ModuleTable de solo lectura devuelve el nombre de la tabla en el módulo que causó el error.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Propiedad error. ModuleTable (Mergemod. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690193"
---
# <a name="errormoduletable-property"></a>Error. ModuleTable (propiedad)

La propiedad **ModuleTable** de solo lectura devuelve el nombre de la tabla en el módulo que causó el error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**Get \_ ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

