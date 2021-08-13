---
description: Recupera las estadísticas de replicación asociadas a la relación de replicación especificada de la máquina virtual.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: Msvm_ReplicationService::GetReplicationStatisticsEx (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d4386692dcaf86527e28b82c91415bf858b47cd19bbc4693af6bff12255138c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253705"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a>Método Msvm \_ ReplicationService::GetReplicationStatisticsEx

Recupera las estadísticas de replicación asociadas a la relación de replicación especificada de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se recuperan las estadísticas de replicación.

</dd> <dt>

*ReplicationRelationship* \[ En\]
</dt> <dd>

Representación de cadena de una instancia incrustada de la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) que define la relación de replicación para la que se recuperan las estadísticas de replicación.

</dd> <dt>

*ReplicationStatistics* \[ out\]
</dt> <dd>

Si se realiza correctamente, recibe una instancia incrustada de la clase [**\_ ReplicationStatistics de Msvm**](msvm-replicationstatistics.md) que contiene las estadísticas de replicación de la relación de replicación solicitada.

</dd> <dt>

*ReplicationHealthIssues* \[ out\]
</dt> <dd>

Si se realiza correctamente, recibe una matriz de instancias insertadas de la clase Error de [**Msvm \_**](msvm-error.md) que indican cualquier advertencia o error de replicación para la máquina virtual solicitada.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Esta referencia puede ser **NULL** si la tarea se ha completado.

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

**Sistema en uso** (32774)
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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> <dt>

[**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

