---
description: Modifica la configuración de replicación de una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, modifica la configuración de replicación de la relación de replicación con la réplica extendida.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Método ModifyReplicationSettings de la clase Msvm_ReplicationService
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
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688062"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a>Método ModifyReplicationSettings de la \_ clase ReplicationService de MSVM

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

*ComputerSystem* \[ de\]
</dt> <dd>

Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe modificar la configuración de replicación.

</dd> <dt>

*ReplicationSettingData* \[ de\]
</dt> <dd>

Representación de cadena de la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define la nueva configuración de replicación.

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

**ModifyReplicationSettings** toma una instancia de [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) como entrada. La FRSD asociada a la máquina virtual como proveedor de host a host es la opción predeterminada. La FRSD de entrada se valida para la configuración válida de cada propiedad del proveedor predeterminado. En esta tabla se resumen las diferencias de validación con respecto al proveedor externo.



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
</dt> </dl>

 

