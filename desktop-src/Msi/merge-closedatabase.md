---
description: El método CerrarBaseDeDatos del objeto Merge cierra la base de datos de Windows Installer abierta actualmente.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge. CerrarBaseDeDatos (método) (Mergemod. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678875"
---
# <a name="mergeclosedatabase-method"></a>Merge. CerrarBaseDeDatos (método)

El método **CerrarBaseDeDatos** del objeto [**Merge**](merge-object.md) cierra la base de datos de Windows Installer abierta actualmente.

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

**True** si se deben guardar los cambios; en caso contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Al cerrar una base de datos se borra toda la información de dependencias, pero no se afecta a los errores que no se hayan recuperado.

### <a name="c"></a>C++

Vea [**CerrarBaseDeDatos**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) (función).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
