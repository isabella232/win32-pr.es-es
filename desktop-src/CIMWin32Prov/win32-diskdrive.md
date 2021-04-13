---
description: Representa una unidad de disco física tal como la muestra un equipo que ejecuta el sistema operativo Windows.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Clase Win32_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539141"
---
# <a name="win32_diskdrive-class"></a>\_Clase Win32 DiskDrive

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDrive de Win32** representa una unidad de disco física tal como la muestra un equipo que ejecuta el sistema operativo Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a>Miembros

La **clase \_ DiskDrive de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ DiskDrive** tiene estos métodos.



| Método            | Descripción                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reset**         | Sin implementar. Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ DiskDrive**](cim-diskdrive.md) para obtener documentación.<br/>                 |
| **SetPowerState** | Sin implementar. Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ DiskDrive**](cim-diskdrive.md) para obtener documentación.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ DiskDrive de Win32** tiene estas propiedades.

<dl> <dt>

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


</dt> <dd></dd> <dt>

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

El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)


</dt> <dd>

La unidad de disco no está disponible.

</dd> </dl>

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de \| [**\_ disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Número de bytes de cada sector para la unidad de disco físico.

Ejemplo: 512

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")
</dt> </dl>

Matriz de funcionalidades del dispositivo de acceso a medios. Por ejemplo, el dispositivo puede admitir el acceso aleatorio (3), el medio extraíble (7) y la limpieza automática (9).

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)


</dt> <dd>

Admite medios extraíbles

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)


</dt> <dd>

Admite medios Dual-Sided

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)


</dt> <dd>

Expulsión antes de desmontar la unidad no necesaria

</dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")
</dt> </dl>

Lista de explicaciones más detalladas para cualquiera de las características de dispositivos de acceso indicadas en la matriz de **funcionalidades** . Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Algoritmo o herramienta que usa el dispositivo para admitir la compresión. Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

Nombre del algoritmo de compresión o de uno de los valores siguientes.

<dt>



 ("Desconocido")


</dt> <dd>

Si el dispositivo admite capacidades de compresión o no, no se conoce.

</dd> <dt>



 ("Comprimido")


</dt> <dd>

El dispositivo admite capacidades de compresión, pero su esquema de compresión no se conoce o no se revela.

</dd> <dt>



 ("No comprimido")


</dt> <dd>

El dispositivo no admite la compresión.

</dd> </dl>

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

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño de bloque predeterminado, en bytes, para este dispositivo.

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Identificador único de la unidad de disco con otros dispositivos en el sistema.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

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

Tipo de detección y corrección de errores admitidos por este dispositivo.

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

</dd> <dt>

**FirmwareRevision**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| [**\_ \_ descriptor de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)de inesperados win32api de entrada y salida de dispositivo \| ProductRevisionOffset")
</dt> </dl>

Revisión para el firmware de la unidad de disco que asigna el fabricante.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Windows 95/98 Functions \| \_ \_ info Map info \| btInt13Unit")
</dt> </dl>

Número de unidad física de la unidad especificada. Esta propiedad se rellena con la estructura de [**\_ \_ número de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) devuelta desde el código de control [**\_ \_ obtener \_ \_ número de dispositivo de almacenamiento de ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) . Un valor de 0xFFFFFFFF indica que la unidad especificada no se asigna a una unidad física.

Ejemplo: 1

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**InterfaceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Device INPUT and Output Functions \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")
</dt> </dl>

Tipo de interfaz de la unidad de disco físico.

Los valores son:

SCSI

CÁMARAS

IDE

USB

1394

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

**Le**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ hardware máquina local \\ \\ \\ \\ DEVICEMAP \\ \\ SCSI SCSI puerto SCSI \\ \\ bus SCSI identificador identificador \\ \\ \\ \\ \\ \\ de unidad lógica \\ \\ ", "Win32Registry \| manufacturer")
</dt> </dl>

Nombre del fabricante de la unidad de disco.

Ejemplo: "Seagate"

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")
</dt> </dl>

Tamaño máximo del medio, en kilobytes, de los medios admitidos por este dispositivo.

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**MediaLoaded**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediatype \| FixedMedia")
</dt> </dl>

Si es **true**, se cargan los medios de una unidad de disco, lo que significa que el dispositivo tiene un sistema de archivos legible y es accesible. En el caso de las unidades de disco fijas, esta propiedad siempre será **true**.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediatype")
</dt> </dl>

Tipo de medio utilizado o al que este dispositivo tiene acceso.

Los valores posibles son:

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

**Medio de disco duro externo**


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

**Medios extraíbles** ("medios extraíbles distintos de disquete")


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

**Disco duro fijo** ("medio de disco duro fijo")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("el formato es desconocido")


</dt> <dd></dd> </dl>

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ hardware máquina local \\ \\ \\ \\ DEVICEMAP \\ \\ SCSI SCSI puerto SCSI \\ \\ bus SCSI identificador identificador \\ \\ \\ \\ \\ \\ de unidad lógica \\ \\ ", "Win32Registry \| ProductID")
</dt> </dl>

Número de modelo del fabricante de la unidad de disco.

Ejemplo: "ST32171W"

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, el dispositivo de acceso a medios necesita limpieza. Si la limpieza manual o automática es posible, se indica en la propiedad **Capabilities** .

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de elementos multimedia que se admiten o insertan (cuando el dispositivo de acceso a medios admite varios medios individuales).

Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).

</dd> <dt>

**Particiones**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \ \| [**\_ información de partición**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition")
</dt> </dl>

Número de particiones en esta unidad de disco físico que reconoce el sistema operativo.

Ejemplo: 2

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


</dt> <dd>

No se admiten capacidades relacionadas con la energía para este dispositivo.

</dd> <dt>

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

Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.). La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**SCSIBus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PathId")
</dt> </dl>

Número de bus SCSI de la unidad de disco.

Ejemplo: 0

</dd> <dt>

**SCSILogicalUnit**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras LUN de \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| ")
</dt> </dl>

Número de unidad lógica (LUN) SCSI de la unidad de disco.

Ejemplo: 0

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo de \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| númeroDePuerto")
</dt> </dl>

Número de puerto SCSI de la unidad de disco.

Ejemplo: 0

</dd> <dt>

**SCSITargetId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| TargetId")
</dt> </dl>

Número de identificador SCSI de la unidad de disco.

Ejemplo: 0

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")
</dt> </dl>

Número de sectores de cada pista para esta unidad de disco físico.

Ejemplo: 63

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| [**\_ \_ descriptor de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)de inesperados win32api de entrada y salida de dispositivo \| SerialNumberOffset")
</dt> </dl>

Número asignado por el fabricante para identificar el medio físico.

Ejemplo: WD-WM3493798728

</dd> <dt>

**Signature**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras firma de \| [**\_ \_ información de diseño de unidad**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| ")
</dt> </dl>

Identificación del disco. Esta propiedad se puede usar para identificar un recurso compartido.

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructura \| [**\_ geométrica del disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño de la unidad de disco. Se calcula multiplicando el número total de cilindros, pistas en cada cilindro, sectores de cada pista y bytes de cada sector.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Los valores son:

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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Valor de la propiedad **CreationClassName** del equipo de ámbito.

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

**TotalCylinders**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")
</dt> </dl>

Número total de cilindros en la unidad de disco físico. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

Ejemplo: 657

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TotalHeads**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")
</dt> </dl>

Número total de cabezas en la unidad de disco. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

</dd> <dt>

**TotalSectors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")
</dt> </dl>

Número total de sectores de la unidad de disco físico. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

Ejemplo: 2649024

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TotalTracks**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")
</dt> </dl>

Número total de pistas en la unidad de disco físico. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

Ejemplo: 42048

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")
</dt> </dl>

Número de pistas en cada cilindro de la unidad de disco físico. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

Ejemplo: 64

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las unidades de disco duro físico son el medio de almacenamiento principal para la información en cualquier entorno informático. Aunque las organizaciones suelen usar dispositivos como unidades de cinta y unidades de disco compacto para archivar datos, estos dispositivos no son adecuados para el almacenamiento diario de datos de usuario. Solo los discos duros físicos ofrecen la velocidad y la facilidad de uso necesaria para almacenar datos y para ejecutar aplicaciones y el sistema operativo.

Para administrar los datos de forma eficaz, es importante tener un inventario detallado de todos los discos físicos, sus capacidades y sus capacidades. Puede usar la clase **Win32 \_ DiskDrive** para derivar este tipo de inventario.

Cualquier interfaz a una unidad de disco físico de Windows es un descendiente (o miembro) de esta clase. Las características de la unidad de disco que se muestran a través de este objeto corresponden a las características lógicas y de administración de la unidad. En algunos casos, es posible que esto no refleje las características físicas reales del dispositivo. Cualquier objeto basado en otro dispositivo lógico no sería un miembro de esta clase.

Por motivos de seguridad, los usuarios que se conectan desde un equipo remoto deben tener el privilegio de **\_ \_ conexión SC Manager** habilitado para poder enumerar esta clase. Para obtener más información, consulte [seguridad del servicio y derechos de acceso](/windows/desktop/Services/service-security-and-access-rights).

La **clase \_ DiskDrive de Win32** se deriva [**de \_ DiskDrive de CIM**](cim-diskdrive.md) que deriva [**de \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md). La **clase \_ MediaAccessDevice de CIM** deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

## <a name="examples"></a>Ejemplos

El ejemplo de código de PowerShell [Informe de inventario de servidores-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) en la galería de TechNet usa una serie de clases, incluido **Win32 \_ DiskDrive**, para devolver información sobre el estado del servidor.

La [unidad de asignación a la letra de unidad con la \_ propiedad de tipo de interfaz DiskDrive de Win32](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) el ejemplo de código de PowerShell asigna una unidad a una letra de unidad.

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

[**\_DISKDRIVE CIM**](cim-diskdrive.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas de WMI: discos y sistemas de archivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

