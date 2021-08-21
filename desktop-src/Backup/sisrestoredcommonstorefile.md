---
title: Función SisRestoredCommonStoreFile (Sisbkup.h)
description: Informa a la arquitectura de SIS de que se ha escrito un archivo de almacén común.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Copia de seguridad de la función SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 389d40b76614fe64038133c8cc0623706d4f2be82e68b3e096b59b3023f08bf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529495"
---
# <a name="sisrestoredcommonstorefile-function"></a>Función SisRestoredCommonStoreFile

La **función SisRestoredCommonStoreFile** informa a la arquitectura de SIS de que se ha escrito un archivo de almacén común.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisRestoreStructure* \[ En\]
</dt> <dd>

Puntero a una estructura de restauración de SIS devuelta [**desde SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*commonStoreFileName* \[ En\]
</dt> <dd>

Nombre del archivo de almacenamiento común restaurado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

Se debe llamar a esta función después de restaurar un archivo de almacenamiento común. Notifica a la arquitectura de SIS que se ha escrito un nuevo archivo de almacén común, de modo que la arquitectura de SIS puede realizar tareas de mantenimiento interno, como inicializar sus estructuras de datos internas o corregir los vínculos al archivo de almacenamiento común.

La operación de restauración solo debe restaurar archivos de almacenamiento común notificados por [**SisRestoredLink,**](sisrestoredlink.md)incluso si hay archivos de almacenamiento común adicionales en los medios de copia de seguridad. La operación de restauración puede restaurar los vínculos de SIS y los archivos de almacenamiento común en el orden que elija. sin embargo, debe llamar a **SisRestoredLink** después de restaurar cualquier vínculo y debe llamar a esta función después de restaurar cualquier archivo de almacenamiento común. Dado que la operación de restauración no puede identificar qué archivos de almacenamiento común se restaurarán hasta que se le notifican los nombres de archivo como resultado de restaurar un vínculo, la operación de restauración siempre restaurará un archivo de almacén común después de que se restaure al menos un vínculo que haga referencia a él. Sin embargo, puede restaurar vínculos SIS adicionales que apunten a ese archivo de almacenamiento común.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

