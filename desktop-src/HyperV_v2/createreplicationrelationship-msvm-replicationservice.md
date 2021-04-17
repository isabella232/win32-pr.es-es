---
description: Crea una nueva relación de replicación para una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, extiende la relación de replicación al proveedor especificado.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Método CreateReplicationRelationship de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667831"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>Método CreateReplicationRelationship de la \_ clase ReplicationService de MSVM

Crea una nueva relación de replicación para una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, extiende la relación de replicación al proveedor especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe habilitar la replicación.

</dd> <dt>

*ReplicationSettingData* \[ de\]
</dt> <dd>

Representación de cadena de una instancia de la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define la configuración de replicación de la nueva relación de replicación que se va a crear para la máquina virtual.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

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

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
</dt> </dl>

## <a name="remarks"></a>Observaciones

**CreateReplicationRelationship** toma una instancia de [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) como entrada. La FRSD asociada a la máquina virtual como proveedor de host a host es la opción predeterminada. La FRSD de entrada se valida para la configuración válida de cada propiedad del proveedor predeterminado. En esta tabla se resumen las diferencias de validación con respecto al proveedor externo.



| Propiedad                                             | Proveedores externos                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | Igual que el proveedor predeterminado                           |
| AuthenticationType                                   | Omitido                                            |
| CertificateThumbPrint                                | Omitido                                            |
| RootCertificateThumbPrint (RO)                       | Omitido                                            |
| CompressionEnabled                                   | Igual que el proveedor predeterminado                           |
| BypassProxyServer                                    | Igual que el proveedor predeterminado                           |
| RecoveryConnectionPoint                              | \*Se omite (puede cambiar si el proveedor tiene requisitos) |
| RecoveryHostSystem (RO)                              | Omitido                                            |
| PrimaryConnectionPoint (RO)                          | Igual que el proveedor predeterminado                           |
| PrimaryHostSystem (RO)                               | Igual que el proveedor predeterminado                           |
| RecoveryServerPortNumber                             | \*Se omite (puede cambiar si el proveedor tiene requisitos) |
| ReplicateHostKvpItems                                | Omitido                                            |
| ApplicationConsistentSnapshotInterval                | Igual que el proveedor predeterminado                           |
| RecoveryHistory                                      | Igual que el proveedor predeterminado                           |
| IncludedDisks\[\]                                    | Igual que el proveedor predeterminado                           |
| AutoResynchronizeEnabled                             | Igual que el proveedor predeterminado                           |
| AutoResynchronizeIntervalStart                       | Igual que el proveedor predeterminado                           |
| AutoResynchronizeIntervalEnd                         | Igual que el proveedor predeterminado                           |
| EnableWriteOrderPreservationAcrossDisks (desusado) | Igual que el proveedor predeterminado                           |
| ReplicationInterval                                  | Igual que el proveedor predeterminado                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

