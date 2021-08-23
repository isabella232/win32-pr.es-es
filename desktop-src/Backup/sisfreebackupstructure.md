---
title: Función SisFreeBackupStructure (Sisbkup.h)
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
ms.openlocfilehash: 1e506881110ad9fbb60ea12479c64f8ef8024f8e0f9ddee753813795d31f3dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021363"
---
# <a name="sisfreebackupstructure-function"></a>Función SisFreeBackupStructure

La **función SisFreeBackupStructure** libera la estructura de copia de seguridad de SIS especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisBackupStructure* \[ En\]
</dt> <dd>

Puntero a la estructura de copia de seguridad de SIS devuelta [**desde SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

Se debe llamar a esta función una vez completada la operación de copia de seguridad para el volumen identificado por el valor *del parámetro sisBackupStructure.*

Tenga en cuenta que no es seguro suponer que esto solo desasigne la memoria. Por ejemplo, esta función también puede realizar operaciones administrativas adicionales para la arquitectura de SIS. Por lo tanto, llame a esta función incluso si la operación de copia de seguridad se cerrará inmediatamente después.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

