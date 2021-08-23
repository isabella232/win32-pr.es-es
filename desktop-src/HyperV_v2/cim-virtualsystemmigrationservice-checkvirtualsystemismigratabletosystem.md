---
description: 'Más información sobre: Método CheckVirtualSystemIsMigratableToSystem de la CIM_VirtualSystemMigrationService clase'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Método CheckVirtualSystemIsMigratableToSystem de la CIM_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f2f543cff29464d76f1b2729efa9bca1a0c677d3cd7173975f59d2007aafb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682724"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToSystem de la clase \_ CIM VirtualSystemMigrationService

Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un sistema de destino. Este método no garantiza que una migración posterior siempre se realizará correctamente, debido a la disponibilidad dinámica de recursos. Descripción del código de retorno:

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

[**CIM \_ Instancia de ComputerSystem**](cim-computersystem.md) que hace referencia al sistema de equipo virtual de origen que se va a migrar.

</dd> <dt>

*DestinationSystem* \[ En\]
</dt> <dd>

[**CIM \_ Instancia**](cim-system.md) del sistema que hace referencia al sistema de destino al que se va a migrar el sistema virtual.

</dd> <dt>

*MigrationSettingData* \[ En\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la [**clase CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.

</dd> <dt>

*NewSystemSettingData* \[ En\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa nuevas propiedades aplicables al sistema virtual después de migrarla.

</dd> <dt>

*NewResourceSettingData* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**\_ ResourceAllocationSettingData de CIM**](cim-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de migrarlo.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

El resultado de la comprobación de migración indica si el sistema virtual se puede migrar correctamente o no.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>    | Comprobación realizada; resultado notificado a través del valor del \[ \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**No compatible**</dt> <dt>1</dt> </dl>              | Método no compatible con la implementación de . No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Error**</dt> <dt>2</dt> </dl>                     | Error de comprobación por motivos no especificados. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Tiempo de espera**</dt> <dt>3</dt> </dl>                    | Se ha pasado el tiempo de espera de la comprobación. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Parámetro 4 no**</dt> <dt>válido</dt> </dl>          | Uno o varios parámetros no son válidos formalmente. Por ejemplo, el valor del parámetro *DestinationSystem* no consta de una ruta de acceso de objeto válida. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                        |
| <dl> <dt>**Estado no válido**</dt> <dt>5</dt> </dl>              | El sistema virtual de origen, el sistema host de origen o el sistema host de destino se encuentran en un estado que permite iniciar la migración solicitada del sistema virtual. puede ser una condición temporal. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                    |
| <dl> <dt>**Parámetros incompatibles**</dt> <dt>6</dt> </dl>    | Uno o varios parámetros de entrada no son compatibles con un conjunto o con respecto al host de destino. Por ejemplo, el valor del *parámetro NewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del *parámetro DestinationSystem.* No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>.</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Método reservado**</dt> <dt>4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Específico del**</dt> <dt>proveedor 32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




