---
description: Solicita que el estado de replicación de la máquina virtual cambie al valor especificado y actúe sobre la relación de replicación principal de la máquina virtual.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Método RequestReplicationStateChange de la Msvm_ComputerSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 568c5016e77baceaadb8176b683d2fd9e1314ab06b907b6d1d3c4e3398a82c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130625"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>Método RequestReplicationStateChange de la clase \_ ComputerSystem de Msvm

Solicita que el estado de replicación de la máquina virtual cambie al valor especificado y actúe sobre la relación de replicación principal de la máquina virtual. Mientras el cambio de estado está en curso, la **propiedad ReplicationState** cambia al valor del *parámetro RequestedState.* Este método solo se admite para las instancias de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representan una máquina virtual.

> [!Note]  
> A partir Windows 8.1, se recomienda no usar **RequestReplicationStateChange** para solicitar el cambio del estado de replicación. En su lugar, [**use RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ En\]
</dt> <dd>

Nuevo estado de replicación. debe ser uno de los valores siguientes.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Listo para iniciar la replicación inicial** (1)


</dt> <dd>

Listo para iniciar la replicación inicial.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando a completar la replicación inicial** (2)


</dt> <dd>

Esperando a completar la replicación inicial.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicación** (3)


</dt> <dd>

Replicating.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completada** (4)


</dt> <dd>

Se ha completado la replicación sincronizada.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)


</dt> <dd>

Suspender replicación.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar resincronización** (9)


</dt> <dd>

Cancele la resincronización.

</dd> </dl> </dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia opcional a un objeto [**\_ ConcreteJob de Msvm**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método .

</dd> <dt>

*TimeoutPeriod* \[ En\]
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                                | Descripción                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Correcto<br/>                                                                                                          |
| <dl> <dt>**Parámetros de método activados: trabajo iniciado**</dt> <dt>4096</dt> </dl> | La transición es asincrónica.<br/>                                                                                  |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Acceso denegado**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**No compatible**</dt> <dt>con 32770</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**El estado es desconocido**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Tiempo de**</dt> <dt>espera 32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                      | No se admite el valor especificado en uno de los parámetros.<br/>                                                   |
| <dl> <dt>**El sistema está en uso**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>       | El valor especificado en el parámetro *RequestedState* no se admite en el estado o modo de replicación actual.<br/> |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> <dt>**El sistema no está disponible**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Memoria sin memoria**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Archivo no encontrado**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

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

[**Msvm \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

 




