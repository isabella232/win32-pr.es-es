---
description: La clase \_ CacheMemory de CIM define las funcionalidades y la administración de la memoria caché.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: CIM_CacheMemory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c64fd25df2d81f7debf78fd0a50f69656b16c2c5309b1955e1aa0e96e6dde403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284555"
---
# <a name="cim_cachememory-class"></a>Cim \_ CacheMemory (clase)

La **clase \_ CacheMemory** de CIM define las funcionalidades y la administración de la memoria caché.

La memoria caché es la RAM dedicada o asignada donde un procesador busca primero los datos. Los datos de la memoria caché se entregan rápidamente al procesador y normalmente se describen por su proximidad al procesador (por ejemplo, caché principal o secundaria). Una unidad de disco que incluye ram asignada para contener los datos más recientes leídos o adyacentes del disco (para acelerar la recuperación) también se modela como memoria caché.

> [!Note]  
> La memoria caché no es un búfer de nivel de aplicación o sistema operativo; es la RAM que se ha asignado para almacenar en caché los datos del procesador.

 

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a>Miembros

La **clase \_ CacheMemory** de CIM tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ CacheMemory** de CIM tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Restablecer**](reset-method-in-class-cim-cachememory.md)                 | Solicita un restablecimiento del dispositivo lógico. No implementado por WMI.<br/>                                                                 |
| [**SetPowerState**](setpowerstate-method-in-class-cim-cachememory.md) | Define el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar el dispositivo en ese estado. No implementado por WMI.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ CacheMemory** de CIM tiene estas propiedades.

<dl> <dt>

**Acceder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe las propiedades de lectura y escritura del medio.

Esta propiedad se hereda de [**CIM \_ StorageExtent.**](cim-storageextent.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Legible** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Escritura** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lectura y escritura admitidas** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**Escribir una vez** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.18", "MIF. Matriz de memoria física DMTF \| \| 001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Matriz de octetos que contiene información de error adicional. Un ejemplo es comprobación de errores y corrección (ECC) Deserción, o la devolución de los bits de comprobación si se usa una metodología de error basada en CRC. En el último caso, si se reconoce un error de un solo bit y se conoce el algoritmo CRC, se puede determinar el bit exacto que produjo el error. En este campo se incluye este tipo de datos (ECC, check-bit, parity-bit u otra información proporcionada por el proveedor). Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

</dd> <dt>

**asociatividad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.15")
</dt> </dl>

Enumeración que define la asociatividad de la memoria caché del sistema.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

**Asignado directamente** (3)


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

**Conjunto asociativo de dos vías** (4)


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

**Set-Associative de 4 vías** (5)


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

**Totalmente asociativo** (6)


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

**Set-Associative de 8 vías** (7)


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

**Conjunto asociativo de 16 vías** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
</dt> </dl>

Disponibilidad y estado del dispositivo.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Energía completa o en ejecución** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Advertencia** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En prueba** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Apagado** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera de servicio** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de** instalación (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Ahorro de energía: desconocido** (13)


</dt> <dd>

Se sabe que el dispositivo está en modo de ahorro de energía, pero se desconoce su estado exacto.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Ahorro de energía: modo de bajo consumo** (14)


</dt> <dd>

El dispositivo está en un estado de ahorro de energía pero sigue funcionando y puede presentar un rendimiento degradado.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Ahorro de energía: en espera** (15)


</dt> <dd>

El dispositivo no funciona, pero se podría encender rápidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de** energía (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Ahorro de energía: advertencia** (17)


</dt> <dd>

El dispositivo está en estado de advertencia, aunque también en modo de ahorro de energía.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**En pausa** (18)


</dt> <dd>

El dispositivo está en pausa.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)


</dt> <dd>

El dispositivo no está listo.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Sin configurar** (20)


</dt> <dd>

El dispositivo no está configurado.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)


</dt> <dd>

El dispositivo está silencioso.

</dd> </dl>

</dd> <dt>

**Blocksize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño, en bytes, de los bloques que forman la extensión de almacenamiento. Si el tamaño del bloque de variables es variable, se debe especificar el tamaño máximo del bloque, en bytes. Si se desconoce el tamaño del bloque o si un concepto de bloque no es válido (por ejemplo, para extensiones de agregado, memoria o discos lógicos), escriba 1 (uno).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de [**CIM \_ StorageExtent.**](cim-storageextent.md)

</dd> <dt>

**CacheType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.9")
</dt> </dl>

Especifica el almacenamiento en caché de instrucciones, el almacenamiento en caché de datos o ambos. También se pueden definir "Other" y "Unknown".

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

**Instrucción** (3)


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

**Datos** (4)


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

**Unificado** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Código de error Administrador de configuración Win32.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

**Este dispositivo funciona correctamente.**  (0)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

**Este dispositivo no está configurado correctamente.** (1)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

**Windows puede cargar el controlador para este dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.** (3)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro podrían estar dañados.** (4)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

**El controlador para este dispositivo necesita un recurso que Windows puede administrar.** (5)


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**  (6)


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

**No se puede filtrar.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

**Falta el cargador de controladores para el dispositivo.** (8)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

**Este dispositivo no funciona correctamente porque el firmware de control informa incorrectamente de los recursos del dispositivo.** (9)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

**Este dispositivo no se puede iniciar.** (10)


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

**Error en este dispositivo.** (11)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

**Este dispositivo no puede encontrar suficientes recursos gratuitos que pueda usar.** (12)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

**Windows puede comprobar los recursos de este dispositivo.** (13)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.** (14)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

**Este dispositivo no funciona correctamente porque probablemente haya un problema de enumeración.** (15)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

**Windows puede identificar todos los recursos que usa este dispositivo.** (16)


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

**Este dispositivo solicita un tipo de recurso desconocido.** (17)


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

**Vuelva a instalar los controladores de este dispositivo.** (18)


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

**Error al usar el cargador VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

**Es posible que el registro esté dañado.** (20)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

**Error del sistema: intente cambiar el controlador de este dispositivo. Si eso no funciona, consulte la documentación de hardware. Windows está quitando este dispositivo.** (21)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

**Este dispositivo está deshabilitado.** (22)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

**Error del sistema: intente cambiar el controlador de este dispositivo. Si eso no funciona, consulte la documentación de hardware.** (23)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.** (24)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

**Windows está configurando este dispositivo.** (25)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

**Windows está configurando este dispositivo.** (26)


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

**Este dispositivo no tiene una configuración de registro válida.** (27)


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

**Los controladores de este dispositivo no están instalados.** (28)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

**Este dispositivo está deshabilitado porque el firmware del dispositivo no le ha dado los recursos necesarios.** (29)


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que usa otro dispositivo.** (30)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

**Este dispositivo no funciona correctamente porque Windows puede cargar los controladores necesarios para este dispositivo.** (31)


</dt> <dd></dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Si **es TRUE,** el dispositivo usa una configuración definida por el usuario.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.12", "MIF. Matriz de memoria física DMTF \| \| 001.8")
</dt> </dl>

Si **es TRUE,** se puede corregir el error más reciente. Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Dirección u otra información de identificación para dar un nombre único al dispositivo lógico.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array Mapped Addresses \| 001.4", "MIF. DMTF \| Memory Device Mapped Addresses \| 001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Dirección final a la que hace referencia una aplicación o sistema operativo y asignada por un controlador de memoria para este objeto de memoria. La dirección final se especifica en kilobytes.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.15", "MIF. Matriz de memoria física DMTF \| \| 001.10")
</dt> </dl>

Operación de acceso a memoria que produjo el último error. La propiedad **ErrorInfo** describe el tipo de error. Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Read** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Escritura** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Escritura parcial** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.19", "MIF. Dispositivo de memoria DMTF \| \| 002.20", "MIF. Matriz de memoria física DMTF \| \| 001.14")
</dt> </dl>

Dirección del último error de memoria. La propiedad **ErrorInfo** describe el tipo de error. Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** ahora se borra el error notificado en la propiedad **LastErrorCode.**

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.17", "MIF. Matriz de memoria física DMTF \| \| 001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Datos capturados durante el último acceso erróneo a la memoria. Los datos ocupan los primeros *n octetos* de la matriz que son necesarios para contener el número de bits especificado por la **propiedad ErrorTransferSize.** Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Orden de los datos almacenados en la **propiedad ErrorData.** Si **ErrorTransferSize** es 0, esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Primer byte menos significativo** (1)


</dt> <dd>

Byte menos significativo primero.

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Primer byte más significativo** (2)


</dt> <dd>

Byte más significativo primero.

</dd> </dl>

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que proporciona información sobre el error registrado en la **propiedad LastErrorCode** y las acciones correctivas que se deben realizar.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memoria DMTF \| \| 002.12", "MIF. Matriz de memoria física DMTF \| \| 001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Cim \_ Memory**](cim-memory.md).**OtherErrorDescription**")
</dt> </dl>

Tipo de error que se produjo más recientemente. Los valores del 12 al 14 no están definidos en el esquema CIM porque DMI combina la semántica del tipo de error y si se puede corregir. Si se puede corregir un error, se indica en la **propiedad CorrectableError.**

Esta propiedad se hereda de la [**memoria CIM \_**](cim-memory.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**Aceptar** (3)


</dt> <dd>

Aceptar.

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Lectura no leída** (4)


</dt> <dd>

Lecturas no leída.

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Error de paridad** (5)


</dt> <dd>

Error de paridad.

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Error de un solo bit** (6)


</dt> <dd>

Error de un solo bit.

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Error de doble bit** (7)


</dt> <dd>

Error de doble bit.

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Error de varios bits** (8)


</dt> <dd>

Error de varios bits.

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Error de nibble** (9)


</dt> <dd>

Error de nibble.

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Error de suma de** comprobación (10)


</dt> <dd>

Error de suma de comprobación.

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Error de CRC** (11)


</dt> <dd>

Error de CRC.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (12)


</dt> <dd>

Sin definir.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (13)


</dt> <dd>

Sin definir.

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (14)


</dt> <dd>

Sin definir.

</dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Matriz de memoria física DMTF \| \| 001.7")
</dt> </dl>

Indica si se usan algoritmos de paridad o CRC, ECC u otros mecanismos. También se pueden proporcionar detalles sobre el algoritmo.

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.21", "MIF. Matriz de memoria física DMTF \| \| 001.15"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Especifica el intervalo, en bytes, en el que se puede resolver el último error. Por ejemplo, si las direcciones de error se resuelven en el bit 11 (es decir, en una página típica), los errores se pueden resolver en límites de 4 KB y esta propiedad se establece en 4000. Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se produjo el último error de memoria. La propiedad **ErrorInfo** describe el tipo de error. Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002.16", "MIF. Matriz de memoria física DMTF \| \| 001.11"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Tamaño de la transferencia de datos, en bits, que produjo el último error. Un valor de 0 indica que no hay ningún error. Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad debe establecerse en 0.

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**FlushTimer**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.14"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")
</dt> </dl>

Cantidad máxima de tiempo, en segundos, es posible que las líneas o cubos desnuciados permanezcan en la memoria caché antes de vaciarse. Un valor de 0 indica que un temporizador de vaciado no controla un vaciado de caché.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último código de error notificado por el dispositivo lógico.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.2")
</dt> </dl>

Especifica si se trata de la caché principal, secundaria o terciaria. También se pueden definir "Other", "Unknown" y "Not Applicable".

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (3)


</dt> <dd>

Principal.

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundaria** (4)


</dt> <dd>

Secundaria.

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciario** (5)


</dt> <dd>

Terciario.

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)


</dt> <dd>

No es aplicable.

</dd> </dl>

</dd> <dt>

**LineSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.10"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño, en bytes, de un único cubo o línea de caché.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrStorageSize")
</dt> </dl>

Número de bloques consecutivos, cada uno de los que bloquea el tamaño del valor contenido en la **propiedad BlockSize,** que forman la extensión de almacenamiento. El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **BlockSize** por el valor de esta propiedad. Si el valor de **BlockSize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Esta propiedad se hereda de [**CIM \_ StorageExtent.**](cim-storageextent.md)

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Memoria CIM \_**](cim-memory.md).**ErrorInfo**")
</dt> </dl>

Cadena de forma libre que proporciona información si la **propiedad ErrorType** está establecida en 1 ("Other"). Si no se establece en 1, esta cadena no tiene ningún significado.

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.

Ejemplo: \* "PNP030b"

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica las funcionalidades específicas relacionadas con la energía del dispositivo lógico.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Se desconocen las capacidades relacionadas con la energía.

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)


</dt> <dd>

Las capacidades relacionadas con la energía no se admiten para este dispositivo.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)


</dt> <dd>

Se han deshabilitado las capacidades relacionadas con la energía.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)


</dt> <dd>

Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía especificados automáticamente** (4)


</dt> <dd>

El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Se **admite el método SetPowerState.** Este método se encuentra en la clase [**\_ logicalDevice**](cim-logicaldevice.md) de CIM primaria y se puede implementar. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes .](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling compatible** (6)


</dt> <dd>

El **método SetPowerState** se puede invocar con el *parámetro PowerState* establecido en 5 ("Ciclo de energía").

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Encendido con tiempo de encendido admitido** (7)


</dt> <dd>

El **método SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("Ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o intervalo, para el encendido.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el dispositivo se puede administrar con energía, es decir, poner en un estado de ahorro de energía. Si **es FALSE,** el valor entero 1 ("No compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities.**

Esta propiedad no indica si las características de administración de energía están habilitadas actualmente, o si están habilitadas, qué características se admiten. Para obtener más información, vea la **matriz PowerManagementCapabilities.**

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**Propósito**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que describe el medio y su uso.

Esta propiedad se hereda de [**CIM \_ StorageExtent.**](cim-storageextent.md)

</dd> <dt>

**ReadPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.13")
</dt> </dl>

Directiva empleada por la memoria caché para controlar las solicitudes de lectura. Si la directiva de lectura se determina individualmente, es decir, para cada solicitud, se debe especificar el valor 6 ("Determinación por E/S"). "Other" y "Unknown" también son valores válidos.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Lectura** (3)


</dt> <dd>

Lectura.

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Lectura adelantada** (4)


</dt> <dd>

Lectura adelantada.

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Lectura y lectura adelantada** (5)


</dt> <dd>

Lectura y lectura adelantada.

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinación por E/S** (6)


</dt> <dd>

Determinación por E/S.

</dd> </dl>

</dd> <dt>

**ReplacementPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.12")
</dt> </dl>

Enumeración de enteros que describe el algoritmo que determina qué líneas o cubos de caché se deben volver a usar.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Usados menos recientemente (LRU)** (3)


</dt> <dd>

Usados menos recientemente (LRU).

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)


</dt> <dd>

Primero en, primero en salir (FIFO).

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Último en salir (LIFO)** (5)


</dt> <dd>

Último en, primero en salir (LIFO).

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Uso menos frecuente (LFU)** (6)


</dt> <dd>

Usado con menos frecuencia (LFU).

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Usado con más frecuencia (MFU)** (7)


</dt> <dd>

Usado con más frecuencia (MFU).

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Algoritmos múltiples dependientes de los** datos (8)


</dt> <dd>

Varios algoritmos dependientes de los datos.

</dd> </dl>

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array Mapped Addresses \| 001.3", "MIF. DMTF \| Memory Device Mapped Addresses \| 001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Dirección inicial, a la que hace referencia una aplicación o sistema operativo y que asigna un controlador de memoria, para este objeto de memoria. La dirección inicial se especifica en kilobytes.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir el estado operativo y no operativo. El estado operativo puede incluir "Ok", "Degraded" y "Pred Fail". "Error previo" indica que un elemento funciona correctamente, pero predice un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". El "servicio" se puede aplicar durante la resilvering del reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**A partir** de ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Deteniendo")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.3")
</dt> </dl>

Estado del dispositivo lógico. Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("No aplicable").

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**Clave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre de clase de creación del sistema de ámbito.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la información de dirección de la **propiedad ErrorAddress** es una dirección de nivel de sistema (**TRUE**) o una dirección física (**FALSE**). Si la **propiedad ErrorInfo** es igual a 3 ("Ok"), esta propiedad no tiene ningún significado.

Esta propiedad se hereda de la [**memoria \_ CIM**](cim-memory.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**Nombre**"), [**Clave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre del sistema de ámbito.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**WritePolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Caché del sistema DMTF \| \| 003.5")
</dt> </dl>

Define si la memoria caché es de reescribición o escritura a través, o si la información "Varía con dirección" o se define individualmente para cada entrada/salida. También se pueden especificar "Other" y "Unknown".

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Reescriba** (3)


</dt> <dd>

Reescriba.

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Escritura a través** de (4)


</dt> <dd>

Escribir en .

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varía con la dirección** (5)


</dt> <dd>

Varía según la dirección.

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determinación por E/S** (6)


</dt> <dd>

Determinación por E/S.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ Cim CacheMemory** se deriva de [**la memoria \_ CIM**](cim-memory.md).

WMI no implementa esta clase. Para obtener más información sobre las clases derivadas de **\_ CIM CacheMemory**, vea [Clases win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Memoria \_ CIM**](cim-memory.md)
</dt> </dl>

 

