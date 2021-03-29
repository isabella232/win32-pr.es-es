---
title: Función SisFreeRestoreStructure (Sisbkup. h)
description: Libera la memoria asignada para la estructura de restauración de SIS especificada y realiza tareas que preparan el filtro SIS para configurar correctamente los vínculos creados durante la operación de restauración.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Copia de seguridad de la función SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492622"
---
# <a name="sisfreerestorestructure-function"></a>SisFreeRestoreStructure función)

La función **SisFreeRestoreStructure** libera la memoria asignada para la estructura de restauración de SIS especificada y realiza tareas que preparan el filtro SIS para configurar correctamente los vínculos creados durante la operación de restauración.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisRestoreStructure* \[ de\]
</dt> <dd>

Puntero a una estructura de restauración de SIS devuelta desde [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

El acceso a los vínculos de SIS antes de que se complete la llamada a esta función puede producir una comprobación de volumen o una lectura parcial del contenido del vínculo.

Tenga en cuenta que no es seguro asumir que esto solo desasigna memoria. Por ejemplo, esta función también puede realizar operaciones administrativas adicionales para la arquitectura de SIS. Por lo tanto, llame a esta función incluso si la operación de restauración se cerrará inmediatamente después.

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

