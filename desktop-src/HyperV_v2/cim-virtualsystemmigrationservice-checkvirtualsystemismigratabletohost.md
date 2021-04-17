---
description: Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un host de destino especificado por un nombre de red o una dirección IP.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Método CheckVirtualSystemIsMigratableToHost de la clase CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687400"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToHost de la \_ clase VirtualSystemMigrationService de CIM

Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un host de destino especificado por un nombre de red o una dirección IP. Este método no garantiza que una migración posterior se realice siempre correctamente, debido a la disponibilidad dinámica de los recursos.

Descripción del código de retorno:

Nota: este método está pensado como una solución transitoria únicamente hasta que esté disponible el modelado de la compatibilidad con clústeres.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
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

Una referencia de [**\_ ComputerSystem de CIM**](cim-computersystem.md) al sistema del equipo virtual de origen que se va a migrar.

</dd> <dt>

*DestinationHost* \[ de\]
</dt> <dd>

Sistema host de destino para la migración.

Los formatos aceptables para este parámetro se transmiten a través de los valores de los elementos de la propiedad de matriz **DestinationHostFormatsSupported** \[ \] en la instancia de [**\_ VirtualSystemMigrationCapabilities de CIM**](cim-virtualsystemmigrationcapabilities.md) asociada a través de la Asociación [**\_ ElementCapabilities CIM**](cim-elementcapabilities.md) .

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



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>    | Comprobación realizada; resultado indicado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**No compatible**</dt> <dt>1</dt> </dl>              | Método no admitido por la implementación de. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**Error**</dt> <dt>2</dt> </dl>                     | Error al comprobar los motivos no especificados. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Tiempo de espera**</dt> <dt>3</dt> </dl>                    | Se agotó el tiempo de espera de la comprobación. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**Parámetro 4 no válido**</dt> <dt></dt> </dl>          | Uno o más parámetros no son válidos formalmente. Por ejemplo, se podría haber especificado el valor del parámetro *DestinationHost* en un formato no admitido. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                                                                    |
| <dl> <dt>**Estado 5 no válido**</dt> <dt></dt> </dl>              | El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite la iniciación de la migración del sistema virtual solicitada. puede tratarse de una condición temporal. No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/>                                                                                           |
| <dl> <dt>**Parámetros no compatibles**</dt> <dt>6</dt> </dl>    | Uno o varios parámetros de entrada no son compatibles como un conjunto o con respecto al host de destino. Por ejemplo, el valor del parámetro *MigrationNewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del parámetro *DestinationHost* . No se ha proporcionado ningún resultado a través del valor del \[ parámetro out \] *IsMigratable* .<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Método reservado**</dt> <dt>.. 32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> 32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

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

 

 




