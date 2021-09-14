---
description: Representa las capacidades y la capacidad de administración del controlador de vídeo en un sistema informático que ejecuta Windows.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Clase Win32_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974454"
---
# <a name="win32_videocontroller-class"></a>Clase VideoController de Win32 \_

La clase WMI **\_ VideoController** [de](../wmisdk/retrieving-a-class.md) Win32 representa las capacidades y la capacidad de administración del controlador de vídeo en un sistema informático que ejecuta Windows.

El hardware que no es compatible con Windows modelo de controlador de pantalla (WDDM) devuelve valores de propiedad inexactos para instancias de esta clase.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a>Members

La **clase \_ VideoController de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ VideoController de Win32** tiene estos métodos.



| Método            | Descripción                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reset**         | Sin implementar. Para implementar este método, vea el método [**Reset**](reset-method-in-class-cim-controller.md) en [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).<br/>                 |
| **SetPowerState** | Sin implementar. Para implementar este método, vea el [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ VideoController de Win32** tiene estas propiedades.

<dl> <dt>

**AcceleratorCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")
</dt> </dl>

Matriz de gráficos y funcionalidades 3D del controlador de vídeo.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acelerador de gráficos** (2)


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**Acelerador 3D** (3)


</dt> <dd>

Acelerador 3D

</dd> </dl>

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")
</dt> </dl>

Conjunto de chips general que se usa para que este controlador compare las compatibilidades con el sistema.

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation.DACType")
</dt> </dl>

Nombre o identificador del chip del convertidor digital a analógico (DAC). El juego de caracteres de esta propiedad es alfanumérico.

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation.MemorySize"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño de memoria del adaptador de vídeo.

Ejemplo: 64000

</dd> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
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


</dt> <dd>

Energía completa o en ejecución

</dd> <dt>

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


</dt> <dd>

Sin conexión

</dd> <dt>

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

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")
</dt> </dl>

Cadenas de forma libre que proporcionan explicaciones más detalladas de cualquiera de las características del acelerador de vídeo indicadas en la **matriz AcceleratorCapabilities.** Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz **AcceleratorCapabilities** que se encuentra en el mismo índice.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de contexto de dispositivo Win32API \| \| [**GetDeviceCaps")**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)
</dt> </dl>

Tamaño de la tabla de colores del sistema. El dispositivo debe tener una profundidad de color de no más de 8 bits por píxel; De lo contrario, esta propiedad no se establece.

Ejemplo: 256

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Código de error Administrador de configuración Win32.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

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

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows puede cargar el controlador para este dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.** (3)


</dt> <dd>

Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro podrían estar dañados.** (4)


</dt> <dd>

El dispositivo no funciona correctamente. Uno de sus controladores o el registro podrían estar dañados.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows puede administrar.** (5)


</dt> <dd>

El controlador del dispositivo requiere un recurso que Windows puede administrar.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**  (6)


</dt> <dd>

La configuración de arranque del dispositivo entra en conflicto con otros dispositivos.

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

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa incorrectamente de los recursos del dispositivo.** (9)


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

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos gratuitos que pueda usar.** (12)


</dt> <dd>

El dispositivo no puede encontrar suficientes recursos gratuitos para usarlos.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows puede comprobar los recursos de este dispositivo.** (13)


</dt> <dd>

Windows puede comprobar los recursos del dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.** (14)


</dt> <dd>

El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque probablemente haya un problema de nueva enumeración.** (15)


</dt> <dd>

El dispositivo no funciona correctamente debido a un posible problema de nueva enumeración.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows puede identificar todos los recursos que usa este dispositivo.** (16)


</dt> <dd>

Windows puede identificar todos los recursos que usa el dispositivo.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.** (17)


</dt> <dd>

El dispositivo solicita un tipo de recurso desconocido.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores de este dispositivo.** (18)


</dt> <dd>

Los controladores de dispositivos deben volver a instalarse.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.** (20)


</dt> <dd>

El Registro puede estar dañado.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador de este dispositivo. Si eso no funciona, consulte la documentación de hardware. Windows está quitando este dispositivo.** (21)


</dt> <dd>

Error del sistema. Si cambiar el controlador de dispositivo no es eficaz, consulte la documentación de hardware. Windows está quitando el dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.** (22)


</dt> <dd>

El dispositivo está deshabilitado.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador de este dispositivo. Si eso no funciona, consulte la documentación de hardware.** (23)


</dt> <dd>

Error del sistema. Si cambiar el controlador de dispositivo no es eficaz, consulte la documentación de hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.** (24)


</dt> <dd>

El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows está configurando este dispositivo.** (25)


</dt> <dd>

Windows está configurando el dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows está configurando este dispositivo.** (26)


</dt> <dd>

Windows está configurando el dispositivo.

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

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le ha dado los recursos necesarios.** (29)


</dt> <dd>

El dispositivo está deshabilitado. El firmware del dispositivo no proporcionaba los recursos necesarios.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.** (30)


</dt> <dd>

El dispositivo usa un recurso IRQ que está usando otro dispositivo.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows puede cargar los controladores necesarios para este dispositivo.** (31)


</dt> <dd>

El dispositivo no funciona correctamente. Windows cargar los controladores de dispositivo necesarios.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Si **es TRUE,** el dispositivo usa una configuración definida por el usuario.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de . Cuando se usa con las otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de esta clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**CurrentBitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.12"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bits")
</dt> </dl>

Número de bits usados para mostrar cada píxel.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**CurrentHorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.11"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("píxeles")
</dt> </dl>

Número actual de píxeles horizontales.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**CurrentNumberOfColors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de colores admitidos en la resolución actual.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**CurrentNumberOfColumns**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.14")
</dt> </dl>

Número de columnas para este controlador de vídeo (si está en modo de caracteres). En caso contrario, escriba 0 (cero).

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**CurrentNumberOfRows**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.13")
</dt> </dl>

Número de filas para este controlador de vídeo (si está en modo de caracteres). En caso contrario, escriba 0 (cero).

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**CurrentRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")
</dt> </dl>

Frecuencia con la que el controlador de vídeo actualiza la imagen del monitor. Un valor de 0 (cero) indica que se está utilizando la velocidad predeterminada, mientras que 0xFFFFFFFF indica que se está utilizando la velocidad óptima.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**CurrentScanMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.8")
</dt> </dl>

Modo de examen actual.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelazado** (3)


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**No entrelazado** (4)


</dt> <dd>

Sin entrelazado

</dd> </dl>

</dd> <dt>

**CurrentVerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.10"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("píxeles")
</dt> </dl>

Número actual de píxeles verticales.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificador (único para el sistema informático) para este controlador de vídeo.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de contexto de dispositivo Win32API \| \| [**GetDeviceCaps")**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)
</dt> </dl>

Número actual de lápices específicos del dispositivo. Un valor de 0xffff significa que el dispositivo no admite lápices.

Ejemplo: 3

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| EnumDisplaySettings")
</dt> </dl>

Otro tipo de controlador de vídeo. La propiedad puede ser uno de los valores predefinidos o un valor definido por el controlador mayor o igual que 256. Si se elige la dithering line art, el controlador usa un método de dithering que genera bordes bien definidos entre escalas de color negro, blanco y gris. El dithering de arte de línea no es adecuado para imágenes que incluyen continuas continuas en intensidad y matiz, como fotografías examinadas.

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

**Sin dithering** (1)


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

**Dithering with a coarse brush** (2)


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

**Dithering con un pincel fino** (3)


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

**Trama de arte de línea** (4)


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

**El dispositivo realiza el escalado gris** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ ")
</dt> </dl>

Fecha y hora de última modificación del controlador de vídeo instalado actualmente.

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de la biblioteca de instalación de archivos Win32API \| \| GetFileVersionInfo")
</dt> </dl>

Número de versión del controlador de vídeo.

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

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print Spooler Structures \| DevMode \| dmICMIntent")
</dt> </dl>

Valor específico de uno de los tres posibles métodos o intenciones de coincidencia de colores que se deben usar de forma predeterminada. Esta propiedad se usa principalmente para aplicaciones que no ICM aplicaciones. ICM aplicaciones establecen intenciones mediante las ICM de trabajo. Esta propiedad puede ser un valor predefinido o un valor definido por el controlador mayor o igual que 256. La coincidencia de colores basada en la saturación es la opción más adecuada para los gráficos de negocios cuando no se desea la dithering. La coincidencia de colores basada en el contraste es la opción más adecuada para imágenes exploradas o fotográficas cuando se desea el dithering. La coincidencia de colores optimizada para coincidir con el color exacto solicitado es más adecuada para su uso con logotipos empresariales u otras imágenes cuando se desea una coincidencia de color exacta.

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

**Saturación** (1)


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

**Contraste** (2)


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

**Color exacto** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print Spooler Structures \| DevMode \| dmICMMethod")
</dt> </dl>

Método de control de ICM. Para las aplicaciones que no ICM, esta propiedad determina si ICM está habilitado. Para ICM aplicaciones, el sistema examina esta propiedad para determinar cómo controlar ICM compatibilidad. Esta propiedad puede ser un valor predefinido o un valor definido por el controlador mayor o igual que 256. El valor determina qué sistema controla la coincidencia de colores de la imagen.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (1)


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

**Windows** (2)


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

**Controlador de dispositivo** (3)


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

**Dispositivo de destino** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Clase de control Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ \\ \\ \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")
</dt> </dl>

Ruta de acceso al archivo .inf del adaptador de vídeo.

Ejemplo: "C: \\ Windows \\ CONTROLADORES SYSTEM32" \\

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Clase de control Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ \\ \\ \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")
</dt> </dl>

Sección del archivo .inf donde reside la Windows de vídeo.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ ")
</dt> </dl>

Nombre del controlador de dispositivo para mostrar instalado.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último código de error notificado por el dispositivo lógico.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**MaxMemorySupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad máxima de memoria admitida en bytes.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Puerto de bus DMTF \| \| 001.9")
</dt> </dl>

Número máximo de entidades direccionables directamente compatibles con este controlador. Se debe usar un valor de 0 (cero) si se desconoce el número.

Esta propiedad se hereda del [**controlador CIM. \_**](cim-controller.md)

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")
</dt> </dl>

Frecuencia de actualización máxima del controlador de vídeo en hertz.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")
</dt> </dl>

Frecuencia de actualización mínima del controlador de vídeo en hertz.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**Monocromático**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Si **es TRUE,** se usa la escala de grises para mostrar imágenes.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, la propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NumberOfColorPlanes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número actual de planos de color. Si este valor no es aplicable a la configuración de vídeo actual, escriba 0 (cero).

Esta propiedad se hereda de [**CIM \_ PCVideoController.**](cim-pcvideocontroller.md)

</dd> <dt>

**NumberOfVideoPages**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Plug and Play identificador de dispositivo del dispositivo lógico.

Ejemplo: \* "PNP030b"

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de las funcionalidades específicas relacionadas con la energía de un dispositivo lógico.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

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

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía especificados automáticamente** (4)


</dt> <dd>

El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Se [**admite el método SetPowerState.**](setpowerstate-method-in-class-cim-controller.md) Este método se encuentra en la clase [**\_ logicalDevice**](cim-logicaldevice.md) de CIM primaria y se puede implementar. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling compatible** (6)


</dt> <dd>

El [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el *parámetro PowerState* establecido en 5 (Ciclo de energía).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Encendido con tiempo de encendido admitido** (7)


</dt> <dd>

Se admiten Power-On tiempo

El [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro  *PowerState* establecido en 5 (ciclo de energía) y el tiempo establecido en una fecha y hora específicas, o un intervalo, para el encendido.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** el dispositivo se puede administrar mediante energía (se puede poner en modo de suspensión, y así sucesivamente). La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de la administración de energía.

Esta propiedad se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

</dd> <dt>

**ProtocolSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Dmtf \| Bus Port \| 001.2", "MIF. Discos DMTF \| \| 003.3")
</dt> </dl>

Protocolo utilizado por el controlador para acceder a dispositivos "controlados".

Esta propiedad se hereda del [**controlador CIM. \_**](cim-controller.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span id="EISA"></span><span id="eisa"></span>**EISA** (3)


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span id="ISA"></span><span id="isa"></span>**ISA** (4)


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span id="PCI"></span><span id="pci"></span>**PCI** (5)


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)


</dt> <dd>

ATA o ATAPI

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Diskette flexible** (7)


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span id="1496"></span>**1496** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interfaz paralela SCSI** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocolo de Canal de fibra SCSI** (10)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocolo de bus serie SCSI** (11)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocolo de bus serie SCSI-2 (1394)** (12)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Arquitectura de Storage serie SCSI** (13)


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span id="VESA"></span><span id="vesa"></span>**VESA** (14)


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus serie universal** (16)


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocolo paralelo** (17)


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (18)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (19)


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span id="I2C"></span><span id="i2c"></span>**I2C** (20)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energía** (21)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span id="VME"></span><span id="vme"></span>**VME** (24)


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span id="IPI"></span><span id="ipi"></span>**IPI** (25)


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span id="RS232"></span><span id="rs232"></span>**RS232** (27)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>Anillo de token **IEEE 802.5** (33)


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span id="MCA"></span><span id="mca"></span>**MCA** (35)


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span id="IDE"></span><span id="ide"></span>**IDE** (37)


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span id="CMD"></span><span id="cmd"></span>**CMD** (38)


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span id="ST506"></span><span id="st506"></span>**ST506** (39)


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE mejorado** (42)


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span id="AGP"></span><span id="agp"></span>**AGP** (43)


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (44)**


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (temperatura rápida)** (45)


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**MR (serial detector)** (46)


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReservedSystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de contexto de dispositivo Win32API \| \| [**GetDeviceCaps")**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)
</dt> </dl>

Número de entradas reservadas en la paleta del sistema. El sistema operativo puede reservar entradas para admitir colores estándar para las barras de tareas y otros elementos de visualización de escritorio. Este índice solo es válido si el controlador de dispositivo establece el bit **RC \_ PALETTE** en el índice RASTERCAPS y solo está disponible si el controlador es compatible con el controlador de 16 Windows. Si el sistema no usa una paleta, **ReservedSystemPaletteEntries** no está establecido.

Ejemplo: 20

</dd> <dt>

**SpecificationVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Printing and Print Spooler Structures \| DevMode \| dmSpecVersion")
</dt> </dl>

Número de versión de la especificación de datos de inicialización (en la que se basa la estructura).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Entre los estados no operativo se incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

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

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


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

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Estado operativo DMTF \| \| 003.3")
</dt> </dl>

Estado del dispositivo lógico. Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (No aplicable).

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

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

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**Clave \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Valor de la propiedad **CreationClassName del** equipo de ámbito.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**Nombre**"), [**Clave \_ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre del sistema de ámbito.

Esta propiedad se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de contexto de dispositivo Win32API \| \| [**GetDeviceCaps")**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)
</dt> </dl>

Número actual de entradas de índice de color en la paleta del sistema. Este índice solo es válido si el controlador de dispositivo establece el bit **RC \_ PALETTE** en el índice RASTERCAPS y solo está disponible si el controlador es compatible con el controlador de 16 Windows. Si el sistema no usa una paleta, **SystemPaletteEntries** no está establecido.

Ejemplo: 20

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se restablecó por última vez este controlador. Esto podría significar que el controlador se ha apagado o reinicializado.

Esta propiedad se hereda del [**controlador CIM. \_**](cim-controller.md)

</dd> <dt>

**VideoArchitecture**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.2")
</dt> </dl>

Tipo de arquitectura de vídeo.

Esta propiedad se hereda de [**CIM \_ PCVideoController.**](cim-pcvideocontroller.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

**CGA** (3)


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

**EGA** (4)


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

**VGA** (5)


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

**SVGA** (6)


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

**MDA** (7)


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

**HGC** (8)


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

**MCGA** (9)


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

**8514A** (10)


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

**XGA** (11)


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

**Búfer de marco lineal** (12)


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (160)


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoMemoryType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.6")
</dt> </dl>

Tipo de memoria de vídeo.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

**VRAM** (3)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

**DRAM** (4)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

**SRAM** (5)


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

**WRAM** (6)


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

**EDO RAM** (7)


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

**DRAM sincrónica de ráfaga** (8)


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

**SRAM de ráfaga canalizada** (9)


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

**CDRAM** (10)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

**3DRAM** (11)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

**SDRAM** (12)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

**SGRAM** (13)


</dt> <dd></dd> </dl>

</dd> <dt>

**VideoMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Video \| 003.3")
</dt> </dl>

Modo de vídeo actual.

Esta propiedad se hereda de [**CIM \_ PCVideoController.**](cim-pcvideocontroller.md)

</dd> <dt>

**VideoModeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de contexto de dispositivo Win32API \| \| [**GetDeviceCaps")**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)
</dt> </dl>

Configuración actual de resolución, color y modo de examen del controlador de vídeo.

Ejemplo: "1024 x 768 x 256 colores"

</dd> <dt>

**VideoProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que describe el procesador de vídeo.

Esta propiedad se hereda de [**CIM \_ VideoController.**](cim-videocontroller.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ VideoController de Win32** se deriva de [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).

Para obtener más información sobre el uso de esta clase, como la recuperación de información de varios monitores, vea Usar PowerShell para detectar información [de varios monitores.](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)

## <a name="examples"></a>Ejemplos

En el [ejemplo de VBScript List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) (Enumerar propiedades del controlador de vídeo) se enumeran las propiedades del controlador de vídeo.

En el siguiente ejemplo de PowerShell se enumeran las propiedades del controlador de vídeo.


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
