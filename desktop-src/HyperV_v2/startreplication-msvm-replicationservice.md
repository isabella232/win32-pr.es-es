---
description: Inicia la replicación de una máquina virtual.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Método StartReplication de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f774192cf5c65f6fff0d9a1a17df51483984b49efd6be437f0348547eed5082c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050495"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>Método StartReplication de la clase ReplicationService de Msvm \_

Inicia la replicación de una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, inicia la replicación con una réplica extendida.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe iniciar la replicación.

</dd> <dt>

*InitialReplicationType* \[ En\]
</dt> <dd>

Tipo de transferencia que se va a usar para realizar la replicación inicial.

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Transferencia de red** (1)


</dt> <dd>

Transferencia de red.

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exportación** (2)


</dt> <dd>

Exportación.

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Transferencia de red seeded** (3)


</dt> <dd>

Transferencia de red de eded.

</dd> </dl> </dd> <dt>

*InitialReplicationExportLocation* \[ En\]
</dt> <dd>

Si *InitialReplicationType* es 2 (Export), este parámetro contiene la ruta de acceso completa del directorio al que se va a exportar la replicación inicial. Este parámetro no se usa para otros valores de *InitialReplicationType* y puede ser **Null.** Este directorio se puede reutilizar para exportar la replicación de varias máquinas virtuales. Este método coloca cada replicación de máquina virtual en un subdirectorio independiente bajo esta ruta de acceso.

</dd> <dt>

*StartTime* \[ En\]
</dt> <dd>

Hora de inicio programada para la replicación inicial a través de la conexión de red al servidor de recuperación. Este parámetro se omite cuando *InitialReplicationType* es 2 (Export). Si este parámetro es **Null**, la replicación inicial se inicia inmediatamente.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

