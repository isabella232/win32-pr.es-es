---
title: Función SisFreeBackupStructure (Sisbkup. h)
description: Libera la estructura de copia de seguridad de SIS especificada.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Copia de seguridad de la función SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801670"
---
# <a name="sisfreebackupstructure-function"></a>SisFreeBackupStructure función)

La función **SisFreeBackupStructure** libera la estructura de copia de seguridad de SIS especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisBackupStructure* \[ de\]
</dt> <dd>

Puntero a la estructura de copia de seguridad de SIS devuelta desde [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Se debe llamar a esta función después de que se complete la operación de copia de seguridad para el volumen identificado por el valor del parámetro *sisBackupStructure* .

Tenga en cuenta que no es seguro asumir que esto solo desasigna memoria. Por ejemplo, esta función también puede realizar operaciones administrativas adicionales para la arquitectura de SIS. Por lo tanto, llame a esta función incluso si la operación de copia de seguridad se cerrará inmediatamente después.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

