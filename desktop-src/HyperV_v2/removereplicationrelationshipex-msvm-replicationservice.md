---
description: Quita la relación de replicación de la máquina virtual especificada.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Msvm_ReplicationService:: RemoveReplicationRelationshipEx (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666602"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a>MSVM \_ ReplicationService:: RemoveReplicationRelationshipEx (método)

Quita la relación de replicación de la máquina virtual especificada.

## <a name="syntax"></a>Sintaxis


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a quitar la replicación.

</dd> <dt>

*ReplicationRelationship* \[ de\]
</dt> <dd>

Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación que se va a quitar.

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

## <a name="remarks"></a>Observaciones

En el caso de una máquina virtual de réplica, no se puede quitar la replicación principal si está habilitada la replicación extendida.

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

[**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

