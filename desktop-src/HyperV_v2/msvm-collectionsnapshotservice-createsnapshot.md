---
description: Crea una instantánea de una colección de sistema virtual.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Método CreateSnapshot de la Msvm_CollectionSnapshotService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 251213d0ff7a98d922a4dec761252479f911e66e2304596a97858fe0b7dc5fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426915"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método CreateSnapshot de la clase \_ CollectionSnapshotService de Msvm

Crea una instantánea de una colección de sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Colección* \[ En\]
</dt> <dd>

Referencia a una [**colección \_ CIMOfMSE**](cim-collectionofmses.md) que describe la colección del sistema virtual afectada.

</dd> <dt>

*SnapshotSettings* \[ En\]
</dt> <dd>

Contiene la configuración de parámetros.

</dd> <dt>

*SnapshotType* \[ En\]
</dt> <dd>

Tipo de instantánea solicitada:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Instantánea estándar** (1)


</dt> <dd>

Instantánea estándar del sistema virtual.

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Instantánea de recuperación** (2)


</dt> <dd>

Instantánea para escenarios de recuperación, incluida la replicación de conmutación por error y la copia de seguridad.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del** proveedor (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshotCollection* \[ in, out\]
</dt> <dd>

Si se ejecuta correctamente, devuelve una referencia de [**\_ colección CIM**](cim-collection.md) que contiene la instantánea del sistema virtual.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta a una instancia de [**\_ CIM ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 (completado) o 4096 (trabajo iniciado); de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Tipo no** válido (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

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

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




