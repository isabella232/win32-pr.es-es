---
description: Determina si el sistema virtual especificado se puede migrar a un sistema de destino.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Método CheckVirtualSystemIsMigratableToSystem de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686577"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToSystem de la \_ clase VirtualSystemMigrationService de MSVM

Determina si el sistema virtual especificado se puede migrar a un sistema de destino.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual para probar la capacidad de migración de.

</dd> <dt>

*DestinationSystem* \[ de\]
</dt> <dd>

Una referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual en la que se va a probar la capacidad de migración.

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

*IsMigratable* \[ enuncia\]
</dt> <dd>

Recibe el resultado de la comprobación de la migración que indica si el sistema virtual se puede migrar correctamente.

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

**Método reservado** (de no.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




