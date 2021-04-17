---
description: La propiedad errores de solo lectura del objeto Merge devuelve una colección de objetos error que es el conjunto actual de errores.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Propiedad Merge. errors (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670799"
---
# <a name="mergeerrors-property"></a>Merge. errors (propiedad)

La propiedad **errores** de solo lectura del objeto [**Merge**](merge-object.md) devuelve una colección de objetos [**error**](error-object.md) que es el conjunto actual de errores.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

La recuperación no es destructiva. Se pueden recuperar varias instancias de la colección de errores mediante una llamada repetida a este método.

### <a name="c"></a>C++

Vea la función [**Get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
