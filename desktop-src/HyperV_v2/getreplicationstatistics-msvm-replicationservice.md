---
description: Recupera las estadísticas de replicación de una máquina virtual y actúa sobre la relación de replicación principal de la máquina virtual.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Método GetReplicationStatistics de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 767ea873b725523e3d430708dc5485d3d24c62e07e5cebac001b020ee996bd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392935"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Método GetReplicationStatistics de la clase ReplicationService de Msvm \_

Recupera las estadísticas de replicación de una máquina virtual y actúa sobre la relación de replicación principal de la máquina virtual.

> [!Note]  
> A partir Windows 8.1, se recomienda no usar **GetReplicationStatistics** más para recuperar las estadísticas de replicación. En su lugar, [**use GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se recuperan las estadísticas de replicación.

</dd> <dt>

*ReplicationStatistics* \[ out\]
</dt> <dd>

Si se realiza correctamente, recibe una instancia incrustada de la clase [**\_ ReplicationStatistics de Msvm**](msvm-replicationstatistics.md) que contiene las estadísticas de replicación de la máquina virtual solicitada.

</dd> <dt>

*ReplicationHealthIssues* \[ out\]
</dt> <dd>

Si se realiza correctamente, recibe una matriz de instancias incrustadas de la clase Error de [**Msvm \_**](msvm-error.md) que indican cualquier advertencia o error de replicación para la máquina virtual solicitada.

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

**Sistema en uso** (32774)
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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> </dl>

 

