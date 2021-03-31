---
title: Función SisFreeAllocatedMemory (Sisbkup. h)
description: Libera memoria asignada por las funciones de la API de SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Copia de seguridad de la función SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905110"
---
# <a name="sisfreeallocatedmemory-function"></a>SisFreeAllocatedMemory función)

La función **SisFreeAllocatedMemory** libera memoria asignada por las funciones de la API de SIS.

## <a name="syntax"></a>Sintaxis


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*allocatedSpace* \[ de\]
</dt> <dd>

Puntero a la memoria asignada por la API de SIS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una vez completada la llamada a esta función, es posible que el llamador ya no tenga acceso a la memoria liberada.

Esta llamada debe usarse para desasignar la memoria asignada para las cadenas de parámetros de *commonStoreRootPathname* devueltas desde [**SisCreateBackupStructure**](siscreatebackupstructure.md) y [**SisCreateRestoreStructure**](siscreaterestorestructure.md), y la matriz de cadenas que contienen los nombres de archivo de almacenamiento común devueltos por **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** y [**SisRestoredLink**](sisrestoredlink.md). En el último caso, la propia matriz también se debe liberar llamando a **SisFreeAllocatedMemory**.

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





