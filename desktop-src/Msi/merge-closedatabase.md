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
ms.openlocfilehash: 3f3b250cbaebd565f14ef7f10cd8180e497f20347d00a7e96a74298d3e5dc770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013033"
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

## <a name="remarks"></a>Comentarios

El cierre de una base de datos borra toda la información de dependencia, pero no afecta a los errores que no se han recuperado.

### <a name="c"></a>C++

Vea [**CloseDatabase function (Función CloseDatabase).**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
