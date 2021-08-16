---
title: Función SisFreeRestoreStructure (Sisbkup.h)
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
ms.openlocfilehash: a787283f933ae4ccd2d8100c39e6118b40c545c030bb236a27a2f1598417742e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835553"
---
# <a name="sisfreerestorestructure-function"></a>Función SisFreeRestoreStructure

La función **SisFreeRestoreStructure** libera la memoria asignada para la estructura de restauración de SIS especificada y realiza tareas que preparan el filtro SIS para configurar correctamente los vínculos creados durante la operación de restauración.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisRestoreStructure* \[ En\]
</dt> <dd>

Puntero a una estructura de restauración de SIS devuelta [**desde SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

El acceso a los vínculos sis antes de que se complete la llamada a esta función puede dar lugar a una comprobación del volumen o a una lectura parcial del contenido del vínculo.

Tenga en cuenta que no es seguro suponer que esto solo desasigna memoria. Por ejemplo, esta función también puede realizar operaciones administrativas adicionales para la arquitectura de SIS. Por lo tanto, llame a esta función incluso si la operación de restauración se cerrará inmediatamente después.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

