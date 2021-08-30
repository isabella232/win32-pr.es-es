---
description: Determina si el sistema virtual especificado se puede migrar a un host de destino especificado por un nombre de red o una dirección IP.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Método CheckVirtualSystemIsMigratableToHost de la Msvm_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5305ead7b84255524d87355596015a06d6dba7887ba028bdc5e677b4a9e6cd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041915"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToHost de la clase Msvm \_ VirtualSystemMigrationService

Determina si el sistema virtual especificado se puede migrar a un host de destino especificado por un nombre de red o una dirección IP.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa la máquina virtual de la que se probará la capacidad de migración.

</dd> <dt>

*DestinationHost* \[ En\]
</dt> <dd>

Nombre del sistema host para la migración. La propiedad **DestinationHostFormatsSupported** de la clase [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) asociada a esta clase especifica el formato de este nombre.

</dd> <dt>

*MigrationSettingData* \[ En\]
</dt> <dd>

Instancia incrustada de la [**clase Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.

</dd> <dt>

*NewSystemSettingData* \[ En\]
</dt> <dd>

Instancia insertada de la [**clase Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa nuevas propiedades aplicables al sistema virtual después de migrarla.

</dd> <dt>

*NewResourceSettingData* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**\_ ResourceAllocationSettingData de Msvm**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de migrarlo.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

Recibe el resultado de la comprobación de migración que indica si el sistema virtual se puede migrar correctamente.

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

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**Parámetros incompatibles** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535 )
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

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




