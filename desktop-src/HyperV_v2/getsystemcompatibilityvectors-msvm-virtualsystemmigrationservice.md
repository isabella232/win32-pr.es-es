---
description: Obtiene una lista de instancias de Msvm CompatibilityVector que se pueden usar para comprobar la compatibilidad de máquina \_ virtual (VM) para hospedar.
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: Msvm_VirtualSystemMigrationService::GetSystemCompatibilityVectors (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 19eb9fe54c9a20e635d706eff9b22eb0e78cb8347b27fcdcaff0f419e60a6112
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427665"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>Método Msvm \_ VirtualSystemMigrationService::GetSystemCompatibilityVectors

Obtiene una lista de instancias de [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que se pueden usar para comprobar la compatibilidad de máquina virtual (VM) para hospedar.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa la máquina virtual para la que se recuperarán los vectores de compatibilidad. Si este parámetro hace referencia al sistema del equipo host, los datos devueltos en el parámetro *CompatibilityVectors* se pueden usar para determinar si alguna de las máquinas virtuales del sistema del equipo host se puede migrar rápidamente a otro sistema de equipo host.

</dd> <dt>

*CompatibilityVectors* \[ out\]
</dt> <dd>

Matriz de [**instancias de Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que contienen la información de compatibilidad para las máquinas virtuales o el sistema de equipo de hospedaje.

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

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentarios

**GetSystemCompatibilityVectors** obtiene información de compatibilidad para una máquina virtual (VM) (cuando se ejecuta en un sistema de equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host). La información de compatibilidad permanece opaca para el cliente, mientras que la información proporciona una manera de comparar la información de compatibilidad del host con la de la máquina virtual.

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

[**Compatibilidad de \_ MsvmVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




