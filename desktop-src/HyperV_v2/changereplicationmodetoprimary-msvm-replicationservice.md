---
description: Cambia la relación de replicación extendida a la relación principal de una máquina virtual de réplica. La máquina virtual de réplica debe estar en un estado de conmutación por error confirmada.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Msvm_ReplicationService:: ChangeReplicationModeToPrimary (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666341"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a>MSVM \_ ReplicationService:: ChangeReplicationModeToPrimary (método)

Cambia la relación de replicación extendida a la relación principal de una máquina virtual de réplica. La máquina virtual de réplica debe estar en un estado de conmutación por error confirmada.

## <a name="syntax"></a>Sintaxis


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Referencia a una instancia de un equipo de [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que este método cambia la relación de replicación extendida a la relación principal.

</dd> <dt>

*ReplicationRelationship* \[ de\]
</dt> <dd>

Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación extendida que este método cambia a la relación principal.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)). Esta referencia puede ser **null** si la tarea se ha completado.

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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\\\Virtualización de raíz \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

