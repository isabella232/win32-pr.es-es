---
description: Representa un sistema informático que ejecuta Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Clase Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6a2d965a764be8925fda55958302d815b62ad6180ce4d3abb48d399fc2e817
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700005"
---
# <a name="win32_computersystem-class"></a>Clase ComputerSystem de Win32 \_

La **clase WMI \_ ComputerSystem** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 representa un sistema informático que ejecuta Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a>Miembros

La **clase \_ ComputerSystem de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ComputerSystem de Win32** tiene estos métodos.



| Método                                                                                          | Descripción                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**JoinDomainOrWorkgroup**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | Agrega un sistema informático a un dominio o grupo de trabajo.<br/>                                                                                                                                                                                   |
| [**Renombrar**](rename-method-in-class-win32-computersystem.md)                                   | Cambia el nombre de un equipo local.<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | Sin implementar. Para obtener más información sobre cómo implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).<br/> |
| [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | Quita un sistema informático de un dominio o grupo de trabajo.<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>Propiedades

La **clase \_ ComputerSystem de Win32** tiene estas propiedades.

<dl> <dt>

**AdminPasswordStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Configuración \| AdminPasswordStatus")
</dt> </dl>

Configuración de seguridad de hardware del sistema para el estado de la contraseña de administrador.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**No implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticManagedPagefile**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Si **es True**, el sistema administra el archivo de página.

</dd> <dt>

**AutomaticResetBootOption**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE \_ \\ \\ SYSTEM \\ \\ CurrentControlSet Control \\ \\ \\ \\ CrashControl \| AutoReboot")
</dt> </dl>

Si **es True,** la opción de arranque de restablecimiento automático está habilitada.

</dd> <dt>

**AutomaticResetCapability**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Si **es True**, el restablecimiento automático está habilitado.

</dd> <dt>

**BootOptionOnLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("opción de arranque de funcionalidad de tipo SMBIOS \| 23 \| al \| límite")
</dt> </dl>

El límite de opciones de arranque es ON. Identifica la acción del sistema cuando se alcanza el valor **ResetLimit.**

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Sistema operativo** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Utilidades del** sistema (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**No reiniciar** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootOptionOnWatchDog**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("opción de arranque de funcionalidades de tipo SMBIOS \| 23") \| \|
</dt> </dl>

Tipo de acción de reinicio después de que transcurra el tiempo en el temporizador de control.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Sistema operativo** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Utilidades del** sistema (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

**No reiniciar** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootROMSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Si **es True**, indica si se admite una ROM de arranque.

</dd> <dt>

**BootStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 32 \| System Boot Information Boot \| Status")
</dt> </dl>

Campos Estado y Datos adicionales que identifican el estado de arranque.

Este valor procede del miembro **Estado de arranque** de la estructura Información de arranque **del** sistema en la información de SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.

</dd> <dt>

**BootupState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")
</dt> </dl>

Se ha iniciado el sistema. El arranque con errores omite los archivos de inicio del usuario también denominados SafeBoot.

La lista siguiente contiene los valores necesarios:

<dl> <dd>"Arranque normal"</dd> <dd>"Arranque con seguridad de errores"</dd> <dd>"Fail-safe with network boot"</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**Arranque normal** ("arranque normal")


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

**Arranque con errores** ("arranque seguro para errores")


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

**Fail-safe with network boot** ("Fail-safe with network boot")


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

Breve descripción del objeto de una cadena de una línea.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ChassisBootupState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estado de arranque del tipo SMBIOS \| \| 3")
</dt> </dl>

Estado de arranque del chasis.

Este valor procede del miembro **Boot-up State** de la estructura **System Enclosure o Chassis** en la información de SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Caja fuerte** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Advertencia** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**No recuperable** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**ChassisSKUNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 \| Chassis SKU \| Number")
</dt> </dl>

Número de SKU del chasis o del gabinete como una cadena.

Este valor procede del miembro **SKU Number** de la estructura System Enclosure **o Chassis en** la información de SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre de la primera clase concreta de la cadena de herencia de una instancia. Puede usar esta propiedad con otras propiedades de la clase para identificar todas las instancias de la clase y sus subclases.

Esta propiedad se hereda del [**sistema CIM. \_**](cim-system.md)

</dd> <dt>

**CurrentTimeZone**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Time Structures TIME ZONE INFORMATION \| [**\_ \_ Bias"),**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")
</dt> </dl>

Cantidad de tiempo que el sistema informático unitario se desplaza con respecto a la hora universal coordinada (UTC).

</dd> <dt>

**DaylightInEffect**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Funciones de tiempo de Win32API \| \| [**GetTimeZoneInformation")**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)
</dt> </dl>

Si **es True,** el modo de horario de verano es ON.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| GetComputerNameEx \| ComputerNameDnsHostname")
</dt> </dl>

Nombre del equipo local según el servidor de nombres de dominio (DNS).

</dd> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**WKSTA INFO \_ \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ langroup")
</dt> </dl>

Nombre del dominio al que pertenece un equipo.

> [!Note]  
> Si el equipo no forma parte de un dominio, se devuelve el nombre del grupo de trabajo.

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (Ds) Structures \| [**DSROLE PRIMARY DOMAIN INFO \_ \_ \_ \_ BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ MACHINE \_ ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| MachineRole")
</dt> </dl>

Rol de un equipo en un grupo de trabajo de dominio asignado. Un grupo de trabajo de dominio es una colección de equipos de la misma red. Por ejemplo, una **propiedad DomainRole** puede mostrar que un equipo es una estación de trabajo miembro.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**Estación de trabajo** independiente (0)


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**Estación de trabajo miembro** (1)


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**Servidor independiente** (2)


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**Servidor miembro** (3)


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**Controlador de dominio de copia de** seguridad (4)


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**Controlador de dominio principal** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**EnableDaylightSavingsTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Habilita el horario de verano (DST) en un equipo. Un valor true **indica** que la hora del sistema cambia a una hora por delante o por detrás cuando DST se inicia o finaliza. Un valor false **indica** que la hora del sistema no cambia a una hora por delante o por detrás cuando DST se inicia o finaliza. Un valor **NULL indica** que el estado de DST es desconocido en un sistema.

</dd> <dt>

**FrontPanelResetStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Configuración \| FrontPanelResetStatus")
</dt> </dl>

En la tabla siguiente se muestra la configuración de seguridad de hardware para el botón de restablecimiento en un equipo.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**No implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HypervisorPresent**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Si **es True**, existe un hipervisor.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 8 y Windows Server 2012.

</dd> <dt>

**DesatencionesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Si **es True,** existe un puerto de insonoridad (IR) en un sistema informático.

</dd> <dt>

**InitialLoadInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Datos necesarios para buscar el dispositivo de carga inicial o el servicio de arranque para solicitar que se inicie el sistema operativo.

Esta propiedad se hereda de [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

**Windows Server 2008 R2:** Esta propiedad está disponible, pero vacía.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

El objeto está instalado. Un objeto no necesita un valor para indicar que está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**KeyboardPasswordStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Configuración \| KeyboardPasswordStatus")
</dt> </dl>

Configuración de seguridad de hardware del sistema para El estado de la contraseña del teclado.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**No implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastLoadInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Entrada de matriz de **la propiedad InitialLoadInfo** que contiene los datos para iniciar el sistema operativo cargado.

Esta propiedad se hereda de [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 Información del sistema \| \| Manufacturer")
</dt> </dl>

Nombre de un fabricante del equipo.

Ejemplo: Adventure Works

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 Información del sistema Product \| \| Name")
</dt> </dl>

Nombre del producto que un fabricante proporciona a un equipo. Esta propiedad debe tener un valor .

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Clave de una [**instancia \_ del sistema CIM**](cim-system.md) en un entorno empresarial.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor de **nombre del** sistema del equipo que se genera automáticamente. El [**objeto \_ ComputerSystem**](cim-computersystem.md) de CIM y sus derivados son objetos de nivel superior del Modelo de información común (CIM). Proporcionan el ámbito de varios componentes. Se [**requieren \_ claves**](cim-system.md) únicas del sistema **CIM, \_** pero puede definir una heurística para crear el nombre del sistema del equipo CIM que genera el mismo nombre y es independiente del protocolo de detección. Esto evita problemas de inventario y administración cuando el mismo recurso o entidad se detecta varias veces, pero no se puede resolver en un objeto. Se recomienda usar una heurística, pero no es necesario.

La heurística se describe en la especificación del modelo común CIM V2 y se supone que las reglas documentadas se usan para determinar y asignar un nombre. La **lista de valores NameFormat** define el orden para asignar un nombre de sistema de equipo. Varias reglas se asignan al mismo valor.

El [**valor \_ cim computersystem name**](cim-computersystem.md) que se calcula mediante la heurística es el valor clave del sistema. Sin embargo, use alias para asignar un nombre diferente para **CIM \_ ComputerSystem,** que puede ser más único para su empresa.

Esta propiedad se hereda del [**sistema CIM. \_**](cim-system.md)

Los valores son los siguientes:

<dt>

<span id="IP"></span><span id="ip"></span>

**IP** ("IP")


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Dial** ("Dial")


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** ("HID")


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**NWA** ("NWA")


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**HWA** ("HWA")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("X25")


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** ("ISDN")


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** ("IPX")


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**DCC** ("DCC")


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E.164** ("E.164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** ("Otros")


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkServerModeEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures SERVER INFO \| [**\_ \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ type SV TYPE \| \_ \_ SERVER")
</dt> </dl>

Si **es True**, el modo de servidor de red está habilitado.

</dd> <dt>

**NumberOfLogicalProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Número de procesadores lógicos disponibles en el equipo.

Puede usar **NumberOfLogicalProcessors** y **NumberOfProcessors** para determinar si el equipo es hyperthreading. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Información del sistema Structures SYSTEM \| [**\_ INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")
</dt> </dl>

Número de procesadores físicos disponibles actualmente en un sistema. Este es el número de procesadores habilitados para un sistema, que no incluye los procesadores deshabilitados. Si un sistema informático tiene dos procesadores físicos cada uno que contiene dos procesadores lógicos, el valor de **NumberOfProcessors** es 2 y **NumberOfLogicalProcessors** es 4. Los procesadores pueden ser varios núcleos o pueden ser procesadores de hyperthreading. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

**OEMLogoBitmap**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Lista de datos de un mapa de bits que crea el fabricante de equipos originales (OEM).

</dd> <dt>

**OEMStringArray**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings ("cadenas**](/windows/desktop/WmiSdk/standard-qualifiers) OEM de tipo SMBIOS \| 11") \|
</dt> </dl>

Lista de cadenas de forma libre que define un OEM. Por ejemplo, un OEM define los números de pieza para los documentos de referencia del sistema, la información de contacto del fabricante, y así sucesivamente.

</dd> <dt>

**PartOfDomain**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Si **es True**, el equipo forma parte de un dominio. Si el valor es **NULL**, el equipo no está en un dominio o el estado es desconocido. Si quita el equipo de un dominio, el valor se convierte en **false.**

</dd> <dt>

**PauseAfterReset**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tiempo de espera de tipo SMBIOS \| 23"), \| [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")
</dt> </dl>

Retraso de tiempo antes de que se inicie un reinicio en milisegundos. Se usa después de un ciclo de energía del sistema, el restablecimiento del sistema local o remoto y el restablecimiento automático del sistema. Un valor de 1 (menos uno) indica que el valor de pausa es desconocido.

**Windows Vista:** Esta propiedad puede devolver un número desconocido.

</dd> <dt>

**PCSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Tipo de equipo en uso, como portátil, de escritorio o tableta.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Sin especificar** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Escritorio** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Móvil** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Estación de** trabajo (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Servidor SOHO** (5)


</dt> <dd>

Servidor Office y Office inicio (SOHO)

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC del dispositivo** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Servidor de rendimiento** (7)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**PCSystemTypeEx**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Tipo de equipo en uso, como portátil, de escritorio o tableta.

**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 8.1 y Windows Server 2012 R2.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**Sin especificar** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Escritorio** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

**Móvil** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

**Estación de** trabajo (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**Enterprise Server** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**Servidor SOHO** (5)


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**PC del dispositivo** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**Servidor de rendimiento** (7)


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

**Pizarra** (8)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Máximo** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Power Controls \| 001.2")
</dt> </dl>

Matriz de las funcionalidades específicas relacionadas con la energía de un dispositivo lógico.

Esta propiedad se hereda de **\_ CIM LogicalDevice.**

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

Se [**admite el método SetPowerState.**](setpowerstate-method-in-class-cim-controller.md) Este método se encuentra en la clase **\_ logicalDevice** de CIM primaria y se puede implementar. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling compatible** (6)


</dt> <dd>

El [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el *parámetro PowerState* establecido en 5 (Ciclo de energía).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Encendido con tiempo de encendido admitido** (7)


</dt> <dd>

Timed Power-On compatible

El [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro  *PowerState* establecido en 5 (ciclo de energía) y la hora establecida en una fecha y hora específicas, o un intervalo, para la encendido.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** el dispositivo se puede administrar mediante energía, por ejemplo, un dispositivo se puede poner en modo de suspensión, y así sucesivamente. Esta propiedad no indica que las características de administración de energía están habilitadas actualmente, pero indica que el dispositivo lógico es capaz de la administración de energía.

Esta propiedad se hereda de [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

</dd> <dt>

**PowerOnPasswordStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 24 \| Hardware Security Configuración \| PowerOnPasswordStatus")
</dt> </dl>

Configuración de seguridad de hardware del sistema para Power-On de contraseña.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**No implementado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de energía actual de un equipo y su sistema operativo asociado. Los estados de ahorro de energía tienen los siguientes valores: El valor 4 (desconocido) indica que se sabe que el sistema está en modo de ahorro de energía, pero se desconoce su estado exacto en este modo. 2 (modo de bajo consumo) indica que el sistema está en un estado de ahorro de energía, pero sigue funcionando y puede presentar un rendimiento degradado; 3 (En espera) indica que el sistema no funciona, pero se podría llevar a toda la energía rápidamente; y 7 (Advertencia) indica que el sistema del equipo está en estado de advertencia y en modo de ahorro de energía.

Esta propiedad se hereda de [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Energía completa** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Ahorro de energía: modo de bajo consumo** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Ahorro de energía: en espera** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Ahorro de energía: desconocido** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de** energía (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Apagado** (6)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Ahorro de energía: advertencia** (7)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Ahorro de energía: hibernación** (8)


</dt> <dd>

Hibernación de ahorro de energía.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Ahorro de energía: apagado flexible** (9)


</dt> <dd>

Ahorro de energía desactivado.

</dd> </dl>

</dd> <dt>

**PowerSupplyState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 System Enclosure or \| Chassis Power Supply \| State")
</dt> </dl>

Estado de la fuente de alimentación o de los suministros cuando se izó por última vez.

Este valor procede del miembro **Power Supply State** de la estructura System Enclosure o **Chassis en** la información de SMBIOS.

En la lista siguiente se identifican los valores de esta propiedad.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Caja fuerte** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Advertencia** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**No recuperable** (6)


</dt> <dd>

No recuperable

</dd> </dl>

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Información de contacto del propietario del sistema principal, por ejemplo, número de teléfono, dirección de correo electrónico, entre otros.

Esta propiedad se hereda del [**sistema CIM. \_**](cim-system.md)

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nombre del propietario del sistema principal.

Esta propiedad se hereda del [**sistema CIM. \_**](cim-system.md)

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Hardware Security \| 001.4")
</dt> </dl>

Si está habilitada, el valor es 4 y el sistema informático unitario se puede restablecer mediante los botones de encendido y restablecimiento. Si está deshabilitado, el valor es 3 y no se permite un restablecimiento.

Esta propiedad se hereda de [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**No implementado** (5)


</dt> <dd>

No recuperable

</dd> </dl>

</dd> <dt>

**ResetCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 23 \| System Reset Reset \| Count")
</dt> </dl>

Número de restablecimientos automáticos desde el último restablecimiento. Un valor de 1 (menos uno) indica que el recuento es desconocido.

</dd> <dt>

**ResetLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Límite de restablecimiento de restablecimiento del sistema de tipo SMBIOS \| 23") \| \|
</dt> </dl>

Número de veces consecutivas que se intenta restablecer el sistema. Un valor de 1 (menos uno) indica que el límite es desconocido.

</dd> <dt>

**Roles**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Lista que especifica los roles de un sistema en el entorno de tecnología de la información.

Esta propiedad se hereda del [**sistema CIM. \_**](cim-system.md)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Estado actual de un objeto.

Por Win32_ComputerSystem, el estado siempre es "Correcto".

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dl>

</dd> <dt>

**SupportContactDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Información de compatibilidad con Win32API \| [**GetPrivateProfileString")**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \|
</dt> </dl>

Lista de la información de contacto de soporte técnico para el Windows operativo.

</dd> <dt>

**SystemFamily**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 Información del sistema \| \| Family")
</dt> </dl>

Familia a la que pertenece un equipo determinado. Una familia hace referencia a un conjunto de equipos que son similares pero no idénticos desde un punto de vista de hardware o software.

Este valor procede del miembro **Family** de la **estructura Información del sistema** en la información de SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.

</dd> <dt>

**SystemSKUNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 Información del sistema SKU \| \| Number")
</dt> </dl>

Identifica una configuración de equipo determinada para su venta. A veces también se denomina identificador de producto o número de pedido de compra.

Este valor procede del miembro **SKU Number (Número** de SKU) de **la Información del sistema** estructura en la información de SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.

</dd> <dt>

**SystemStartupDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| Boot Loader \| timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")
</dt> </dl>

**SystemStartupDelay** ya no está disponible para su uso porque Boot.ini no se usa para configurar el inicio del sistema. En su lugar, use [las clases BCD](/previous-versions/windows/desktop/bcd/bcd-classes) proporcionadas por el proveedor WMI datos de la configuración de arranque (BCD) (BCD) o el **comando Bcdedit.**

</dd> <dt>

**SystemStartupOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sistemas operativos Win32API \| [**GetPrivateProfileSection")**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \|
</dt> </dl>

**SystemStartupOptions** ya no está disponible para su uso porque Boot.ini no se usa para configurar el inicio del sistema. En su lugar, use [las clases BCD](/previous-versions/windows/desktop/bcd/bcd-classes) proporcionadas por el proveedor WMI datos de la configuración de arranque (BCD) (BCD) o el **comando Bcdedit.**

</dd> <dt>

**SystemStartupSetting**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**SystemStartupSetting** ya no está disponible para su uso porque Boot.ini no se usa para configurar el inicio del sistema. En su lugar, use [las clases BCD](/previous-versions/windows/desktop/bcd/bcd-classes) proporcionadas por el proveedor WMI datos de la configuración de arranque (BCD) (BCD) o el **comando Bcdedit.**

</dd> <dt>

**SystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Información del sistema Structures SYSTEM \| [**\_ INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")
</dt> </dl>

Sistema que se ejecuta en Windows equipo basado en el servidor. Esta propiedad debe tener un valor .

En la lista siguiente se identifican algunos de los valores posibles para esta propiedad.

<dl> <dd>"PC basado en x64"</dd> <dd>"PC basado en X86"</dd> <dd>"PC basado en MIPS"</dd> <dd>"Equipo basado en alfa"</dd> <dd>"Power PC"</dd> <dd>"SH-x PC"</dd> <dd>"StrongARM PC"</dd> <dd>"PC Intel de 64 bits"</dd> <dd>"EQUIPO alfa de 64 bits"</dd> <dd>"Desconocido"</dd> <dd>"X86-Nec98 PC"</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**PC basado en X86** ("PC basado en X86")


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

**EQUIPO basado en MIPS** ("PC basado en MIPS")


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

**Equipo basado en alfa** ("PC basado en alfa")


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**Power PC** ("Power PC")


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**SH-x PC** ("SH-x PC")


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**StrongARM PC** ("StrongARM PC")


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**Equipo Intel de 64 bits** ("PC Intel de 64 bits")


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

**PC basado en x64** ("PC basado en x64")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**X86-Nec98 PC** ("X86-Nec98 PC")


</dt> <dd></dd> </dl>

</dd> <dt>

**Estado de la temperatura**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 3 System Enclosure or \| Chassis Thermal \| State")
</dt> </dl>

Estado térmico del sistema al arrancar por última vez.

Este valor procede del miembro **Estado térmico** de la estructura Del gabinete del sistema o **chasis** en la información de SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Caja fuerte** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Advertencia** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**No recuperable** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**TotalPhysicalMemory**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estructuras de administración de memoria de Win32API \| \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño total de la memoria física. Tenga en cuenta que, en algunas circunstancias, es posible que esta propiedad no devuelva un valor preciso para la memoria física. Por ejemplo, no es preciso si el BIOS usa parte de la memoria física. Para obtener un valor preciso, use la **propiedad Capacity** en [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) en su lugar.

Ejemplo: 67108864

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Información del sistema Functions \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")
</dt> </dl>

Nombre de un usuario que ha iniciado sesión actualmente. Esta propiedad debe tener un valor . En una sesión de terminal services, **UserName** devuelve el nombre del usuario que ha iniciado sesión en la consola, no el usuario que inició sesión durante la sesión de terminal Service.

Ejemplo: jeffsmith

</dd> <dt>

**WakeUpType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 Información del sistema \| \| Wake-up Type")
</dt> </dl>

Evento que hace que el sistema se encienda.

Este valor procede del miembro **Tipo de reactivación** de la **estructura Información del sistema** en la información de SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

**Temporizador de APM** (3)


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

**Anillo de módem** (4)


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**LAN Remote** (5)


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**Conmutador de** alimentación (6)


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PME \# de PCI** (7)


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**Alimentación de CA restaurada** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Nombre del grupo de trabajo para este equipo. Si el valor de la **propiedad PartOfDomain** es **False,** se devuelve el nombre del grupo de trabajo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para determinar el número total de instancias de procesador asociadas a un objeto de sistema de equipo, use la clase de [**asociación \_ ComputerSystemProcessor de Win32.**](win32-computersystemprocessor.md)

Una **instancia de \_ ComputerSystem win32** que tiene varios procesadores físicos tiene varias instancias de procesador [**Win32 \_**](win32-processor.md) asociadas. Si el valor de **NumberOfLogicalProcessors** es mayor que el valor de **NumberOfProcessors,** el sistema del equipo es un sistema de varios núcleos o tiene uno o varios procesadores habilitados para el hyperthreading. Para obtener más información, vea la **sección Propiedades NumberOfLogicalProcessors** y **NumberOfCores** y Comentarios en **Procesador Win32. \_**

La **clase \_ ComputerSystem de Win32** se deriva de [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código del Centro de [scripting](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) se usa El sistema de equipos **Win32 \_** para recuperar información de varios sistemas informáticos y mostrarla en una GUI.

Puede encontrar un script de ejemplo que obtiene datos del sistema operativo y del procesador de **Win32 \_ ComputerSystem**, [**Procesador Win32 \_**](win32-processor.md)y Sistema operativo [**Win32 \_**](win32-operatingsystem.md) en los ejemplos del [**tema Procesador Win32. \_**](win32-processor.md)

En el ejemplo de VBScript siguiente se describe cómo recuperar el nombre de dominio del equipo local de instancias de **\_ ComputerSystem de Win32.**


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



En el ejemplo de Perl siguiente se describe cómo recuperar el nombre del equipo local de las instancias de **\_ ComputerSystem de Win32.**


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



En el ejemplo de Perl siguiente se describe cómo recuperar el nombre de dominio DNS de la máquina local de las instancias de **\_ ComputerSystem de Win32.**


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Tareas wmi: cuentas y dominios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Tareas wmi: hardware del equipo](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[Tareas wmi: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

