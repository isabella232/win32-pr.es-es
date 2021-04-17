---
description: La propiedad DatabaseTable de solo lectura del objeto error devuelve el nombre de la tabla en la base de datos que causó el error.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Propiedad error. DatabaseTable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653307"
---
# <a name="errordatabasetable-property"></a>Error. DatabaseTable (propiedad)

La propiedad **DatabaseTable** de solo lectura del objeto [**error**](error-object.md) devuelve el nombre de la tabla en la base de datos que causó el error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error mediante una llamada a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**Get \_ DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

