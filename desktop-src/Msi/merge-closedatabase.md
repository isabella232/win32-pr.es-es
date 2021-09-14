---
description: El método CloseDatabase del objeto Merge cierra la base de datos del instalador Windows actualmente abierta.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Método Merge.CloseDatabase (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074400"
---
# <a name="mergeclosedatabase-method"></a>Método Merge.CloseDatabase

El **método CloseDatabase** del objeto [**Merge**](merge-object.md) cierra la base de datos del instalador Windows actualmente abierta.

## <a name="syntax"></a>Sintaxis


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCommit* 
</dt> <dd>

**TRUE si** se deben guardar los cambios; en caso contrario, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El cierre de una base de datos borra toda la información de dependencia, pero no afecta a los errores que no se han recuperado.

### <a name="c"></a>C++

Vea [**CloseDatabase function (Función CloseDatabase).**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
