---
title: Función SisCreateBackupStructure (Sisbkup.h)
description: Crea una estructura de copia de seguridad de SIS basada en la información proporcionada.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Copia de seguridad de la función SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655dfe09285e72b0b961f81c26d6afcc4aae53101a3b12b1bf0a9f1823a45d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021373"
---
# <a name="siscreatebackupstructure-function"></a>Función SisCreateBackupStructure

La **función SisCreateBackupStructure** crea una estructura de copia de seguridad de SIS basada en la información proporcionada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*volumeRoot* \[ En\]
</dt> <dd>

Nombre de archivo de la raíz del volumen, sin la barra diagonal inversa final, del volumen del que se va a realizar una copia de seguridad. Por ejemplo, especifique "C:" y no "C: \\ ".

</dd> <dt>

*sisBackupStructure* \[ out\]
</dt> <dd>

Estructura de copia de seguridad de SIS devuelta.

</dd> <dt>

*commonStoreRootPathname* \[ out\]
</dt> <dd>

Nombre completo de la ruta de acceso del almacén común del volumen especificado. Por ejemplo, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Número de archivos enumerados en *el parámetro commonStoreFilesToBackUp.*

</dd> <dt>

*commonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Puntero a una matriz de nombres de archivo que especifica una lista de archivos internos utilizados por SIS para administrar el volumen especificado. Se debe hacer una copia de seguridad de estos archivos al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [ **SisCSFilesToBackupForLink.**](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

Esta función crea una estructura de copia de seguridad de SIS, que usa la API de copia de seguridad de SIS para crear y mantener una lista de los vínculos de archivo en el volumen y los archivos originales a los que apuntan los vínculos. Solo se debe llamar a esta función una vez para cada volumen habilitado para SIS del que se va a realizar una copia de seguridad. Todos los archivos del volumen especificado deben tratarse como archivos de almacenamiento común y realizar una copia de seguridad solo si SIS indica que deben hacerlo.

Los *parámetros countOfCommonStoreFilesToBackUp* y *commonStoreFilesToBackUp juntos* devuelven una lista de archivos de los que se debe realizar una copia de seguridad independientemente de los vínculos de los que se haga una copia de seguridad.

Si *countOfCommonStoreFilesToBackUp* es 0, *commonStoreFilesToBackUp* puede ser un **puntero NULL.** Se debe omitir el valor del parámetro *commonStoreFilesToBackUp.*

Una vez completada la operación de copia de seguridad, desasigne la memoria usada por la matriz *commonStoreFilesToBackUp* de cadenas llamando a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

