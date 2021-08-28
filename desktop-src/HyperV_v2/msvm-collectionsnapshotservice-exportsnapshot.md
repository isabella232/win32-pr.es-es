---
description: Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo. La colección de instantáneas, sus opciones de configuración asociadas y sus valores de recursos asociados se conservarán en el archivo resultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Método ExportSnapshot de la Msvm_CollectionSnapshotService clase
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
ms.openlocfilehash: ec61899e92da562250bf392077468adef14a35eda72d89d28ad9b3ddc3da2f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426845"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ExportSnapshot de la clase \_ CollectionSnapshotService de Msvm

Exporta una colección de instantáneas de sistemas de equipos virtuales a un archivo. La colección de instantáneas, sus opciones de configuración asociadas y sus valores de recursos asociados se conservarán en el archivo resultante.

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

*SnapshotCollection* \[ En\]
</dt> <dd>

Referencia a una colección [**CIM \_ que**](cim-collection.md) representa la colección de instantáneas que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ En\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar la colección del sistema virtual. Si la propiedad **CreateVmExportSubdirectory** del parámetro *ExportSettingData* está establecida en **True,** este directorio se puede reutilizar para exportar varias colecciones de sistemas virtuales y este método coloca cada definición de colección del sistema virtual en un subdirectorio independiente bajo esta ruta de acceso.

</dd> <dt>

*ExportSettingData* \[ En\]
</dt> <dd>

Instancia de [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) que representa la configuración de la operación de exportación.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta sincrónicamente, devuelve 0 si se ejecuta correctamente. Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida Job se puede usar para realizar un seguimiento del progreso de la operación asincrónica. Cualquier otro valor devuelto indica un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Colección de \_ MsvmSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




