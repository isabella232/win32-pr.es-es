---
description: La propiedad ModuleKeys de solo lectura del objeto Error devuelve un puntero a una colección de cadenas que contiene las claves principales de la fila del módulo que produce el error, una clave por cada entrada de la colección.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Propiedad Error.ModuleKeys (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d33b546bea909700cc1a737043947d980006764daa86771820740570adf7f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044605"
---
# <a name="errormodulekeys-property"></a>Propiedad Error.ModuleKeys

La propiedad **ModuleKeys** de solo lectura del objeto [**Error**](error-object.md) devuelve un puntero a una colección de cadenas que contiene las claves principales de la fila del módulo que produce el error, una clave por cada entrada de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

El cliente es responsable de liberar la colección de cadenas cuando ya no es necesaria.

La colección está vacía si los valores no se aplican al tipo del error. Puede determinar el tipo de error llamando a la [**propiedad Type**](error-type.md) del [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Consulte get ModuleKeys function (Obtener [**\_ función ModuleKeys).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

