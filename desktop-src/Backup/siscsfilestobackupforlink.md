---
title: Función SisCSFilesToBackupForLink (Sisbkup. h)
description: Devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo SIS especificado.
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
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656501"
---
# <a name="siscsfilestobackupforlink-function"></a>SisCSFilesToBackupForLink función)

La función **SisCSFilesToBackupForLink** devuelve información que describe los archivos de almacenamiento común a los que apunta el vínculo SIS especificado.

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

*sisBackupStructure* \[ de\]
</dt> <dd>

Puntero a la estructura de copia de seguridad de SIS devuelta desde [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> <dt>

*reparseData* \[ de\]
</dt> <dd>

Puntero al contenido del punto de análisis de SIS. Este punto de reanálisis contiene datos que describen un vínculo de SIS. Para recuperar los datos del punto de reanálisis para un archivo, use el código de control de [**\_ \_ \_ punto de reanálisis de FSCTL**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ de\]
</dt> <dd>

Tamaño del contenido del punto de análisis de SIS al que apunta *reparseData*, en bytes.

</dd> <dt>

*thisFileContext* \[ enuncia\]
</dt> <dd>

Puntero a una cadena de contexto proporcionada por la aplicación de copia de seguridad que llama a esta función. El contenido de esta cadena de contenido viene determinado por esta aplicación de copia de seguridad y la API de copia de seguridad de SIS no la interpreta. Este parámetro es opcional; Si no se usa, establezca el valor de este parámetro en **null**. En este caso, el valor de este parámetro no se procesará.

</dd> <dt>

*matchingFileContext* \[ enuncia\]
</dt> <dd>

Puntero de doble indirecto a la cadena de contexto del vínculo SIS identificada por la información pasada en los cuatro primeros parámetros de esta función. Este parámetro es opcional; Si no se proporciona una cadena de contexto como valor del parámetro *thisFileContext* , establezca el valor de este parámetro en **null**. En este caso, el valor de este parámetro no se procesará.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ enuncia\]
</dt> <dd>

Número de archivos enumerados en el parámetro *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de nombres de archivo. Se debe realizar una copia de seguridad de estos archivos al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

La aplicación de copia de seguridad debe llamar a esta función solo una vez para cada archivo de vínculo SIS del que se realiza la copia de seguridad.

La aplicación de copia de seguridad puede identificar un punto de análisis de SIS mediante su etiqueta, la etiqueta de reanálisis de e/s \_ \_ \_ . Esta etiqueta se define en Winnt. h.

Si este punto de análisis identificado por el valor del parámetro *reparseData* describe la primera instancia de un archivo del que se va a hacer una copia de seguridad, esta función devolverá **null** como el valor del parámetro *matchingFileContext* e inicializará el valor de la matriz *commonStoreFilesToBackUp* de cadenas con los nombres del archivo o archivos de almacenamiento común que se van a incluir en la copia de seguridad. De lo contrario, esta función establecerá el valor del parámetro *matchingFileContext* en la cadena de contexto correspondiente a la primera instancia del archivo especificado y establecerá el valor del parámetro *countOfCommonStoreFilesToBackUp* en 0. Si hay varios archivos de almacenamiento común correspondientes al vínculo especificado, el valor del parámetro *thisFileContext* será la cadena de contexto correspondiente al primer archivo de almacenamiento común devuelto en la matriz, es decir, commonStoreFilesToBackUp \[ 0 \] .

La versión actual de esta función devolverá como máximo un archivo de almacenamiento común, pero es posible que en versiones futuras un solo vínculo esté respaldado por varios archivos de almacenamiento común, por ejemplo, uno para cada flujo del archivo, por lo que la aplicación de copia de seguridad debe admitir varios archivos en cada llamada a esta función. En cualquier caso, cada archivo de almacenamiento común se devolverá una vez por cada paso de copia de seguridad.

La aplicación de copia de seguridad debe realizar una copia de seguridad o restaurar el archivo o los archivos de almacenamiento común identificados por el nombre de archivo o los nombres de archivo devueltos en el parámetro *commonStoreFilesToBackUp* . Independientemente de si hay un archivo de almacenamiento común correspondiente, la aplicación de copia de seguridad debe hacer una copia de seguridad del archivo de vínculo SIS tal como existe en el disco, por ejemplo, como un punto de reanálisis y un archivo disperso, y lo más probable es que no haya ningún rango rellenado. La aplicación de copia de seguridad puede hacer una copia de seguridad o restaurar el archivo o los archivos de almacenamiento común inmediatamente, posponer las copias de seguridad o combinarlos según sea necesario.

Una vez completada la operación de copia de seguridad, Desasigne la memoria usada por la matriz de cadenas *commonStoreFilesToBackUp* llamando a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

