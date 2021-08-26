---
description: Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un host de destino especificado por un nombre de red o una dirección IP.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Método CheckVirtualSystemIsMigratableToHost de la CIM_VirtualSystemMigrationService clase
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
ms.openlocfilehash: 061cf41d2c509a1fb670f2fc8fb5d56c98d54e3619bfddae59857c2cf9cc51b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980525"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToHost de la clase \_ CIM VirtualSystemMigrationService

Método para realizar una comprobación previa para determinar si es probable que un sistema virtual se migre correctamente a un host de destino especificado por un nombre de red o una dirección IP. Este método no garantiza que una migración posterior siempre se realizará correctamente, debido a la disponibilidad dinámica de los recursos.

Descripción del código de retorno:

Nota: Este método está pensado como una solución de transición solo hasta que el modelado de compatibilidad con clústeres esté disponible.

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

*ComputerSystem* \[ En\]
</dt> <dd>

Una [**referencia \_ cim computersystem**](cim-computersystem.md) al sistema de equipo virtual de origen que se va a migrar.

</dd> <dt>

*DestinationHost* \[ En\]
</dt> <dd>

Sistema host de destino para la migración.

Los formatos aceptables para este parámetro se transmiten a través de valores de elementos de la propiedad de matriz **DestinationHostFormatsSupported** en la instancia de \[ \] [**CIM \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) que está asociada a través de la asociación [**\_ ElementCapabilities de CIM.**](cim-elementcapabilities.md)

</dd> <dt>

*MigrationSettingData* \[ En\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa la configuración de migración aplicable a la operación de migración.

</dd> <dt>

*NewSystemSettingData* \[ En\]
</dt> <dd>

Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa nuevas propiedades aplicables al sistema virtual después de migrarla.

</dd> <dt>

*NewResourceSettingData* \[ En\]
</dt> <dd>

Matriz de cadenas que contiene una instancia incrustada de la clase [**\_ ResourceAllocationSettingData de CIM**](cim-resourceallocationsettingdata.md) que representa nuevas propiedades aplicables a los recursos virtuales en el ámbito del sistema virtual después de migrarla.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

El resultado de la comprobación de migración indica si el sistema virtual se puede migrar correctamente o no.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>    | Comprobación realizada; resultado notificado a través del valor del \[ \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**No se admite**</dt> <dt>1</dt> </dl>              | Método no compatible con la implementación de . No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**Error**</dt> <dt>2</dt> </dl>                     | Error de comprobación por motivos no especificados. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Tiempo de espera**</dt> <dt>3</dt> </dl>                    | Se ha pasado el tiempo de espera de la comprobación. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**Parámetro 4 no**</dt> <dt>válido</dt> </dl>          | Uno o varios parámetros no son formalmente válidos. Por ejemplo, el valor del parámetro *DestinationHost* se podría haber especificado en un formato no admitido. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                                                                    |
| <dl> <dt>**Estado no válido**</dt> <dt>5</dt> </dl>              | El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite iniciar la migración del sistema virtual solicitado; puede ser una condición temporal. No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/>                                                                                           |
| <dl> <dt>**Parámetros incompatibles**</dt> <dt>6</dt> </dl>    | Uno o varios parámetros de entrada son incompatibles como un conjunto o con respecto al host de destino. Por ejemplo, el valor del parámetro *MigrationNewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del *parámetro DestinationHost.* No se notifica ningún resultado a través del valor \[ del \] *parámetro Out IsMigratable.*<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>.</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Método reservado**</dt> <dt>4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Específico del**</dt> <dt>proveedor 32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




