---
title: Función SisCreateBackupStructure (Sisbkup. h)
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
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489820"
---
# <a name="siscreatebackupstructure-function"></a>SisCreateBackupStructure función)

La función **SisCreateBackupStructure** crea una estructura de copia de seguridad de SIS basada en la información proporcionada.

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

*volumeRoot* \[ de\]
</dt> <dd>

Nombre de archivo de la raíz del volumen, sin la barra diagonal inversa final, del volumen del que se va a realizar la copia de seguridad. Por ejemplo, especifique "C:" y no "C: \\ ".

</dd> <dt>

*sisBackupStructure* \[ enuncia\]
</dt> <dd>

Estructura de copia de seguridad de SIS devuelta.

</dd> <dt>

*commonStoreRootPathname* \[ enuncia\]
</dt> <dd>

Nombre completo de la ruta de acceso del almacén común del volumen especificado. Por ejemplo, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ enuncia\]
</dt> <dd>

Número de archivos enumerados en el parámetro *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de nombres de archivo que especifica una lista de archivos internos utilizados por SIS para administrar el volumen especificado. Se debe realizar una copia de seguridad de estos archivos al mismo tiempo y de la misma manera que los archivos de almacenamiento común solicitados por [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Esta función crea una estructura de copia de seguridad de SIS, que usa la API de copia de seguridad de SIS para crear y mantener una lista de los vínculos de archivo en el volumen y los archivos originales a los que apuntan los vínculos. Se debe llamar a esta función solo una vez para cada volumen habilitado para SIS en el que se realiza la copia de seguridad. Todos los archivos del volumen especificado deben tratarse como archivos de almacenamiento común y copia de seguridad solo si SIS indica que deben hacerlo.

Los parámetros *countOfCommonStoreFilesToBackUp* y *commonStoreFilesToBackUp* devuelven conjuntamente una lista de archivos de los que se debe hacer una copia de seguridad, independientemente de los vínculos de los que se haya realizado una copia de seguridad.

Si *countOfCommonStoreFilesToBackUp* es 0, *commonStoreFilesToBackUp* puede ser un puntero **nulo** . Se debe omitir el valor del parámetro *commonStoreFilesToBackUp* .

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

