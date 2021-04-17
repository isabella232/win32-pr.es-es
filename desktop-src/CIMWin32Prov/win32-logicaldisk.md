---
description: Representa un origen de datos que se resuelve en un dispositivo de almacenamiento local real en un equipo con Windows.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Win32_LogicalDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659359"
---
# <a name="win32_logicaldisk-class"></a>Win32 \_ LogicalDisk (clase)

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalDisk de Win32** representa un origen de datos que se resuelve en un dispositivo de almacenamiento local real en un equipo con Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a>Miembros

La clase **Win32 \_ LogicalDisk** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ LogicalDisk** tiene estos métodos.



| Método                                                                             | Descripción                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Emprende**](chkdsk-method-in-class-win32-logicaldisk.md)                         | Invoca la operación [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) en el disco.<br/>                                                                                                                    |
| [**ExcludeFromAutochk**](excludefromautochk-method-in-class-win32-logicaldisk.md) | Excluye los discos de la operación [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) que se ejecutarán en el siguiente reinicio.<br/>                                                                                      |
| **Reset**                                                                          | Sin implementar. Para obtener más información sobre cómo implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ LogicalDisk**](cim-logicaldisk.md) for Documentation.<br/> |
| [**ScheduleAutoChk**](scheduleautochk-method-in-class-win32-logicaldisk.md)       | Programa que se ejecute [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) en el siguiente reinicio si se ha establecido el bit de integridad.<br/>                                                                                |
| **SetPowerState**                                                                  | Sin implementar. Para obtener más información sobre cómo implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ LogicalDisk**](cim-logicaldisk.md).<br/>   |



 

### <a name="properties"></a>Propiedades

La clase **Win32 \_ LogicalDisk** tiene estas propiedades.

<dl> <dt>

**Acceder**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de acceso a medios disponible.

Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)


</dt> <dd>

Editable

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")
</dt> </dl>

Disponibilidad y estado del dispositivo.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)


</dt> <dd>

En ejecución o completa

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )


</dt> <dd>

Sin conexión

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)


</dt> <dd>

Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)


</dt> <dd>

El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)


</dt> <dd>

El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)


</dt> <dd>

El dispositivo está en un estado de advertencia, pero también en el modo de ahorro de energía.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)


</dt> <dd>

El dispositivo está en pausa.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)


</dt> <dd>

El dispositivo no está listo.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)


</dt> <dd>

El dispositivo no está configurado.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)


</dt> <dd>

El dispositivo está en silencio.

</dd> </dl>

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Tamaño, en bytes, de los bloques que forman esta extensión de almacenamiento. Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.

Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción del objeto de una cadena de una línea.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api ( \| funciones del sistema de archivos) \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ \_ Compressed")
</dt> </dl>

Si **es true**, el volumen lógico existe como una única entidad comprimida, como un volumen de DoubleSpace. Si se admite la compresión basada en archivos, como en NTFS, esta propiedad es **false**.

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Código de error de Windows Configuration Manager.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**  (0)


</dt> <dd>

El dispositivo funciona correctamente.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.** (1)


</dt> <dd>

El dispositivo no está configurado correctamente.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.** (3)


</dt> <dd>

Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.** (4)


</dt> <dd>

El dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.** (5)


</dt> <dd>

El controlador del dispositivo requiere un recurso que Windows no puede administrar.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**  (6)


</dt> <dd>

La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.** (8)


</dt> <dd>

Falta el cargador de controladores para el dispositivo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.** (9)


</dt> <dd>

El dispositivo no funciona correctamente. El firmware de control informa incorrectamente de los recursos del dispositivo.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.** (10)


</dt> <dd>

El dispositivo no se puede iniciar.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.** (11)


</dt> <dd>

Error en el dispositivo.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.** (12)


</dt> <dd>

El dispositivo no puede encontrar suficientes recursos disponibles para su uso.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.** (13)


</dt> <dd>

Windows no puede comprobar los recursos del dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.** (14)


</dt> <dd>

El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.** (15)


</dt> <dd>

El dispositivo no funciona correctamente debido a un posible problema de reenumeración.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.** (16)


</dt> <dd>

Windows no puede identificar todos los recursos que usa el dispositivo.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.** (17)


</dt> <dd>

El dispositivo está solicitando un tipo de recurso desconocido.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.** (18)


</dt> <dd>

Se deben volver a instalar los controladores de dispositivos.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.** (20)


</dt> <dd>

Es posible que el registro esté dañado.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.** (21)


</dt> <dd>

Error del sistema. Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware. Windows está quitando el dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.** (22)


</dt> <dd>

El dispositivo está deshabilitado.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.** (23)


</dt> <dd>

Error del sistema. Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.** (24)


</dt> <dd>

El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.** (25)


</dt> <dd>

Windows todavía está configurando el dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.** (26)


</dt> <dd>

Windows todavía está configurando el dispositivo.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.** (27)


</dt> <dd>

El dispositivo no tiene una configuración de registro válida.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.** (28)


</dt> <dd>

Los controladores de dispositivo no están instalados.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.** (29)


</dt> <dd>

El dispositivo está deshabilitado. El firmware del dispositivo no proporcionó los recursos necesarios.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.** (30)


</dt> <dd>

El dispositivo usa un recurso de IRQ que otro dispositivo está usando.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.** 31


</dt> <dd>

El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Si es **true**, el dispositivo usa una configuración definida por el usuario.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia. Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Identificador único del disco lógico desde otros dispositivos del sistema.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

Para obtener un ejemplo de código que recupera esta propiedad, vea la sección Comentarios, más adelante.

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| FileFunctions \| GetDriveType")
</dt> </dl>

Valor numérico que corresponde al tipo de unidad de disco que representa este disco lógico.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

**No hay directorio raíz** (1)


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

**Disco extraíble** (2)


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

**Disco local** (3)


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

**Unidad de red** (4)


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

**Disco compacto** (5)


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

**Disco RAM** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de detección y corrección de errores admitidos por esta extensión de almacenamiento.

Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).

</dd> <dt>

**Systems**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))
</dt> </dl>

Sistema de archivos en el disco lógico.

Ejemplo: "NTFS"

</dd> <dt>

**FreeSpace**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Espacio, en bytes, disponible en el disco lógico.

Esta propiedad se hereda del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último código de error indicado por el dispositivo lógico.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**MaximumComponentLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))
</dt> </dl>

Longitud máxima de un componente de nombre de archivo compatible con la unidad de Windows. Un componente de nombre de archivo es la parte de un nombre de archivo entre barras diagonales inversas. El valor se puede usar para indicar que el sistema de archivos especificado admite nombres largos. Por ejemplo, para un sistema de archivos FAT que admite nombres largos, la función almacena el valor 255, en lugar del indicador 8,3 anterior. También se pueden admitir nombres largos en los sistemas que usan el sistema de archivos NTFS.

Ejemplo: 255

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Device INPUT and Output Functions \| DeviceIoControl")
</dt> </dl>

Tipo de medio actualmente presente en la unidad lógica. Este valor será uno de los valores de la \_ enumeración de tipo de medio definido en Winioctl. h. Es posible que el valor no sea exacto para unidades extraíbles si actualmente no hay ningún medio en la unidad.

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>El **formato es desconocido** (0)


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (1)


</dt> <dd>

Disquete de 5 1/2 pulgadas; 1,2 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (2)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 1,44 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (3)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 2,88 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (4)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 20,8 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (5)


</dt> <dd>

Disquete de 3 1/2 pulgadas-720 KB-512 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (6)


</dt> <dd>

Disquete de 5 1/2 pulgadas-360 KB-512 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (7)


</dt> <dd>

Disquete de 5 1/2 pulgadas-320 KB-512 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (8)


</dt> <dd>

Disquete de 5 1/2 pulgadas-320 KB-1024 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (9)


</dt> <dd>

Disquete de 5 1/2 pulgadas-180 KB-512 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (10)


</dt> <dd>

Disquete de 5 1/2 pulgadas-160 KB-512 bytes/sector

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Medio extraíble distinto de disquete** (11)


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Medio de disco duro fijo** (12)


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (13)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 120 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (14)


</dt> <dd>

Disquete de 3 1/2 pulgadas-640 KB-512 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (15)


</dt> <dd>

Disquete de 5 1/2 pulgadas-640 KB-512 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (16)


</dt> <dd>

Disquete de 5 1/2 pulgadas-720 KB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (17)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 1,2 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (18)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 1,23 MB-1024 bytes/sector

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (19)


</dt> <dd>

Disquete de 5 1/2 pulgadas; 1,23 MB-1024 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (20)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 128 MB-512 bytes/sector

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (21)


</dt> <dd>

Disquete de 3 1/2 pulgadas; 230 MB-512 bytes/sector

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**disquete de 8 pulgadas** (22)


</dt> <dd>

Disquete de 8 pulgadas-256 KB-128 bytes/sector

</dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")
</dt> </dl>

Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento. El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad. Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.

Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

Ejemplo: " \* PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.

Esta propiedad se hereda del **\_ LogicalDevice de CIM**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)


</dt> <dd>

Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)


</dt> <dd>

El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)


</dt> <dd>

Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar. Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)


</dt> <dd>

El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)


</dt> <dd>

Power-On de tiempo admitido

El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.). Esta propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| funciones de red de Windows \| WNetGetConnection")
</dt> </dl>

Ruta de acceso de red al dispositivo lógico.

</dd> <dt>

**Propósito**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que describe el medio y su uso.

Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).

</dd> <dt>

**QuotasDisabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica que la administración de cuotas no está habilitada (TRUE) en este sistema.

</dd> <dt>

**QuotasIncomplete**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica que se ha utilizado la administración de cuotas pero se ha deshabilitado (**true**). Incompleto hace referencia a la información que queda en el sistema de archivos una vez deshabilitada la administración de cuotas.

</dd> <dt>

**QuotasRebuilding**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, indica que el sistema de archivos está en el proceso activo de compilar información y configurar el disco para la administración de cuotas.

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño de la unidad de disco.

Esta propiedad se hereda del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md).

Para obtener un ejemplo de código que recupera esta propiedad, vea la sección Comentarios, más adelante.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** ("Aceptar")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred FAIL** ("Pred FAIL")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detener** ("detener")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

Con **estrés** ("acentuado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Recover** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicación perdida** ("pérdida de comunicación")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")
</dt> </dl>

Estado del dispositivo lógico. Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


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

**SupportsDiskQuotas**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, este volumen admite cuotas de disco.

</dd> <dt>

**SupportsFileBasedCompression**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ file \_ compression")
</dt> </dl>

Si es **true**, la partición de disco lógico admite la compresión basada en archivos, como es el caso del sistema de archivos NTFS. Esta propiedad es **false** cuando la propiedad **Compressed** es **true**.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Valor de la propiedad de ámbito de equipo de **CreationClassName** .

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre del sistema de ámbito.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**VolumeDirty**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL \_ está \_ sucio por volumen \_ ")
</dt> </dl>

Si **es true**, el disco requiere que [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) se ejecute en el siguiente reinicio. Esta propiedad solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo. No es aplicable a las unidades lógicas asignadas.

</dd> <dt>

**VolumeName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))
</dt> </dl>

Nombre del volumen del disco lógico.

Restricciones: máximo 32 caracteres.

Para obtener un ejemplo de código que recupera esta propiedad, vea la sección Comentarios, más adelante.

</dd> <dt>

**VolumeSerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))
</dt> </dl>

Número de serie del volumen del disco lógico.

Restricciones: máximo de 11 caracteres.

Ejemplo: "A8C3-D032"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **Win32 \_ LogicalDisk** se deriva del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) que deriva de [**CIM \_ StorageExtent**](cim-storageextent.md). La **clase \_ StorageExtent de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

Una unidad de disco física es la piedra angular de cualquier sistema de administración de almacenamiento. Sin embargo, una vez instalada una unidad de disco física, ni los usuarios ni los administradores del sistema suelen tratar directamente con el hardware. En su lugar, los usuarios y los administradores del sistema interactúan con las unidades lógicas que se han creado en el disco.

Una unidad lógica es una subdivisión de una partición a la que se le ha asignado su propia letra de unidad. (Es posible tener una partición a la que no se le haya asignado una letra de unidad). Al hablar acerca de la unidad C o D, se hace referencia a una unidad lógica en lugar de a una unidad de disco físico. Del mismo modo, al guardar un documento en la unidad E, lo guarda en la unidad lógica. Los discos físicos componen el hardware que conforma una unidad, incluidos tales componentes como cabezales, sectores y cilindros. Por el contrario, las unidades lógicas tienen propiedades como el espacio en disco, el espacio disponible en disco y las letras de unidad.

> [!Note]  
> La clase **Win32 \_ LogicalDisk** solo se puede usar para enumerar las propiedades de las unidades de disco locales. Sin embargo, puede usar la clase [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md) para enumerar las propiedades de las unidades de red asignadas.

 

## <a name="examples"></a>Ejemplos

Puede encontrar otros ejemplos con el **\_ LogicalDisk de Win32** para obtener datos de disco o volumen en el tema [tareas de WMI: discos y sistemas de archivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .

El ejemplo de código VBScript del administrador de [información WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la galería de TechNet utiliza la clase **Win32 \_ LogicalDisk** para recuperar información de hardware de varios equipos remotos.

La [información de obtención de disco mediante WMI/CIM..](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) . En el ejemplo de código de PowerShell de la galería de TechNet se usa el **\_ LogicalDisk de Win32** para recuperar **DeviceID**, **NombreDeVolumen** y **el tamaño** de un dispositivo de destino. En concreto, este ejemplo incluye un control riguroso de las excepciones y devuelve un solo objeto por equipo, en lugar de por disco.

El scripting empresarial suele implicar la configuración de hardware y software en equipos remotos. a su vez, esto requiere que sepa, de antemano, el tipo de unidades de disco instaladas en un equipo. Por ejemplo, un script que instala una aplicación en la unidad E solo funciona si la unidad E es un disco duro. Si la unidad E representa un disquete o una unidad de CD-ROM, el script produce un error. En el código siguiente se identifican las unidades y los tipos de unidad instalados en un equipo


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





Los ejemplos siguientes enumeran el espacio disponible en todas las unidades de disco duro de un equipo.


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





En el ejemplo de código siguiente se devuelve el tipo de sistema de archivos (FAT, NTFS, FAT32, etc.) que se usa en cada unidad de un equipo.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





El siguiente ejemplo de código de PowerShell recupera información adicional sobre los discos locales lógicos.


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDisk de CIM \_**](cim-logicaldisk.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas de WMI: discos y sistemas de archivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

