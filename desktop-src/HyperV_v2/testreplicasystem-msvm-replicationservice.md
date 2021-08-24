---
description: Crea una nueva réplica de una máquina virtual con la instantánea especificada con fines de prueba.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Método TestReplicaSystem de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d23a97e43dce07d8c0ac0b06f2b488f5966ee63d82f5d92eacac017dc8e05de1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870255"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a>Método TestReplicaSystem de la clase ReplicationService de Msvm \_

Crea una nueva réplica de una máquina virtual con la instantánea especificada con fines de prueba.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de Cim ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe probar la replicación.

</dd> <dt>

*SnapshotSettingData* \[ En\]
</dt> <dd>

Referencia a una instancia [**de CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea usada para crear el sistema de conmutación por error de prueba. Si este parámetro es **Null,** la conmutación por error se realizará fuera del punto más reciente en el tiempo.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Si una máquina virtual se define correctamente, recibe una referencia a una instancia de la clase [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual de prueba recién definida. Cuando este sistema ya no sea necesario, destruyémalo llamando al [**método DestroySystem.**](destroysystem-msvm-virtualsystemmanagementservice.md)

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

 

