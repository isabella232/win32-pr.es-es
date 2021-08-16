---
title: Función SisCSFilesToBackupForLink (Sisbkup.h)
description: Devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo de SIS especificado.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Copia de seguridad de la función SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e39d4370e68b67a5c05c1f259c52190be3b931dd02164da191bacf879cd6cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835563"
---
# <a name="siscsfilestobackupforlink-function"></a>Función SisCSFilesToBackupForLink

La **función SisCSFilesToBackupForLink** devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo de SIS especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisBackupStructure* \[ En\]
</dt> <dd>

Puntero a la estructura de copia de seguridad de SIS devuelta [**desde SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> <dt>

*reparseData* \[ En\]
</dt> <dd>

Puntero al contenido del punto de rean aproximado de SIS. Este punto de análisis contiene datos que describen un vínculo de SIS. Para recuperar los datos de punto de análisis de un archivo, use el código de control [**FSCTL \_ GET \_ REPARSE \_ POINT.**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point)

</dd> <dt>

*reparseDataSize* \[ En\]
</dt> <dd>

Tamaño del contenido del punto de rean aproximado de SIS al que *apunta reparseData*, en bytes.

</dd> <dt>

*thisFileContext* \[ out\]
</dt> <dd>

Puntero a una cadena de contexto proporcionada por la aplicación de copia de seguridad que llama a esta función. El contenido de esta cadena de contenido viene determinado por completo por esta aplicación de copia de seguridad y no lo interpreta la API de copia de seguridad de SIS. Este parámetro es opcional; Si no se usa, establezca el valor de este parámetro en **NULL.** El valor de este parámetro no se procesará en este caso.

</dd> <dt>

*matchingFileContext* \[ out\]
</dt> <dd>

Puntero doble indirecto a la cadena de contexto del vínculo SIS identificado por la información pasada en los cuatro primeros parámetros de esta función. Este parámetro es opcional; Si no se proporciona una cadena de contexto como valor del *parámetro thisFileContext,* establezca el valor de este parámetro en **NULL.** El valor de este parámetro no se procesará en este caso.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Número de archivos enumerados en *el parámetro commonStoreFilesToBackUp.*

</dd> <dt>

*commonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Puntero a una matriz de nombres de archivo. Se debe hacer una copia de seguridad de estos archivos al mismo tiempo y de la misma manera que los archivos de almacenamiento común [**solicitados por SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

La aplicación de copia de seguridad debe llamar a esta función solo una vez para cada archivo de vínculo DE SIS del que se va a realizar una copia de seguridad.

La aplicación de copia de seguridad puede identificar un punto de rean aproximado de SIS por su etiqueta, IO \_ REPARSE \_ TAG \_ SIS. Esta etiqueta se define en Winnt.h.

Si este punto de análisis identificado por el valor del parámetro *reparseData* describe la primera instancia de un archivo del que se va a realizar una copia de seguridad, esta función devolverá **NULL** como valor del parámetro *matchingFileContext* e inicializará el valor de la matriz *commonStoreFilesToBackUp* de cadenas con los nombres del archivo de almacén común o los archivos de los que se va a realizar una copia de seguridad. De lo contrario, esta función establecerá el valor del parámetro *matchingFileContext* en la cadena de contexto correspondiente a la primera instancia del archivo especificado y establecerá el valor del parámetro *countOfCommonStoreFilesToBackUp* en 0. Si hay varios archivos de almacenamiento común correspondientes al vínculo especificado, el valor del parámetro *thisFileContext* será la cadena de contexto correspondiente al primer archivo de almacén común devuelto en la matriz, commonStoreFilesToBackUp \[ \] 0.

La versión actual de esta función devolverá como máximo un archivo de almacén común, pero es posible que en versiones futuras un único vínculo pueda estar respaldo por varios archivos de almacenamiento común, por ejemplo, uno para cada secuencia del archivo, por lo que la aplicación de copia de seguridad debe admitir varios archivos en cada llamada a esta función. En cualquier caso, cada archivo de almacenamiento común se devolverá como máximo una vez para cada paso de copia de seguridad.

La aplicación de copia de seguridad debe realizar una copia de seguridad o restaurar el archivo de almacenamiento común o los archivos identificados por el nombre de archivo o los nombres de archivo devueltos en el *parámetro commonStoreFilesToBackUp.* Independientemente de si hay un archivo de almacenamiento común correspondiente, la aplicación de copia de seguridad debe hacer una copia de seguridad del archivo de vínculo de SIS tal como existe en el disco, por ejemplo, como un punto de análisis y un archivo disperso, y lo más probable es que no haya intervalos rellenados. La aplicación de copia de seguridad puede realizar una copia de seguridad o restaurar el archivo o los archivos de almacenamiento común inmediatamente, posponer la copia de seguridad o combinarlos según sea necesario.

Una vez completada la operación de copia de seguridad, desasigne la memoria utilizada por la matriz *commonStoreFilesToBackUp* de cadenas mediante una llamada a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

