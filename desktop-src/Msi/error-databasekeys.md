---
description: La propiedad DatabaseKeys de solo lectura del objeto Error devuelve una colección de cadenas que contiene las claves principales de la fila de base de datos que produce el error. Hay una clave por entrada en la colección.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Propiedad Error.DatabaseKeys (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158474"
---
# <a name="errordatabasekeys-property"></a>Error.DatabaseKeys, propiedad

La propiedad **DatabaseKeys de** solo lectura del [**objeto Error**](error-object.md) devuelve una colección de cadenas que contiene las claves principales de la fila de base de datos que produce el error. Hay una clave por entrada en la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

El cliente es responsable de liberar la colección de cadenas cuando ya no es necesaria.

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a la [**propiedad Type**](error-type.md) del [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Vea get DatabaseKeys function ( obtener [**\_ función DatabaseKeys).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

