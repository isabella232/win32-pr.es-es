---
title: Función SisFreeAllocatedMemory (Sisbkup.h)
description: Libera la memoria asignada por las funciones de LA API de SIS.
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
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702185"
---
# <a name="sisfreeallocatedmemory-function"></a>Función SisFreeAllocatedMemory

La **función SisFreeAllocatedMemory** libera la memoria asignada por las funciones de LA API de SIS.

## <a name="syntax"></a>Sintaxis


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*allocatedSpace* \[ En\]
</dt> <dd>

Puntero a la memoria asignada por la API de SIS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una vez completada la llamada a esta función, es posible que el autor de la llamada ya no tenga acceso a la memoria liberada.

Esta llamada debe usarse para desasignar la memoria asignada para las cadenas de parámetro *commonStoreRootPathname* devueltas desde [**SisCreateBackupStructure**](siscreatebackupstructure.md) y [**SisCreateRestoreStructure**](siscreaterestorestructure.md), y la matriz de cadenas que contienen nombres de archivo de almacén común devueltos desde **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink,**](siscsfilestobackupforlink.md) **SisCreateRestoreStructure** y [**SisRestoredLink.**](sisrestoredlink.md) En el último caso, la propia matriz también debe liberarse llamando a **SisFreeAllocatedMemory**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
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

 

 





