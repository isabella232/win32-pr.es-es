---
description: La propiedad DatabaseTable de solo lectura del objeto Error devuelve el nombre de la tabla de la base de datos que produjo el error.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Propiedad Error.DatabaseTable (Mergemod.h)
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
ms.openlocfilehash: b9e52523b37c90de4c4592fdeb059e6269f4e05e240242e69e14f0be6d4d53a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378176"
---
# <a name="errordatabasetable-property"></a>Error.DatabaseTable, propiedad

La propiedad **DatabaseTable** de solo lectura del [**objeto Error**](error-object.md) devuelve el nombre de la tabla de la base de datos que produjo el error.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a [**la propiedad Type**](error-type.md) del objeto [**Error.**](error-object.md)

### <a name="c"></a>C++

Vea get DatabaseTable function (Obtener [**\_ función DatabaseTable).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

