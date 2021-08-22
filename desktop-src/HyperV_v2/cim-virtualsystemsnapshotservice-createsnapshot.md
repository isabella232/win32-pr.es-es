---
description: Crea una instantánea de un sistema virtual.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Método CreateSnapshot de la CIM_VirtualSystemSnapshotService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ee1a2e66745ceac50cc00ba6e625a171f18c7d2b54d4e51af2c86f6711675ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532755"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Método CreateSnapshot de la clase \_ CIM VirtualSystemSnapshotService

Crea una instantánea de un sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSystem* \[ En\]
</dt> <dd>

Una [**referencia \_ cim computersystem**](cim-computersystem.md) al sistema virtual afectado.

</dd> <dt>

*SnapshotSettings* \[ En\]
</dt> <dd>

Configuración de parámetros.

</dd> <dt>

*SnapshotType* \[ En\]
</dt> <dd>

Tipo de instantánea solicitada:

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantánea completa** (2)


</dt> <dd>

Instantánea completa del sistema virtual.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Instantánea de disco** (3)


</dt> <dd>

Instantánea de discos del sistema virtual.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del** proveedor (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[ in, out\]
</dt> <dd>

Una [**referencia CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) a la instantánea del sistema virtual resultante.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver un trabajo. En este caso, la instancia de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa la nueva instantánea del sistema virtual se presenta a través de la asociación [**\_ AffectedJobElement**](cim-affectedjobelement.md) de CIM con el valor de la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **CIM \_ VirtualSystemSettingData** que representa la instantánea del sistema virtual y el valor de **ElementEffects** establecido en 5 (Crear).

> [!Note]  
> Este parámetro era de lectura y escritura en Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.

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

**Parámetros de método activados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ VirtualSystemSnapshotService**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




