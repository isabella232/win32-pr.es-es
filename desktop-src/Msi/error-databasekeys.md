---
description: La propiedad DatabaseKeys de solo lectura del objeto error devuelve una colección de cadenas que contiene las claves principales de la fila de la base de datos que produce el error. Hay una clave por cada entrada de la colección.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Propiedad error. DatabaseKeys (Mergemod. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653308"
---
# <a name="errordatabasekeys-property"></a>Error. DatabaseKeys (propiedad)

La propiedad **DatabaseKeys** de solo lectura del objeto [**error**](error-object.md) devuelve una colección de cadenas que contiene las claves principales de la fila de la base de datos que produce el error. Hay una clave por cada entrada de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

El cliente es responsable de liberar la colección de cadenas cuando ya no se necesita.

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**Get \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

