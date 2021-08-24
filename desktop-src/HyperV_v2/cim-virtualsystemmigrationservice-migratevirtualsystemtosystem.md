---
description: Método para mover, migrar o reubicar un sistema virtual a un sistema de destino.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Método MigrateVirtualSystemToSystem de la CIM_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7b60e691f2f873a26a52f59def32b35005d45914f7fe379af14b5260b02a0c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393423"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método MigrateVirtualSystemToSystem de la clase \_ CIM VirtualSystemMigrationService

Método para mover, migrar o reubicar un sistema virtual a un sistema de destino.

Descripción del código de retorno:

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

*ComputerSystem* \[ En\]
</dt> <dd>

Sistema de equipo virtual de origen que se va a migrar.

</dd> <dt>

*DestinationSystem* \[ En\]
</dt> <dd>

Sistema host de destino donde migrar el sistema virtual.

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

*NewComputerSystem* \[ out\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ComputerSystem de CIM**](cim-computersystem.md) que representa el sistema del equipo virtual después de migrarlo.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver [**un \_ concretejob CIM**](cim-concretejob.md) que representa el trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.



| Código o valor devuelto                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Se migró el sistema virtual.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**No se admite**</dt> <dt>1</dt> </dl>                              | Método no compatible con la implementación de .<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Error**</dt> <dt>2</dt> </dl>                                     | Error de migración del sistema virtual por motivos no especificados.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Tiempo de espera**</dt> <dt>3</dt> </dl>                                    | Tiempo de espera de migración del sistema virtual; el estado del sistema virtual es desconocido.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Parámetro 4 no**</dt> <dt>válido</dt> </dl>                          | Uno o varios parámetros no son formalmente válidos Por ejemplo, el valor del parámetro Sistema de destino no contiene una ruta de acceso de objeto válida.<br/>                                                                                                                                                    |
| <dl> <dt>**Estado no válido**</dt> <dt>5</dt> </dl>                              | El sistema virtual de origen, el sistema host de origen o el sistema host de destino están en un estado que permite iniciar la migración del sistema virtual solicitado; puede ser una condición temporal.<br/>                                                                                             |
| <dl> <dt>**Parámetros incompatibles**</dt> <dt>6</dt> </dl>                    | Uno o varios parámetros de entrada son incompatibles como un conjunto o con respecto al host de destino. Por ejemplo, el valor del *parámetro MigrationNewSettingData* contiene propiedades que no son compatibles con el sistema host de destino identificado por el valor del *parámetro DestinationSystem.*<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>.</dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Método reservado**</dt> <dt>4097..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Específico del**</dt> <dt>proveedor 32768..65535</dt> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




