---
description: La propiedad Errors de solo lectura del objeto Merge devuelve una colección de objetos Error que es el conjunto actual de errores.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Propiedad Merge.Errors (Mergemod.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071904"
---
# <a name="mergeerrors-property"></a>Merge.Errors, propiedad

La propiedad **Errors** de solo lectura del [**objeto Merge**](merge-object.md) devuelve una colección de [**objetos Error**](error-object.md) que es el conjunto actual de errores.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

La recuperación no es destructiva. Se pueden recuperar varias instancias de la colección de errores llamando repetidamente a este método.

### <a name="c"></a>C++

Consulte [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
