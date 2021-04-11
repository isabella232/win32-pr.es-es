---
description: Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo. La colección de instantáneas, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Método ExportSnapshot de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276183"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ExportSnapshot de la \_ clase CollectionSnapshotService de MSVM

Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo. La colección de instantáneas, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SnapshotCollection* \[ de\]
</dt> <dd>

Referencia a una [**\_ colección CIM**](cim-collection.md) que representa la colección de instantáneas que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ de\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar la colección de sistemas virtuales. Si la propiedad **CreateVmExportSubdirectory** del parámetro *ExportSettingData* se establece en **true** , este directorio se puede reutilizar para exportar varias colecciones de sistemas virtuales y este método coloca cada definición de colección de sistemas virtuales en un subdirectorio independiente en esta ruta de acceso.

</dd> <dt>

*ExportSettingData* \[ de\]
</dt> <dd>

Instancia de [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) que representa la configuración de la operación de exportación.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente. Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del trabajo se puede usar para realizar el seguimiento del progreso de la operación asincrónica. Cualquier otro valor devuelto indica un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




