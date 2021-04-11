---
description: Representa un dispositivo conectado a un equipo que se ejecuta en un sistema operativo Microsoft Windows y que puede generar una imagen impresa o texto en papel o en otro medio.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Clase Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274968"
---
# <a name="win32_printer-class"></a>\_Clase Printer de Win32

La [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ impresora de Win32** representa un dispositivo conectado a un equipo que se ejecuta en un sistema operativo Microsoft Windows y que puede generar una imagen impresa o texto en papel o en otro medio.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a>Miembros

La **clase \_ Printer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ Printer de Win32** tiene estos métodos.



| Método                                                                               | Descripción                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddPrinterConnection**](addprinterconnection-method-in-class-win32-printer.md)   | Agrega una conexión a la impresora.<br/>                                                                                                                                                                      |
| [**CancelAllJobs**](cancelalljobs-method-in-class-win32-printer.md)                 | Cancela todos los trabajos.<br/>                                                                                                                                                                                      |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-printer.md) | Devuelve el descriptor de seguridad que controla el acceso a la impresora.<br/>                                                                                                                                   |
| [**Pausar**](pause-method-in-class-win32-printer.md)                                 | Pone en pausa la cola de impresión.<br/>                                                                                                                                                                                |
| [**PrintTestPage**](printtestpage-method-in-class-win32-printer.md)                 | Imprime una página de prueba.<br/>                                                                                                                                                                                    |
| [**RenamePrinter**](renameprinter-method-in-class-win32-printer.md)                 | Cambia el nombre de una impresora.<br/>                                                                                                                                                                                     |
| **Reset**                                                                            | Sin implementar. Para obtener más información sobre cómo implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**la \_ impresora CIM**](cim-printer.md).<br/>                 |
| [**Reanudar**](resume-method-in-class-win32-printer.md)                               | Reanuda la cola de impresión en pausa.<br/>                                                                                                                                                                            |
| [**SetDefaultPrinter**](setdefaultprinter-method-in-class-win32-printer.md)         | Establece la impresora predeterminada.<br/>                                                                                                                                                                              |
| **SetPowerState**                                                                    | Sin implementar. Para obtener más información sobre cómo implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**la \_ impresora CIM**](cim-printer.md).<br/> |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-printer.md) | Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora.<br/>                                                                                                              |



 

### <a name="properties"></a>Propiedades

La **clase \_ Printer de Win32** tiene estas propiedades.

<dl> <dt>

**Atributos**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mapa de bits de atributos para un dispositivo de impresión basado en Windows.

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Impresora \_ de ATRIBUTO \_ en cola** (1 (0x1))


</dt> <dd>

En cola

Los trabajos de impresión se almacenan en búfer y se ponen en cola.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Impresora \_ de ATTRIBUTE \_ Direct** (2 (0X2))


</dt> <dd>

Directo

Documento que se va a enviar directamente a la impresora. Este valor se usa si los trabajos de impresión no se ponen en cola correctamente.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Impresora \_ de ATRIBUTO \_ predeterminado** (4 (0x4))


</dt> <dd>

Valor predeterminado

Impresora predeterminada en un equipo.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Impresora \_ de ATTRIBUTE \_ Shared** (8 (0x8))


</dt> <dd>

Compartido

Disponible como recurso compartido de red.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Impresora \_ de \_Red de atributos** (16 (0x10))


</dt> <dd>

Red

Conectado a una red. Si se establecen los bits locales y de red, indica una impresora de red.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Impresora \_ de ATRIBUTO \_ Hidden** (32 (0x20))


</dt> <dd>

Hidden

Oculta de algunos usuarios de la red.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Impresora \_ de ATRIBUTO \_ local** (64 (0x40))


</dt> <dd>

Local

Conectado directamente a un equipo. Si se establecen los bits locales y de red, indica una impresora de red.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Impresora \_ de ATTRIBUTE \_ ENABLEDEVQ** (128 (0x80))


</dt> <dd>

EnableDevQ

Habilite la cola en la impresora, si está disponible.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Impresora \_ de \_KEEPPRINTEDJOBS de atributo** 256 (0x100))


</dt> <dd>

KeepPrintedJobs

El administrador de trabajos de impresión no debe eliminar los documentos una vez impresos.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Impresora \_ de El atributo se \_ \_ completa \_ primero** (512 (0x200))


</dt> <dd>

DoCompleteFirst

Inicie los trabajos que han terminado de poner en cola primero.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Impresora \_ de El atributo \_ funciona \_ sin conexión** (1024 (0x400))


</dt> <dd>

WorkOffline

Poner en cola los trabajos de impresión cuando una impresora no está disponible.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Impresora \_ de El atributo \_ habilita \_ BIDI** (2048 (0x800))


</dt> <dd>

EnableBIDI

Habilitar la impresión bidireccional.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Impresora \_ de ATRIBUTO \_ \_ solo sin formato** (4096 (0x1000))


</dt> <dd>

Permita que solo se pongan en cola los trabajos de tipo de datos sin procesar.

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Impresora \_ de ATRIBUTO \_ publicado** (8192 (0x2000))


</dt> <dd>

Publicado

Publicado en el servicio de directorio de red.

</dd> </dl>

</dd> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")
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

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredJobSheets")
</dt> </dl>

Matriz de todas las hojas de trabajo disponibles en una impresora. También se puede usar para describir el banner que una impresora puede proporcionar al principio de cada trabajo, u otras opciones especificadas por el usuario.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**AveragePagesPerMinute**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tasa de impresión, en promedio de páginas por minuto, que una impresora puede producir resultados.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ impresora CIM**](cim-printer.md). CapabilityDescriptions "," CIM \_ PrintJob. Finishing "," CIM \_ PrintService. Capabilities ")
</dt> </dl>

Matriz de capacidades de impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)


</dt> <dd>

Two-Sided borde largo

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)


</dt> <dd>

Two-Sided borde corto

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ impresora CIM**](cim-printer.md).**Funcionalidades**")
</dt> </dl>

Matriz de cadenas de formato libre que proporcionan explicaciones detalladas para las características de impresora indicadas en la matriz de **capacidades** . Cada entrada de esta matriz se relaciona con una entrada de la matriz de **capacidades** que se encuentra en el mismo índice.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción de un objeto: una cadena de una línea.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. charset"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")
</dt> </dl>

Matriz de juegos de caracteres disponibles para la salida. Las cadenas proporcionadas en esta propiedad deben cumplir la semántica y la sintaxis que se especifican en la sección 4.1.2 ("charset Parameters") en RFC 2046 (MIME parte 2) y contenidas en el registro de juegos de caracteres de IANA. Algunos ejemplos son "UTF-8", "US-ASCII" y "ISO-8859-1".

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**Comentario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Comentario para una cola de impresión.

Ejemplo: impresora de color

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Código de error de Configuration Manager de Win32.

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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
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

Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada para crear una instancia. Cuando se usa con otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**Funcionalidades**")
</dt> </dl>

Matriz de funciones de impresora que se usan actualmente. También debe aparecer una entrada en esta propiedad en la matriz de **capacidades** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)


</dt> <dd>

Two-Sided borde largo

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)


</dt> <dd>

Two-Sided borde corto

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**CharSetsSupported**")
</dt> </dl>

Juego de caracteres que se usa actualmente para la salida. Las cadenas proporcionadas en esta propiedad deben cumplir la semántica y la sintaxis que se especifican en la sección 4.1.2 ("charset Parameters") en RFC 2046 (MIME parte 2) y contenidas en el registro de juegos de caracteres de IANA. Entre los ejemplos se incluyen "UTF-8", "US-ASCII" e ISO-8859-1.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). LanguagesSupported ","**\_ impresora CIM**.**CurrentMimeType**")
</dt> </dl>

Idioma de la impresora que se usa actualmente. El lenguaje utilizado debe aparecer en la propiedad **LanguagesSupported** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPD** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Datos de línea** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**Wps** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simple** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**Impress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automática** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lip** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Mayúsculas** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Pantallas LCD** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**Dices** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**CurrentLanguage**")
</dt> </dl>

Tipo MIME que se está usando actualmente si **CurrentLanguage** es un tipo MIME (valor = 47).

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**NaturalLanguagesSupported**")
</dt> </dl>

Idioma que la impresora utiliza para la administración actualmente. El idioma que se muestra aquí también debe aparecer en la propiedad **NaturalLanguagesSupported** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Tipo de papel que está usando la impresora. Se debe expresar en el formato especificado por la aplicación de impresión de documentos ISO/IEC 10175 (DPA), que se resume en el Apéndice C de RFC 1759 (Printer MIB).

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**Valor predeterminado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, la impresora es la impresora predeterminada.

</dd> <dt>

**DefaultCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**Funcionalidades**")
</dt> </dl>

Matriz de las funciones de impresora utilizadas de forma predeterminada. Cada entrada de la matriz **DefaultCapabilities** también debe aparecer en la matriz **Capabilities** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)


</dt> <dd>

One-Sided

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)


</dt> <dd>

Two-Sided borde largo

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)


</dt> <dd>

Two-Sided borde corto

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**DefaultCopies**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de copias producidas para un trabajo, a menos que se especifique lo contrario.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). LanguagesSupported ","**\_ impresora CIM**.**DefaultMimeType**")
</dt> </dl>

Idioma de impresora predeterminado. El idioma que se muestra aquí también debe aparecer en la propiedad **LanguagesSupported** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPD** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Datos de línea** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**Wps** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simple** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**Impress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automática** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lip** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Mayúsculas** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Pantallas LCD** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**Dices** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

48
</dt> <dd>

XPS

</dd> <dt>

49
</dt> <dd>

HPGL2

</dd> <dt>

50
</dt> <dd>

PCLXL

</dd> </dl>

</dd> <dt>

**DefaultMimeType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**DefaultLanguage**")
</dt> </dl>

Tipo MIME que se está usando actualmente, si el valor **DefaultLanguage** es un tipo MIME (valor = 47).

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de páginas de secuencia de impresión que la impresora representa en una hoja de medios, a menos que un trabajo especifique lo contrario.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**DefaultPaperType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**PaperTypesAvailable**")
</dt> </dl>

Tipo de papel que utiliza la impresora, a menos que un trabajo de impresión especifique un tipo de papel diferente. La cadena se debe expresar en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 1017, que se resume en el Apéndice C de [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**DefaultPriority**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Valor de prioridad predeterminado asignado a cada trabajo de impresión.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")
</dt> </dl>

Descripción de un objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")
</dt> </dl>

Información de error de la impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

**Sin errores** (2)


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

**Papel bajo** (3)


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

**Sin papel** (4)


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

**Tóner bajo** (5)


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

**Sin tóner** (6)


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

**Puerta abierta** (7)


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

**Atascado** (8)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Sin conexión** (9)


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

**Servicio solicitado** (10)


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

**Bandeja de salida llena** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Identificador único de la impresora en un sistema.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**Direct**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, el trabajo de impresión se envía directamente a la impresora. Si es **false**, el trabajo de impresión se pone en cola.

</dd> <dt>

**DoCompleteFirst**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, la impresora inicia los trabajos que han terminado de poner en cola. Si **es false**, la impresora inicia los trabajos en el orden en que se reciben los trabajos.

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre del controlador de impresora de Windows.

Ejemplo: controlador de fax de Windows

</dd> <dt>

**EnableBIDI**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, la impresora puede imprimir bidireccionalmente.

</dd> <dt>

**EnableDevQueryPrint**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, la impresora contiene documentos en la cola cuando las configuraciones de documento e impresora no coinciden.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, se ha borrado el error comunicado en **LastErrorCode** .

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**DetectedErrorState**")
</dt> </dl>

Matriz de información complementaria para el estado de error actual indicado en **DetectedErrorState**.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**ExtendedDetectedErrorState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Notifica información de error estándar. Se debe registrar información adicional en **DetectedErrorState**.

Los valores son:

<dt>

0 (0X0)
</dt> <dd>

Unknown

</dd> <dt>

1 (0x1)
</dt> <dd>

Otros

</dd> <dt>

2 (0X2)
</dt> <dd>

Sin errores

</dd> <dt>

3 (0X3)
</dt> <dd>

Falta papel

</dd> <dt>

4 (0x4)
</dt> <dd>

No hay papel

</dd> <dt>

5 (0X5)
</dt> <dd>

Falta tóner

</dd> <dt>

6 (0x6)
</dt> <dd>

Sin tóner

</dd> <dt>

7 (0X7)
</dt> <dd>

Puerta abierta

</dd> <dt>

8 (0x8)
</dt> <dd>

Papel atascado

</dd> <dt>

9 (0x9)
</dt> <dd>

Servicio solicitado

</dd> <dt>

10 (0xA)
</dt> <dd>

Bandeja de salida llena

</dd> <dt>

11 (0xB)
</dt> <dd>

Problema de papel

</dd> <dt>

12 (0xC)
</dt> <dd>

No se puede imprimir la página

</dd> <dt>

13 (0xD)
</dt> <dd>

Intervención del usuario requerida

</dd> <dt>

14 (0xE)
</dt> <dd>

Memoria insuficiente

</dd> <dt>

15 (0xF)
</dt> <dd>

Servidor desconocido

</dd> </dl>

</dd> <dt>

**ExtendedPrinterStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Información de estado de una impresora diferente de la especificada en la propiedad **Availability** .

<dt>

1 (0x1)
</dt> <dd>

Otros

</dd> <dt>

2 (0X2)
</dt> <dd>

Unknown

</dd> <dt>

3 (0X3)
</dt> <dd>

Inactivo

</dd> <dt>

4 (0x4)
</dt> <dd>

Impresión

</dd> <dt>

5 (0X5)
</dt> <dd>

Preparando

</dd> <dt>

6 (0x6)
</dt> <dd>

Impresión detenida

</dd> <dt>

7
</dt> <dd>

Sin conexión

</dd> <dt>

8 (0x8)
</dt> <dd>

En pausa

</dd> <dt>

9 (0x9)
</dt> <dd>

Error

</dd> <dt>

10 (0xA)
</dt> <dd>

Ocupado

</dd> <dt>

11 (0xB)
</dt> <dd>

No disponible

</dd> <dt>

12 (0xC)
</dt> <dd>

En espera

</dd> <dt>

13 (0xD)
</dt> <dd>

Processing

</dd> <dt>

14 (0xE)
</dt> <dd>

Inicialización

</dd> <dt>

15
</dt> <dd>

Ahorro de energía

</dd> <dt>

16 (0x10)
</dt> <dd>

Eliminación pendiente

</dd> <dt>

17 (0x11)
</dt> <dd>

E/s activa

</dd> <dt>

18 (0X12)
</dt> <dd>

Alimentación manual

</dd> </dl>

</dd> <dt>

**Oculto**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, la impresora está oculta para los usuarios de la red.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](../wmisdk/standard-qualifiers.md) ("píxeles por pulgada")
</dt> </dl>

Resolución horizontal de la impresora, en píxeles por pulgada.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")
</dt> </dl>

Fecha y hora en que se instaló un objeto. El objeto se puede instalar sin que se escriba un valor en esta propiedad. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **contador**
</dt> </dl>

Número de trabajos de impresión desde la última vez que se restableció la impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**KeepPrintedJobs**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el administrador de trabajos de impresión no elimina los trabajos completados.

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ PrintService. LanguagesSupported ")
</dt> </dl>

Matriz de los idiomas de impresión admitidos de forma nativa.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span id="PCL"></span><span id="pcl"></span>**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span id="PJL"></span><span id="pjl"></span>**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span id="PS"></span><span id="ps"></span>**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span id="IPDS"></span><span id="ipds"></span>**IPD** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Datos de línea** (15)


</dt> <dd>

LineData

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span id="MODCA"></span><span id="modca"></span>**MODCA** (16)


</dt> <dd>

DODCA

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span id="REGIS"></span><span id="regis"></span>**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span id="SCS"></span><span id="scs"></span>**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span id="PDS"></span><span id="pds"></span>**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span id="IGP"></span><span id="igp"></span>**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span id="WPS"></span><span id="wps"></span>**Wps** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span id="LN03"></span><span id="ln03"></span>**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span id="QUIC"></span><span id="quic"></span>**QUIC** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simple** (31)


</dt> <dd>

SimpleText

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span id="NPAP"></span><span id="npap"></span>**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span id="DOC"></span><span id="doc"></span>**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**Impress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automática** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span id="LIPS"></span><span id="lips"></span>**Lip** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Mayúsculas** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span id="EXCL"></span><span id="excl"></span>**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span id="LCDS"></span><span id="lcds"></span>**Pantallas LCD** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span id="XES"></span><span id="xes"></span>**Dices** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span id="MIME"></span><span id="mime"></span>**MIME** (47)


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span id="XPS"></span><span id="xps"></span>**XPS** (48)


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último código de error que el dispositivo lógico informa.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**Local**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, la impresora no está conectada a una red. Si las propiedades **local** y de **red** están establecidas en **true**, la impresora es una impresora de red.

</dd> <dt>

**Ubicación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Ubicación física de la impresora.

Ejemplo: Bldg. 38, habitación 1164

</dd> <dt>

**MarkingTechnology**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")
</dt> </dl>

Tecnología de marcado que utiliza la impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

**LED electrográfico** (3)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

**Láser electrográfico** (4)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

**Otra fotografía** (5)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

**Impacto** de la matriz de puntos de encabezado de movimiento


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

**24pin de matriz de puntos de encabezado de movimiento impactante** (7)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

La **matriz de puntos de encabezado de movimiento de impacto** (8)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

La **cabeza de movimiento de impacto está totalmente formada** (9)


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

**Banda de impacto** (10)


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

**Impacto en otros** (11)


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

**Inyección de tinta acuosa** (12)


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

**Inyección de tinta sólida** (13)


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

**Inyección de tinta** (14)


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

**Lápiz** (15)


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

**Transferencia térmica** (16)


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

**Sensible térmica** (17)


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

**Difusión térmica** (18)


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

**Otro térmico** (19)


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

**Electroerosión** (20)


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**Electrostática** (21)


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**Microficha fotográfica** (22)


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**Filmadora fotográfica** (23)


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**Otros fotográficos** (24)


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

Desposición de la **iones** (25)


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

**eBeam** (26)


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

**Typesetter** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCopies**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. copias")
</dt> </dl>

Número máximo de copias que la impresora puede producir para un trabajo.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. NumberUp")
</dt> </dl>

Número máximo de páginas de secuencia de impresión que la impresora puede representar en una hoja de medios, como papel.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. jobs"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Trabajo más grande como un flujo de bytes, en kilobytes, que la impresora puede aceptar. Un valor de 0 (cero) indica que no se ha establecido ningún límite.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). LanguagesSupported "," CIM \_ PrintJob. MimeTypes "," CIM \_ PrintService. MimeTypesSupported ")
</dt> </dl>

Matriz de explicaciones detalladas del tipo MIME que admite la impresora. Si se proporcionan datos, el valor 47 ("MIME") debe incluirse en la propiedad **LanguagesSupported** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nombre de la impresora.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ")
</dt> </dl>

Matriz de idiomas admitidos para las cadenas que la impresora utiliza para la salida de información de administración. Debe ajustarse a [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt). Por ejemplo, "en" se utiliza para inglés.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**Network**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, la impresora es una impresora de red. Si las propiedades **local** y de **red** están establecidas en **true**, la impresora es una impresora de red.

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de los tipos de papel que admite la impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span id="A"></span><span id="a"></span>**A** (2)


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (3)


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span id="C"></span><span id="c"></span>**C** (4)


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span id="D"></span><span id="d"></span>**D** (5)


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (6)


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letra** (7)


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-Envelope** (9)


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-Envelope** (10)


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-número-10-sobre** (11)


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-Envelope** (12)


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-Envelope** (13)


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-Envelope** (14)


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-número-9-sobre** (15)


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-Envelope** (16)


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-Envelope** (17)


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span id="A0"></span><span id="a0"></span>**A0** (18)


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span id="A1"></span><span id="a1"></span>**A1** (19)


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span id="A2"></span><span id="a2"></span>**A2** (20)


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span id="A3"></span><span id="a3"></span>**A3** (21)


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span id="A4"></span><span id="a4"></span>**A4** (22)


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span id="A5"></span><span id="a5"></span>**A5** (23)


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span id="A6"></span><span id="a6"></span>**A6** (24)


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span id="A7"></span><span id="a7"></span>**A7** (25)


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span id="A8"></span><span id="a8"></span>**A8** (26)


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span id="B0"></span><span id="b0"></span>**B0** (28)


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span id="B1"></span><span id="b1"></span>**B1** (29)


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span id="B2"></span><span id="b2"></span>**B2** (30)


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span id="B3"></span><span id="b3"></span>**B3** (31)


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span id="B4"></span><span id="b4"></span>**B4** (32)


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span id="B5"></span><span id="b5"></span>**B5** (33)


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span id="B6"></span><span id="b6"></span>**B6** (34)


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span id="B7"></span><span id="b7"></span>**B7** (35)


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span id="B8"></span><span id="b8"></span>**B8** (36)


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span id="B9"></span><span id="b9"></span>**B9** (37)


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span id="B10"></span><span id="b10"></span>**B10** (38)


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span id="C0"></span><span id="c0"></span>**C0** (39)


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span id="C1"></span><span id="c1"></span>**C1** (40)


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)


</dt> <dd>

C2

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span id="C4"></span><span id="c4"></span>**C4** (42)


</dt> <dd>

C3

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span id="C5"></span><span id="c5"></span>**C5** (43)


</dt> <dd>

C4

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span id="C6"></span><span id="c6"></span>**C6** (44)


</dt> <dd>

C5

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span id="C7"></span><span id="c7"></span>**C7** (45)


</dt> <dd>

C6

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span id="C8"></span><span id="c8"></span>**C8** (46)


</dt> <dd>

C7

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Designación ISO** (47)


</dt> <dd>

C8

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)


</dt> <dd>

ISO-Designated

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)


</dt> <dd>

JIS B0

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)


</dt> <dd>

JIS B1

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)


</dt> <dd>

JIS B2

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)


</dt> <dd>

JIS B3

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)


</dt> <dd>

JIS B4

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)


</dt> <dd>

JIS B5

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)


</dt> <dd>

JIS B6

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)


</dt> <dd>

JIS B7

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)


</dt> <dd>

JIS B8

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)


</dt> <dd>

JIS B9

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Letra na** (59)


</dt> <dd>

JIS B10

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-legal** (60)


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**Sobre B4** (61)


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**Sobre B5** (62)


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**Sobre C3** (63)


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**Sobre C4** (64)


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**Sobre C5** (65)


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**Sobre C6** (66)


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Sobre monarca** (68)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Ejecutivo** (69)


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Factura** (71)


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Libro de contabilidad** (72)


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Cuarto** (73)


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ PrintService. PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")
</dt> </dl>

Matriz de tipos de papel que están disponibles actualmente en la impresora. Cada cadena se debe expresar en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 10175, que se resume en el Apéndice C de [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB). Cualquier tamaño de papel identificado en esta propiedad también debe aparecer en la propiedad **PaperSizesSupported** .

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

Ejemplo: ISO-A4-color

</dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Parámetros opcionales para el procesador de impresión.

Ejemplo: "copias = 2"

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

Ejemplo: \* PNP030b

</dd> <dt>

**PortName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Puerto que se usa para transmitir datos a una impresora. Si una impresora está conectada a más de un puerto, los nombres de cada puerto se separan mediante comas.

Ejemplo: LPT1:, LPT2:, LPT3:

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

Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar. Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).

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

Si **es true**, se puede administrar la eficacia del dispositivo, lo que significa que se puede poner en modo de suspensión. La propiedad no indica que las características de administración de energía están habilitadas, solo que el dispositivo lógico es capaz de administrar energía.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**PrinterPaperNames**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de tamaños de papel que admite la impresora. Los nombres especificados por la impresora se usan para representar los tamaños de papel compatibles.

Ejemplo: B5 (JIS)

</dd> <dt>

**PrinterState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Uno de los Estados posibles relacionados con esta impresora. Esta propiedad ha quedado obsoleta. En lugar de esta propiedad, use **PrinterStatus**.

<dt>

0
</dt> <dd>

Inactivo: para obtener más información, vea la sección Comentarios a continuación.

</dd> <dt>

1
</dt> <dd>

En pausa

</dd> <dt>

2
</dt> <dd>

Error

</dd> <dt>

3
</dt> <dd>

Eliminación pendiente

</dd> <dt>

4
</dt> <dd>

Atasco de papel

</dd> <dt>

5
</dt> <dd>

Papel de salida

</dd> <dt>

6
</dt> <dd>

Alimentación manual

</dd> <dt>

7
</dt> <dd>

Problema de papel

</dd> <dt>

8
</dt> <dd>

Sin conexión

</dd> <dt>

9
</dt> <dd>

E/s activa

</dd> <dt>

10
</dt> <dd>

Ocupado

</dd> <dt>

11
</dt> <dd>

Impresión

</dd> <dt>

12
</dt> <dd>

Bandeja de salida llena

</dd> <dt>

13
</dt> <dd>

No disponible

</dd> <dt>

14
</dt> <dd>

En espera

</dd> <dt>

15
</dt> <dd>

Processing

</dd> <dt>

16
</dt> <dd>

Inicialización

</dd> <dt>

17
</dt> <dd>

Preparando

</dd> <dt>

18
</dt> <dd>

Tóner bajo

</dd> <dt>

19
</dt> <dd>

Sin tóner

</dd> <dt>

20
</dt> <dd>

Página aparcan

</dd> <dt>

21
</dt> <dd>

Intervención del usuario requerida

</dd> <dt>

22
</dt> <dd>

Memoria insuficiente

</dd> <dt>

23
</dt> <dd>

Puerta abierta

</dd> <dt>

24
</dt> <dd>

Servidor \_ desconocido

</dd> <dt>

25
</dt> <dd>

Ahorro de energía

</dd> </dl>

</dd> <dt>

**PrinterStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")
</dt> </dl>

Información de estado de una impresora diferente de la especificada en la propiedad **disponibilidad** del dispositivo lógico.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (3)


</dt> <dd>

Inactivo: para obtener más información, vea la sección Comentarios a continuación.

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Impresión** (4)


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Preparación** (5)


</dt> <dd>

Preparando

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Impresión detenida** (6)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PrintJobDataType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tipo de datos de un trabajo de impresión en espera del dispositivo de impresión basado en Windows.

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre del administrador de trabajos de impresión que controla los trabajos de impresión.

Ejemplo: SPOOLSS.DLL

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Prioridad de la impresora. Los trabajos en una impresora de prioridad más alta se programan en primer lugar.

</dd> <dt>

**Publicado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, la impresora se publica en el servicio de directorio de red.

</dd> <dt>

**En cola**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el búfer de la impresora y pone en cola los trabajos de impresión.

</dd> <dt>

**RawOnly**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, la impresora solo acepta los datos sin procesar que se van a poner en cola.

</dd> <dt>

**SeparatorFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre del archivo utilizado para crear una página separadora. Esta página se utiliza para separar los trabajos de impresión que se envían a la impresora.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del servidor que controla la impresora. Si esta cadena es **null**, la impresora se controla localmente.

</dd> <dt>

**Compartido**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, la impresora está disponible como un recurso compartido de red.

</dd> <dt>

**ShareName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre del recurso compartido del dispositivo de impresión basado en Windows.

Ejemplo: " \\ \\ servidorimpresión1 \\ Printer2"

</dd> <dt>

**SpoolEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad está obsoleta; No use. Si es **true**, la cola de impresión está habilitada para la impresora.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Fecha y hora en que una impresora puede empezar a imprimir un trabajo: Si la impresora está limitada a imprimirse en momentos concretos. Este valor se expresa como el tiempo transcurrido desde 12:00 AM GMT (hora del meridiano de Greenwich).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: **correcto**, **degradado** y **Pred FAIL** (un elemento, como una unidad de disco duro habilitada para Smart, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativo incluyen: **error**, **Inicio**, **detención** y **servicio**. Este último **servicio** se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es **correcto** ni en ninguno de los otros Estados.

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

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")
</dt> </dl>

Estado del dispositivo lógico. Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (**no aplicable**).

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

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)
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

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nombre del sistema de ámbito.

Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se restableció por última vez la impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Fecha y hora en que una impresora puede imprimir el último trabajo: Si la impresora está limitada a imprimirse en momentos concretos. Este valor se expresa como el tiempo transcurrido desde 12:00 AM GMT (hora del meridiano de Greenwich).

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](../wmisdk/standard-qualifiers.md) ("píxeles por pulgada")
</dt> </dl>

Resolución vertical, en píxeles por pulgada, de la impresora.

Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).

</dd> <dt>

**WorkOffline**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, puede poner en cola los trabajos de impresión en el equipo cuando la impresora está sin conexión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ impresora de Win32** se deriva de la [**\_ impresora CIM**](cim-printer.md). Antes de llamar a [**SWbemObject \_ . put**](../wmisdk/swbemobject-put-.md) o [**IWbemServices::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) para una instancia de **\_ impresora de Win32** , el privilegio **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** para Visual Basic y LoadDriver para los monikers de scripting) debe estar habilitado. Para obtener más información, vea [**constantes de privilegios**](../wmisdk/privilege-constants.md) y [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md). En el ejemplo de código de VBScript siguiente se muestra cómo habilitar el privilegio **SetLoadDriverPrivilege** en el script.

Para trabajar con clústeres de impresora de MSCS, use el prnadmin.dll ensamblado, o bien el espacio de nombres [System. Printing](/dotnet/api/system.printing) .NET Framework.


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



Windows usa las credenciales del usuario que ejecuta el script para determinar cuáles son las impresoras disponibles. Por lo tanto, si está ejecutando un script de forma remota, es posible que solo pueda tener acceso a cualquier impresora que esté disponible para su cuenta de usuario en ese sistema remoto.

No se puede usar la clase **\_ Printer de Win32** para impresoras en un clúster de impresión de MSCS. En su lugar, puede que necesite usar la herramienta PrinterAdmin (PrnAdmin.dll) o el espacio de nombres .NET Framework [System. Printing](/dotnet/api/system.printing) .

> [!Note]  
> Si va a recuperar **PrinterStatus** = 3 o **PrinterState** = 0, es posible que el controlador de impresora no alimente información precisa en WMI. WMI recupera la información de la impresora del proceso de spoolsv.exe. Es posible que el controlador de impresora no informe de su estado al administrador de trabajos de impresión. En este caso, **la \_ impresora de Win32** informa de la impresora como **inactiva**.

 

## <a name="examples"></a>Ejemplos

En el ejemplo de [creación de un dibujo de configuración de equipo con Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell en la galería de TechNet se usa la **\_ impresora Win32** para interactuar con el modelo de automatización de Visio con el fin de crear un dibujo de Visio.

El [script de información del equipo remoto de PowerShell](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) usa una serie de clases, incluida la **\_ impresora Win32**, para recuperar información acerca de un equipo remoto.

En el siguiente ejemplo de código de PowerShell se muestra cómo determinar la impresora predeterminada del equipo local.


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



En el siguiente ejemplo de código de VBScript se describe cómo recuperar estadísticas de impresora de instancias de la **\_ impresora Win32**.


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



En el siguiente ejemplo de código Perl se describe cómo recuperar estadísticas de impresora de instancias de la **\_ impresora Win32**.


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



En el ejemplo de código de VBScript siguiente se muestra cómo obtener el nombre de la impresora predeterminada de un equipo.


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ printer. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Impresora CIM**](cim-printer.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> <dt>

[Tareas de WMI: impresoras e impresión](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
