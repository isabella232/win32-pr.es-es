---
description: Obtiene una lista de instancias de CompatibilityVector de MSVM \_ que se pueden usar para comprobar la compatibilidad de host de la máquina virtual (VM).
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Msvm_VirtualSystemMigrationService:: GetSystemCompatibilityVectors (método)'
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
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000964"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a>MSVM \_ VirtualSystemMigrationService:: GetSystemCompatibilityVectors (método)

Obtiene una lista de instancias de [**\_ CompatibilityVector de MSVM**](msvm-compatibilityvector.md) que se pueden usar para comprobar la compatibilidad de host de la máquina virtual (VM).

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Una referencia a una clase de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual para la que se van a recuperar los vectores de compatibilidad. Si este parámetro hace referencia al sistema del equipo host, los datos devueltos en el parámetro *CompatibilityVectors* se pueden usar para determinar si cualquiera de las máquinas virtuales del equipo host se puede migrar rápidamente a otro sistema de host.

</dd> <dt>

*CompatibilityVectors* \[ enuncia\]
</dt> <dd>

Una matriz de instancias de [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) que contiene la información de compatibilidad para las máquinas virtuales o el sistema de hospedaje.

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
</dt> </dl>

## <a name="remarks"></a>Observaciones

**GetSystemCompatibilityVectors** obtiene información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host). La información de compatibilidad permanece opaca para el cliente, mientras que la información proporciona una manera de comparar la información de compatibilidad del host con la de la máquina virtual.

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

[**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md)
</dt> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




