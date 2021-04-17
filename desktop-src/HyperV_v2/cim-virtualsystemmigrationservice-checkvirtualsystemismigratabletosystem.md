---
description: 'Más información sobre: método CheckVirtualSystemIsMigratableToSystem de la clase CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Método CheckVirtualSystemIsMigratableToSystem de la clase CIM_VirtualSystemMigrationService
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
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687399"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToSystem de la \_ clase VirtualSystemMigrationService de CIM

Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un sistema de destino. Este método no garantiza que una migración posterior se realice siempre correctamente, debido a la disponibilidad dinámica de los recursos. Descripción del código de retorno:

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

*ComputerSystem* \[ de\]
</dt> <dd>

[**CIM \_**](cim-computersystem.md) Instancia de ComputerSystem que hace referencia al sistema del equipo virtual de origen que se va a migrar.

</dd> <dt>

*DestinationSystem* \[ de\]
</dt> <dd>

[**CIM \_ Instancia del sistema**](cim-system.md) que hace referencia al sistema de destino en el que se va a migrar el sistema virtual.

</dd> <dt>

*MigrationSettingData* \[ de\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.

</dd> <dt>

*NewSystemSettingData* \[ de\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa las nuevas propiedades aplicables al sistema virtual después de su migración.

</dd> <dt>

*NewResourceSettingData* \[ de\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa las nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de su migración.

</dd> <dt>

*IsMigratable* \[ enuncia\]
</dt> <dd>

Resultado de la comprobación de la migración que indica si el sistema virtual se puede migrar correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>    | Comprobación realizada; resultado indicado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**No compatible**</dt> <dt>1</dt> </dl>              | Método no admitido por la implementación de. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Error**</dt> <dt>2</dt> </dl>                     | Error al comprobar los motivos no especificados. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Tiempo de espera**</dt> <dt>3</dt> </dl>                    | Se agotó el tiempo de espera de la comprobación. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Parámetro 4 no válido**</dt> <dt></dt> </dl>          | Uno o más parámetros no son válidos formalmente. Por ejemplo, el valor del parámetro *DestinationSystem* no incluye una ruta de acceso de objeto válida. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                        |
| <dl> <dt>**Estado 5 no válido**</dt> <dt></dt> </dl>              | El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite la iniciación de la migración del sistema virtual solicitada. puede tratarse de una condición temporal. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                    |
| <dl> <dt>**Parámetros no compatibles**</dt> <dt>6</dt> </dl>    | Uno o varios parámetros de entrada no son compatibles como un conjunto o con respecto al host de destino. Por ejemplo, el valor del parámetro *NewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del parámetro *DestinationSystem* . No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Método reservado**</dt> <dt>.. 32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> 32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




