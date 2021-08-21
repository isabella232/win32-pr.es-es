---
title: Función SisCreateRestoreStructure (Sisbkup.h)
description: Crea una estructura de restauración de SIS basada en la información proporcionada.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Copia de seguridad de la función SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e2d8ae0033659392c43fc833c66a4ed9d9b7f75790bda2822f0bd6b5db7f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118174002"
---
# <a name="siscreaterestorestructure-function"></a>Función SisCreateRestoreStructure

La **función SisCreateRestoreStructure** crea una estructura de restauración de SIS basada en la información proporcionada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*volumeRoot* \[ En\]
</dt> <dd>

Nombre de archivo de la raíz del volumen, sin la barra diagonal inversa final, del volumen del que se va a realizar una copia de seguridad. Por ejemplo, especifique "C:" y no "C: \\ ". El volumen no puede ser el sistema ni el volumen de arranque.

</dd> <dt>

*sisRestoreStructure* \[ out\]
</dt> <dd>

Estructura de restauración de SIS devuelta. El autor de la llamada debe tratar esta estructura como opaca.

</dd> <dt>

*commonStoreRootPathname* \[ out\]
</dt> <dd>

Nombre completo de la ruta de acceso del almacén común del volumen especificado. Por ejemplo, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ out\]
</dt> <dd>

Número de archivos enumerados en *el parámetro commonStoreFilesToRestore.*

</dd> <dt>

*commonStoreFilesToRestore* \[ out\]
</dt> <dd>

Puntero a una matriz de nombres de archivo que especifica la lista de archivos internos que usa SIS para administrar el volumen especificado. Estos archivos deben restaurarse al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE si** se completa correctamente y **FALSE** en caso contrario. Llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre el motivo por el que se ha fallado la llamada.

## <a name="remarks"></a>Comentarios

Esta función establece el entorno de restauración en el volumen especificado de la manera en que [**SisCreateBackupStructure**](siscreatebackupstructure.md) establece el entorno de copia de seguridad en el volumen especificado.

Tenga en cuenta que esta función no identificará necesariamente el archivo de almacenamiento común o los archivos correspondientes a un conjunto de vínculos SIS en los medios de copia de seguridad si esos archivos comunes de almacenamiento siguen existiendo en el disco. El contenido del flujo de datos de un archivo de almacenamiento común nunca cambia una vez creado, por lo que si el archivo ya existe en el disco, no es necesario restaurarlo.

Los nombres de archivo de almacén común son únicos globalmente para garantizar la integridad de la operación de restauración, incluso si no se produce en el mismo volumen habilitado para SIS al que ha tenido acceso la operación de copia de seguridad.

Una vez completada la operación de restauración, desasigne la memoria usada por la matriz *commonStoreFilesToRestore* de cadenas mediante una llamada a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

