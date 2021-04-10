---
title: Función SisRestoredCommonStoreFile (Sisbkup. h)
description: Informa a la arquitectura de SIS de que se ha escrito un archivo de almacenamiento común.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Copia de seguridad de la función SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996120"
---
# <a name="sisrestoredcommonstorefile-function"></a>SisRestoredCommonStoreFile función)

La función **SisRestoredCommonStoreFile** notifica a la arquitectura de SIS que se ha escrito un archivo de almacenamiento común.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sisRestoreStructure* \[ de\]
</dt> <dd>

Puntero a una estructura de restauración de SIS devuelta desde [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*commonStoreFileName* \[ de\]
</dt> <dd>

Nombre del archivo de almacenamiento común restaurado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se completa correctamente y **false** en caso contrario. Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Se debe llamar a esta función después de haber restaurado un archivo de almacenamiento común. Notifica a la arquitectura de SIS que se ha escrito un nuevo archivo de almacenamiento común, de modo que la arquitectura de SIS puede realizar tareas de mantenimiento internas como la inicialización de sus estructuras de datos internas o la corrección de los vínculos al archivo de almacenamiento común.

La operación de restauración solo debe restaurar los archivos de almacenamiento común que notifique [**SisRestoredLink**](sisrestoredlink.md), aunque haya archivos de almacenamiento común adicionales en el medio de copia de seguridad. La operación de restauración puede restaurar los vínculos de SIS y archivos de almacenamiento común en cualquier orden que elija. sin embargo, debe llamar a **SisRestoredLink** después de restaurar cualquier vínculo y debe llamar a esta función después de que se haya restaurado cualquier archivo de almacenamiento común. Dado que la operación de restauración no puede identificar los archivos de almacenamiento común que se restaurarán hasta que se notifiquen los nombres de archivo como resultado de la restauración de un vínculo, la operación de restauración siempre restaurará un archivo de almacenamiento común cuando se restaure al menos un vínculo que hace referencia a él. Sin embargo, puede restaurar vínculos de SIS adicionales que apunten a ese archivo de almacenamiento común.

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

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

