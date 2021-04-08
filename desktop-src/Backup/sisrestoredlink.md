---
title: Función SisRestoredLink (Sisbkup. h)
description: Devuelve los nombres de los archivos de almacenamiento común a los que apunta el vínculo SIS restaurado especificado.
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
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996119"
---
# <a name="sisrestoredlink-function"></a>SisRestoredLink función)

La función **SisRestoredLink** devuelve los nombres de los archivos de almacenamiento común a los que apunta el vínculo SIS restaurado especificado.

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

*sisRestoreStructure* \[ de\]
</dt> <dd>

Puntero a una estructura de restauración de SIS devuelta desde [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*restoredFileName* \[ de\]
</dt> <dd>

Nombre de archivo completo del archivo de vínculo SIS restaurado.

</dd> <dt>

*reparseData* \[ de\]
</dt> <dd>

Puntero al contenido del punto de análisis de SIS. Este punto de reanálisis contiene datos que describen el vínculo SIS restaurado. Para recuperar los datos del punto de reanálisis para un archivo, use el código de control de [**\_ \_ \_ punto de reanálisis de FSCTL**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ de\]
</dt> <dd>

Tamaño del contenido del punto de análisis de SIS al que apunta *reparseData*, en bytes.

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ enuncia\]
</dt> <dd>

Número de archivos enumerados en el parámetro *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de nombres de archivo de almacenamiento común. Estos archivos deben restaurarse al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

Si el valor del parámetro *countOfCommonStoreFilesToRestore* no es 0, el valor del parámetro *commonStoreFilesToRestore* contendrá los nombres de los archivos de almacenamiento común que se restaurarán como resultado de la restauración del vínculo SIS. Si el valor es 0, se devuelven los archivos de almacenamiento común una vez o ya están presentes en el volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Debe llamar a esta función para cada vínculo SIS que se haya restaurado.

Esta función devolverá cada archivo de almacenamiento común como máximo una vez por cada operación de restauración. cualquier intento de restaurar vínculos de SIS adicionales que ven el mismo archivo de almacenamiento común no dará como resultado que se devuelva el nombre de archivo de almacenamiento común.

Esta función no devolverá un archivo de almacenamiento común que no se devolvió también en una llamada a [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante la operación de copia de seguridad, suponiendo que los datos de análisis de SIS almacenados en el medio no se han dañado.

Al restaurar un vínculo de SIS, la operación de restauración solo debe crear el archivo disperso adecuado, inicializar los intervalos asignados y, a continuación, escribir los datos de reanálisis de SIS exactamente como se leyeron durante la operación de copia de seguridad. Es fundamental que la operación de restauración cree archivos dispersos con intervalos sin asignar en lugar de archivos dispersos (o archivos no dispersos) inicializados con ceros.

Tenga en cuenta que esta función no identificará necesariamente el archivo o los archivos de almacenamiento común correspondientes a un conjunto de vínculos de SIS en el medio de copia de seguridad si todavía existen en el disco. El contenido de un flujo de datos de un archivo de almacenamiento común nunca cambia una vez que se crea, por lo que si el archivo ya existe en el disco, no es necesario restaurarlo.

Los nombres de archivo de almacenamiento común son únicos globalmente para garantizar la integridad de la operación de restauración, incluso si no se produce en el mismo volumen habilitado para SIS al que ha tenido acceso la operación de copia de seguridad.

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
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

