---
description: Realiza una operación de resincronización en la máquina virtual especificada.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Método Resynchronize de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 007a2a620c1ce9ba867b86a1a9dd1ac77324b6712ef04b8ad10736e1ceac3624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913975"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a>Método Resynchronize de la clase ReplicationService de Msvm \_

Realiza una operación de resincronización en la máquina virtual especificada. Cuando un cliente llama a este método para una máquina virtual de réplica, se vuelve a sincronizar con la réplica extendida.

Estos métodos comparan los discos habilitados para replicación en las máquinas virtuales principales y de recuperación, y corrigen los problemas de integridad de los datos de replicación mediante la replicación de los distintos bloques de la principal a la recuperación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**\_ de ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual que se va a resincronizar.

</dd> <dt>

*StartTime* \[ En\]
</dt> <dd>

Hora de inicio programada para que comience la operación de resincronización. Si este parámetro es **Null,** la operación de resincronización se inicia inmediatamente.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método activados: trabajo iniciado** (4096)
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
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> </dl>

 

