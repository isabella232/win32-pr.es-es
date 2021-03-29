---
title: Función SisCreateRestoreStructure (Sisbkup. h)
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
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905111"
---
# <a name="siscreaterestorestructure-function"></a>SisCreateRestoreStructure función)

La función **SisCreateRestoreStructure** crea una estructura de restauración de SIS basada en la información proporcionada.

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

*volumeRoot* \[ de\]
</dt> <dd>

Nombre de archivo de la raíz del volumen, sin la barra diagonal inversa final, del volumen del que se va a realizar la copia de seguridad. Por ejemplo, especifique "C:" y no "C: \\ ". El volumen no puede ser el volumen de sistema o de arranque.

</dd> <dt>

*sisRestoreStructure* \[ enuncia\]
</dt> <dd>

Se devolvió la estructura de restauración de SIS. El llamador debe tratar esta estructura como opaca.

</dd> <dt>

*commonStoreRootPathname* \[ enuncia\]
</dt> <dd>

Nombre completo de la ruta de acceso del almacén común del volumen especificado. Por ejemplo, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ enuncia\]
</dt> <dd>

Número de archivos enumerados en el parámetro *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de nombres de archivo que especifica la lista de archivos internos que SIS usa para administrar el volumen especificado. Estos archivos deben restaurarse al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Esta función establece el entorno de restauración en el volumen especificado en la forma en que [**SisCreateBackupStructure**](siscreatebackupstructure.md) establece el entorno de copia de seguridad en el volumen especificado.

Tenga en cuenta que esta función no identifica necesariamente el archivo o los archivos de almacenamiento común correspondientes a un conjunto de vínculos de SIS en el medio de copia de seguridad si esos archivos de almacenamiento comunes todavía existen en el disco. El contenido de la secuencia de datos de un archivo de almacenamiento común nunca cambia una vez que se crea, por lo que si el archivo ya existe en el disco, no es necesario restaurarlo.

Los nombres de archivo de almacenamiento común son únicos globalmente para garantizar la integridad de la operación de restauración, incluso si no se produce en el mismo volumen habilitado para SIS al que ha tenido acceso la operación de copia de seguridad.

Una vez completada la operación de restauración, cancele la asignación de la memoria usada por la matriz de cadenas *commonStoreFilesToRestore* llamando a [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

