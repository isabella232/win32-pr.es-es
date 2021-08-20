---
description: Modifica la configuración de replicación de una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, modifica la configuración de replicación de la relación de replicación con la réplica extendida.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Método ModifyReplicationSettings de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9e490ecc0eec1dcb4f6549281631f0b43e855ad4fb825b6c07517abe26a6c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149538"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a>Método ModifyReplicationSettings de la clase ReplicationService de Msvm \_

Modifica la configuración de replicación de una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, modifica la configuración de replicación de la relación de replicación con la réplica extendida.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe modificar la configuración de replicación.

</dd> <dt>

*ReplicationSettingData* \[ En\]
</dt> <dd>

Representación de cadena de la clase [**\_ ReplicationSettingData de Msvm**](msvm-replicationsettingdata.md) que define la nueva configuración de replicación.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentarios

**ModifyReplicationSettings toma** una instancia de [**\_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) de Msvm como entrada. El FRSD asociado para la máquina virtual como proveedor de host a host es la opción predeterminada. FrSD de entrada se valida para la configuración válida para cada propiedad para el proveedor predeterminado. En esta tabla se resumen las diferencias de validación con respecto al proveedor externo.



| Propiedad                                             | Proveedores externos                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | Igual que el proveedor predeterminado                           |
| AuthenticationType                                   | Omitido                                            |
| CertificateThumbPrint                                | Omitido                                            |
| RootCertificateThumbPrint (RO)                       | Omitido                                            |
| CompressionEnabled                                   | Igual que el proveedor predeterminado                           |
| BypassProxyServer                                    | Igual que el proveedor predeterminado                           |
| RecoveryConnectionPoint                              | Omitido \* (puede cambiar si el proveedor tiene requisitos) |
| RecoveryHostSystem (RO)                              | Omitido                                            |
| PrimaryConnectionPoint (RO)                          | Igual que el proveedor predeterminado                           |
| PrimaryHostSystem (RO)                               | Igual que el proveedor predeterminado                           |
| RecoveryServerPortNumber                             | Omitido \* (puede cambiar si el proveedor tiene requisitos) |
| ReplicateHostKvpItems                                | Omitido                                            |
| ApplicationConsistentSnapshotInterval                | Igual que el proveedor predeterminado                           |
| RecoveryHistory                                      | Igual que el proveedor predeterminado                           |
| Discos incluidos\[\]                                    | Igual que el proveedor predeterminado                           |
| AutoResynchronizeEnabled                             | Igual que el proveedor predeterminado                           |
| AutoResynchronizeIntervalStart                       | Igual que el proveedor predeterminado                           |
| AutoResynchronizeIntervalEnd                         | Igual que el proveedor predeterminado                           |
| EnableWriteOrderPreservationAcrossDisks (en desuso) | Igual que el proveedor predeterminado                           |
| ReplicationInterval                                  | Igual que el proveedor predeterminado                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> </dl>

 

