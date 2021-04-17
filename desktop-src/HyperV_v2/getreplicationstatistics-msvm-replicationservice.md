---
description: Recupera las estadísticas de replicación de una máquina virtual y actúa en la relación de replicación principal de la máquina virtual.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Método GetReplicationStatistics de la clase Msvm_ReplicationService
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
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666550"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Método GetReplicationStatistics de la \_ clase ReplicationService de MSVM

Recupera las estadísticas de replicación de una máquina virtual y actúa en la relación de replicación principal de la máquina virtual.

> [!Note]  
> A partir de Windows 8.1, se recomienda no usar **GetReplicationStatistics** para recuperar las estadísticas de replicación. En su lugar, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).

 

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

*ComputerSystem* \[ de\]
</dt> <dd>

Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se van a recuperar las estadísticas de replicación.

</dd> <dt>

*ReplicationStatistics* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente, recibe una instancia incrustada de la clase [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contiene las estadísticas de replicación de la máquina virtual solicitada.

</dd> <dt>

*ReplicationHealthIssues* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente, recibe una matriz de instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) que indican cualquier advertencia o error de replicación de la máquina virtual solicitada.

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

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

