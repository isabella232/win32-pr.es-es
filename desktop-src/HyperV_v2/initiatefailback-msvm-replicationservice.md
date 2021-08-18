---
description: Inicia la conmutación por recuperación de una máquina virtual de recuperación.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: Msvm_ReplicationService::InitiateFailback (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b573cf1a0347e8df55b239451d9b99f3d416ebd5b3d0d61e662b6023f07a5b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644951"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a>Método \_ ReplicationService::InitiateFailback de Msvm

Inicia la conmutación por recuperación de una máquina virtual de recuperación.

## <a name="syntax"></a>Sintaxis


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia [**de Cim \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a iniciar una conmutación por recuperación.

</dd> <dt>

*ReplicationSettingData* \[ En\]
</dt> <dd>

Representación de cadena de una instancia incrustada de la clase [**\_ ReplicationSettingData de Msvm**](msvm-replicationsettingdata.md) que define la configuración de replicación para la conmutación por recuperación.

</dd> <dt>

*RecoveryPointIdentifier* \[ En\]
</dt> <dd>

Entrada opcional que identifica el punto de recuperación al que se solicita la conmutación por recuperación.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Esta referencia se puede usar para supervisar el progreso y obtener el resultado del método .

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

## <a name="remarks"></a>Comentarios

**InitiateFailback funciona** en una máquina virtual de recuperación y lleva la máquina virtual al *estado WaitingForFailback.* **InitiateFailback** reenvía la solicitud de conmutación por recuperación al proveedor correspondiente, que vuelve a sincronizar el punto de recuperación desde el lado principal nuevo. Una vez completada la conmutación por recuperación del punto de recuperación solicitado, el estado de replicación pasa *al estado FailbackCompleted.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ReplicationService de Msvm \_**](msvm-replicationservice.md)
</dt> </dl>

 

