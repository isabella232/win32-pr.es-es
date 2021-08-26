---
description: Determina si se puede migrar el sistema virtual especificado.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Método CheckVirtualSystemIsMigratable de la Msvm_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7da99fc5fe2eb69ff93ce85fa2335ca63a36291975b1349097e1586fe15e2cf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041935"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratable de la clase \_ VirtualSystemMigrationService de Msvm

Determina si se puede migrar el sistema virtual especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ComputerSystem de CIM**](cim-computersystem.md) que representa la máquina virtual de la que se probará la capacidad de migración.

</dd> <dt>

*DestinationHost* \[ En\]
</dt> <dd>

Nombre del sistema host para la migración. La propiedad **DestinationHostFormatsSupported** de la clase [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) asociada a esta clase especifica el formato de este nombre.

</dd> <dt>

*MigrationSettingData* \[ En\]
</dt> <dd>

Instancia insertada de la [**clase Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa la configuración de la operación de migración.

</dd> <dt>

*NewSystemSettingData* \[ En\]
</dt> <dd>

Instancia incrustada de la clase [**\_ Msvm VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de migrarla.

</dd> <dt>

*NewResourceSettingData* \[ En\]
</dt> <dd>

Matriz de cadenas que contienen una instancia incrustada de la clase [**\_ ResourceAllocationSettingData de Msvm**](msvm-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales del sistema virtual después de migrarlo.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

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

 

