---
title: Función SisRestoredLink (Sisbkup.h)
description: Devuelve los nombres del archivo de almacenamiento común o los archivos a los que apunta el vínculo de SIS restaurado especificado.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Copia de seguridad de la función SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b330e4c6dfc5324f7041343865ea59885a0aedec01fa9c67014d3709a93834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021323"
---
# <a name="sisrestoredlink-function"></a>Función SisRestoredLink

La **función SisRestoredLink** devuelve los nombres del archivo de almacenamiento común o los archivos a los que apunta el vínculo DE SIS restaurado especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisRestoreStructure* \[ En\]
</dt> <dd>

Puntero a una estructura de restauración de SIS devuelta [**desde SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*restoredFileName* \[ En\]
</dt> <dd>

Nombre de archivo completo del archivo de vínculo SIS restaurado.

</dd> <dt>

*reparseData* \[ En\]
</dt> <dd>

Puntero al contenido del punto de rean aproximado de SIS. Este punto de análisis contiene datos que describen el vínculo de SIS restaurado. Para recuperar los datos de punto de análisis de un archivo, use el código de control [**FSCTL \_ GET \_ REPARSE \_ POINT.**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point)

</dd> <dt>

*reparseDataSize* \[ En\]
</dt> <dd>

Tamaño del contenido del punto de reanado de SIS al que apunta *reparseData*, en bytes.

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ out\]
</dt> <dd>

Número de archivos enumerados en *el parámetro commonStoreFilesToRestore.*

</dd> <dt>

*commonStoreFilesToRestore* \[ out\]
</dt> <dd>

Puntero a una matriz de nombres de archivo de almacenamiento común. Estos archivos deben restaurarse al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

Si el valor del parámetro *countOfCommonStoreFilesToRestore* no es 0, el valor del parámetro *commonStoreFilesToRestore* contendrá los nombres de los archivos de almacenamiento común que se restaurarán como resultado de restaurar el vínculo de SIS. Si el valor es 0, los archivos de common-store se han devuelto una vez o ya están presentes en el volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

Debe llamar a esta función para cada vínculo de SIS que se haya restaurado.

Esta función devolverá cada archivo de almacenamiento común como máximo una vez para cada operación de restauración; Cualquier intento de restaurar vínculos SIS adicionales que vean el mismo archivo de almacenamiento común no dará lugar a que se devuelva ese nombre de archivo de almacenamiento común.

Esta función no devolverá un archivo de almacenamiento común que no se haya devuelto también en una llamada a [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante la operación de copia de seguridad, suponiendo que los datos de análisis de SIS almacenados en el medio no se han dañado.

Al restaurar un vínculo de SIS, la operación de restauración debe crear solo el archivo disperso adecuado, inicializar los intervalos asignados y, a continuación, escribir los datos de análisis de SIS exactamente como se leyeron durante la operación de copia de seguridad. Es fundamental que la operación de restauración cree archivos dispersos con intervalos sin asignar en lugar de archivos dispersos (o archivos no dispersos) inicializados con ceros.

Tenga en cuenta que esta función no identificará necesariamente el archivo de almacenamiento común o los archivos correspondientes a un conjunto de vínculos SIS en los medios de copia de seguridad si esos archivos de almacenamiento común siguen existiendo en el disco. El contenido del flujo de datos de un archivo de almacenamiento común nunca cambia una vez creado, por lo que si el archivo ya existe en el disco, no es necesario restaurarlo.

Los nombres de archivo de almacén común son únicos globalmente para garantizar la integridad de la operación de restauración, incluso si no se produce en el mismo volumen habilitado para SIS al que ha tenido acceso la operación de copia de seguridad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

