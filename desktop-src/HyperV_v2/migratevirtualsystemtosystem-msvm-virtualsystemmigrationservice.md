---
description: Mueve, migra o reubica un sistema virtual en un sistema de destino.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Método MigrateVirtualSystemToSystem de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360593"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método MigrateVirtualSystemToSystem de la \_ clase VirtualSystemMigrationService de MSVM

Mueve, migra o reubica un sistema virtual en un sistema de destino.

## <a name="syntax"></a>Sintaxis


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema del equipo virtual que se va a migrar.

</dd> <dt>

*DestinationSystem* \[ de\]
</dt> <dd>

Referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema al que se va a migrar.

</dd> <dt>

*MigrationSettingData* \[ de\]
</dt> <dd>

Instancia insertada de la clase [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.

</dd> <dt>

*NewSystemSettingData* \[ de\]
</dt> <dd>

Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.

</dd> <dt>

*NewResourceSettingData* \[ de\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de su migración.

</dd> <dt>

*NewComputerSystem* \[ enuncia\]
</dt> <dd>

Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el nuevo sistema migrado.

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

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
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

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

