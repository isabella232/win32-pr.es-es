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
# <a name="win32_printer-class"></a><span data-ttu-id="74ec9-103">\_Clase Printer de Win32</span><span class="sxs-lookup"><span data-stu-id="74ec9-103">Win32\_Printer class</span></span>

<span data-ttu-id="74ec9-104">La [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ impresora de Win32** representa un dispositivo conectado a un equipo que se ejecuta en un sistema operativo Microsoft Windows y que puede generar una imagen impresa o texto en papel o en otro medio.</span><span class="sxs-lookup"><span data-stu-id="74ec9-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="74ec9-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="74ec9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ec9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74ec9-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="74ec9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="74ec9-107">Members</span></span>

<span data-ttu-id="74ec9-108">La **clase \_ Printer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="74ec9-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="74ec9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="74ec9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="74ec9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74ec9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74ec9-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="74ec9-111">Methods</span></span>

<span data-ttu-id="74ec9-112">La **clase \_ Printer de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="74ec9-113">Método</span><span class="sxs-lookup"><span data-stu-id="74ec9-113">Method</span></span>                                                                               | <span data-ttu-id="74ec9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="74ec9-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74ec9-115">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="74ec9-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="74ec9-116">Agrega una conexión a la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="74ec9-117">**CancelAllJobs**</span><span class="sxs-lookup"><span data-stu-id="74ec9-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="74ec9-118">Cancela todos los trabajos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="74ec9-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="74ec9-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="74ec9-120">Devuelve el descriptor de seguridad que controla el acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="74ec9-121">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="74ec9-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="74ec9-122">Pone en pausa la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="74ec9-123">**PrintTestPage**</span><span class="sxs-lookup"><span data-stu-id="74ec9-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="74ec9-124">Imprime una página de prueba.</span><span class="sxs-lookup"><span data-stu-id="74ec9-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="74ec9-125">**RenamePrinter**</span><span class="sxs-lookup"><span data-stu-id="74ec9-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="74ec9-126">Cambia el nombre de una impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="74ec9-127">**Reset**</span><span class="sxs-lookup"><span data-stu-id="74ec9-127">**Reset**</span></span>                                                                            | <span data-ttu-id="74ec9-128">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-128">Not implemented.</span></span> <span data-ttu-id="74ec9-129">Para obtener más información sobre cómo implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="74ec9-130">**Reanudar**</span><span class="sxs-lookup"><span data-stu-id="74ec9-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="74ec9-131">Reanuda la cola de impresión en pausa.</span><span class="sxs-lookup"><span data-stu-id="74ec9-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="74ec9-132">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="74ec9-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="74ec9-133">Establece la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="74ec9-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="74ec9-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="74ec9-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="74ec9-135">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-135">Not implemented.</span></span> <span data-ttu-id="74ec9-136">Para obtener más información sobre cómo implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="74ec9-137">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="74ec9-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="74ec9-138">Escribe una versión actualizada del descriptor de seguridad que controla el acceso a la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="74ec9-139">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74ec9-139">Properties</span></span>

<span data-ttu-id="74ec9-140">La **clase \_ Printer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="74ec9-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74ec9-141">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="74ec9-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-144">Mapa de bits de atributos para un dispositivo de impresión basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="74ec9-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="74ec9-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Impresora \_ de ATRIBUTO \_ en cola** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="74ec9-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-146">En cola</span><span class="sxs-lookup"><span data-stu-id="74ec9-146">Queued</span></span>

<span data-ttu-id="74ec9-147">Los trabajos de impresión se almacenan en búfer y se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="74ec9-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="74ec9-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Impresora \_ de ATTRIBUTE \_ Direct** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="74ec9-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-149">Directo</span><span class="sxs-lookup"><span data-stu-id="74ec9-149">Direct</span></span>

<span data-ttu-id="74ec9-150">Documento que se va a enviar directamente a la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="74ec9-151">Este valor se usa si los trabajos de impresión no se ponen en cola correctamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="74ec9-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Impresora \_ de ATRIBUTO \_ predeterminado** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="74ec9-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-153">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="74ec9-153">Default</span></span>

<span data-ttu-id="74ec9-154">Impresora predeterminada en un equipo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="74ec9-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Impresora \_ de ATTRIBUTE \_ Shared** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="74ec9-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-156">Compartido</span><span class="sxs-lookup"><span data-stu-id="74ec9-156">Shared</span></span>

<span data-ttu-id="74ec9-157">Disponible como recurso compartido de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="74ec9-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Impresora \_ de \_Red de atributos** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="74ec9-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-159">Red</span><span class="sxs-lookup"><span data-stu-id="74ec9-159">Network</span></span>

<span data-ttu-id="74ec9-160">Conectado a una red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-160">Attached to a network.</span></span> <span data-ttu-id="74ec9-161">Si se establecen los bits locales y de red, indica una impresora de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="74ec9-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Impresora \_ de ATRIBUTO \_ Hidden** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="74ec9-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-163">Hidden</span><span class="sxs-lookup"><span data-stu-id="74ec9-163">Hidden</span></span>

<span data-ttu-id="74ec9-164">Oculta de algunos usuarios de la red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="74ec9-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Impresora \_ de ATRIBUTO \_ local** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="74ec9-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-166">Local</span><span class="sxs-lookup"><span data-stu-id="74ec9-166">Local</span></span>

<span data-ttu-id="74ec9-167">Conectado directamente a un equipo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-167">Directly connected to a computer.</span></span> <span data-ttu-id="74ec9-168">Si se establecen los bits locales y de red, indica una impresora de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="74ec9-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Impresora \_ de ATTRIBUTE \_ ENABLEDEVQ** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="74ec9-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-170">EnableDevQ</span><span class="sxs-lookup"><span data-stu-id="74ec9-170">EnableDevQ</span></span>

<span data-ttu-id="74ec9-171">Habilite la cola en la impresora, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="74ec9-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="74ec9-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Impresora \_ de \_KEEPPRINTEDJOBS de atributo** 256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="74ec9-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-173">KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="74ec9-173">KeepPrintedJobs</span></span>

<span data-ttu-id="74ec9-174">El administrador de trabajos de impresión no debe eliminar los documentos una vez impresos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="74ec9-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Impresora \_ de El atributo se \_ \_ completa \_ primero** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="74ec9-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-176">DoCompleteFirst</span><span class="sxs-lookup"><span data-stu-id="74ec9-176">DoCompleteFirst</span></span>

<span data-ttu-id="74ec9-177">Inicie los trabajos que han terminado de poner en cola primero.</span><span class="sxs-lookup"><span data-stu-id="74ec9-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="74ec9-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Impresora \_ de El atributo \_ funciona \_ sin conexión** (1024 (0x400))</span><span class="sxs-lookup"><span data-stu-id="74ec9-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-179">WorkOffline</span><span class="sxs-lookup"><span data-stu-id="74ec9-179">WorkOffline</span></span>

<span data-ttu-id="74ec9-180">Poner en cola los trabajos de impresión cuando una impresora no está disponible.</span><span class="sxs-lookup"><span data-stu-id="74ec9-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="74ec9-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Impresora \_ de El atributo \_ habilita \_ BIDI** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="74ec9-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-182">EnableBIDI</span><span class="sxs-lookup"><span data-stu-id="74ec9-182">EnableBIDI</span></span>

<span data-ttu-id="74ec9-183">Habilitar la impresión bidireccional.</span><span class="sxs-lookup"><span data-stu-id="74ec9-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="74ec9-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Impresora \_ de ATRIBUTO \_ \_ solo sin formato** (4096 (0x1000))</span><span class="sxs-lookup"><span data-stu-id="74ec9-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-185">Permita que solo se pongan en cola los trabajos de tipo de datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="74ec9-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Impresora \_ de ATRIBUTO \_ publicado** (8192 (0x2000))</span><span class="sxs-lookup"><span data-stu-id="74ec9-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-187">Publicado</span><span class="sxs-lookup"><span data-stu-id="74ec9-187">Published</span></span>

<span data-ttu-id="74ec9-188">Publicado en el servicio de directorio de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-189">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="74ec9-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-192">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-193">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-193">Availability and status of the device.</span></span>

<span data-ttu-id="74ec9-194">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="74ec9-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-198">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="74ec9-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="74ec9-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="74ec9-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="74ec9-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="74ec9-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="74ec9-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="74ec9-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="74ec9-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="74ec9-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="74ec9-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="74ec9-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="74ec9-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="74ec9-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-209">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="74ec9-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="74ec9-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-211">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="74ec9-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-213">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="74ec9-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="74ec9-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-216">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="74ec9-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="74ec9-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-218">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="74ec9-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="74ec9-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-220">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="74ec9-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-222">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="74ec9-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-224">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="74ec9-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-225">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="74ec9-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-226">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-228">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="74ec9-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-229">Matriz de todas las hojas de trabajo disponibles en una impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="74ec9-230">También se puede usar para describir el banner que una impresora puede proporcionar al principio de cada trabajo, u otras opciones especificadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="74ec9-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="74ec9-231">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-232">**AveragePagesPerMinute**</span><span class="sxs-lookup"><span data-stu-id="74ec9-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-233">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-235">Tasa de impresión, en promedio de páginas por minuto, que una impresora puede producir resultados.</span><span class="sxs-lookup"><span data-stu-id="74ec9-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-236">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="74ec9-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-237">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-239">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ impresora CIM**](cim-printer.md). CapabilityDescriptions "," CIM \_ PrintJob. Finishing "," CIM \_ PrintService. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-240">Matriz de capacidades de impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-240">Array of printer capabilities.</span></span>

<span data-ttu-id="74ec9-241">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="74ec9-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="74ec9-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="74ec9-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="74ec9-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="74ec9-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="74ec9-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="74ec9-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="74ec9-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="74ec9-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="74ec9-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="74ec9-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="74ec9-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="74ec9-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-257">Two-Sided borde largo</span><span class="sxs-lookup"><span data-stu-id="74ec9-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="74ec9-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-259">Two-Sided borde corto</span><span class="sxs-lookup"><span data-stu-id="74ec9-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="74ec9-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="74ec9-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="74ec9-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="74ec9-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="74ec9-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="74ec9-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="74ec9-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-267">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="74ec9-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-268">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-270">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ impresora CIM**](cim-printer.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-271">Matriz de cadenas de formato libre que proporcionan explicaciones detalladas para las características de impresora indicadas en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="74ec9-272">Cada entrada de esta matriz se relaciona con una entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="74ec9-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="74ec9-273">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-274">**Caption**</span><span class="sxs-lookup"><span data-stu-id="74ec9-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-277">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="74ec9-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-278">Breve descripción de un objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="74ec9-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="74ec9-279">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-280">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-281">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-283">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. charset"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-284">Matriz de juegos de caracteres disponibles para la salida.</span><span class="sxs-lookup"><span data-stu-id="74ec9-284">Array of available character sets for output.</span></span> <span data-ttu-id="74ec9-285">Las cadenas proporcionadas en esta propiedad deben cumplir la semántica y la sintaxis que se especifican en la sección 4.1.2 ("charset Parameters") en RFC 2046 (MIME parte 2) y contenidas en el registro de juegos de caracteres de IANA.</span><span class="sxs-lookup"><span data-stu-id="74ec9-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="74ec9-286">Algunos ejemplos son "UTF-8", "US-ASCII" y "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="74ec9-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="74ec9-287">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-288">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="74ec9-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-290">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-291">Comentario para una cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-291">Comment for a print queue.</span></span>

<span data-ttu-id="74ec9-292">Ejemplo: impresora de color</span><span class="sxs-lookup"><span data-stu-id="74ec9-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-293">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="74ec9-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-294">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-296">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="74ec9-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-297">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="74ec9-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="74ec9-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="74ec9-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="74ec9-300"> (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-301">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="74ec9-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="74ec9-303">(1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-304">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="74ec9-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="74ec9-306">(2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="74ec9-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="74ec9-308">(3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-309">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="74ec9-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="74ec9-311">(4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-312">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-312">Device is not working properly.</span></span> <span data-ttu-id="74ec9-313">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="74ec9-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="74ec9-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="74ec9-315">(5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-316">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="74ec9-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="74ec9-318"> (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-319">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="74ec9-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="74ec9-321">(7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="74ec9-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="74ec9-323">(8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-324">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="74ec9-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="74ec9-326">(9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-327">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-327">Device is not working properly.</span></span> <span data-ttu-id="74ec9-328">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="74ec9-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="74ec9-330">(10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-331">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="74ec9-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="74ec9-333">(11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-334">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="74ec9-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="74ec9-336">(12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-337">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="74ec9-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="74ec9-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="74ec9-339">(13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-340">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="74ec9-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="74ec9-342">(14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-343">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="74ec9-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="74ec9-345">(15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-346">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="74ec9-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="74ec9-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="74ec9-348">(16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-349">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="74ec9-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="74ec9-351">(17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-352">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="74ec9-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="74ec9-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="74ec9-354">(18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-355">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="74ec9-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="74ec9-357">(19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="74ec9-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="74ec9-359">(20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-360">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="74ec9-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="74ec9-362">(21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-363">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="74ec9-363">System failure.</span></span> <span data-ttu-id="74ec9-364">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="74ec9-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="74ec9-365">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="74ec9-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="74ec9-367">(22)</span><span class="sxs-lookup"><span data-stu-id="74ec9-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-368">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="74ec9-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="74ec9-370">(23)</span><span class="sxs-lookup"><span data-stu-id="74ec9-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-371">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="74ec9-371">System failure.</span></span> <span data-ttu-id="74ec9-372">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="74ec9-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="74ec9-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="74ec9-374">(24)</span><span class="sxs-lookup"><span data-stu-id="74ec9-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-375">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="74ec9-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="74ec9-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="74ec9-377">(25)</span><span class="sxs-lookup"><span data-stu-id="74ec9-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-378">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="74ec9-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="74ec9-380">(26)</span><span class="sxs-lookup"><span data-stu-id="74ec9-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-381">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="74ec9-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="74ec9-383">(27)</span><span class="sxs-lookup"><span data-stu-id="74ec9-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-384">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="74ec9-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="74ec9-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="74ec9-386">(28)</span><span class="sxs-lookup"><span data-stu-id="74ec9-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-387">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="74ec9-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="74ec9-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="74ec9-389">(29)</span><span class="sxs-lookup"><span data-stu-id="74ec9-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-390">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-390">Device is disabled.</span></span> <span data-ttu-id="74ec9-391">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="74ec9-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="74ec9-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="74ec9-393">(30)</span><span class="sxs-lookup"><span data-stu-id="74ec9-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-394">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="74ec9-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="74ec9-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="74ec9-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="74ec9-396">31</span><span class="sxs-lookup"><span data-stu-id="74ec9-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-397">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-397">Device is not working properly.</span></span> <span data-ttu-id="74ec9-398">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="74ec9-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-399">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="74ec9-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-400">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-402">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="74ec9-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-403">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="74ec9-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="74ec9-404">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-405">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-408">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74ec9-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-409">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada para crear una instancia.</span><span class="sxs-lookup"><span data-stu-id="74ec9-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="74ec9-410">Cuando se usa con otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="74ec9-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="74ec9-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-412">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="74ec9-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-413">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-415">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-416">Matriz de funciones de impresora que se usan actualmente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="74ec9-417">También debe aparecer una entrada en esta propiedad en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="74ec9-418">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="74ec9-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="74ec9-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="74ec9-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="74ec9-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="74ec9-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="74ec9-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="74ec9-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="74ec9-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="74ec9-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="74ec9-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="74ec9-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="74ec9-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="74ec9-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-434">Two-Sided borde largo</span><span class="sxs-lookup"><span data-stu-id="74ec9-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="74ec9-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-436">Two-Sided borde corto</span><span class="sxs-lookup"><span data-stu-id="74ec9-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="74ec9-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="74ec9-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="74ec9-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="74ec9-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="74ec9-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="74ec9-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="74ec9-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-444">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="74ec9-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-447">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-448">Juego de caracteres que se usa actualmente para la salida.</span><span class="sxs-lookup"><span data-stu-id="74ec9-448">The character set currently used for output.</span></span> <span data-ttu-id="74ec9-449">Las cadenas proporcionadas en esta propiedad deben cumplir la semántica y la sintaxis que se especifican en la sección 4.1.2 ("charset Parameters") en RFC 2046 (MIME parte 2) y contenidas en el registro de juegos de caracteres de IANA.</span><span class="sxs-lookup"><span data-stu-id="74ec9-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="74ec9-450">Entre los ejemplos se incluyen "UTF-8", "US-ASCII" e ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="74ec9-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="74ec9-451">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-452">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="74ec9-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-453">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-455">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). LanguagesSupported ","**\_ impresora CIM**.**CurrentMimeType**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-456">Idioma de la impresora que se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-456">Printer language currently used.</span></span> <span data-ttu-id="74ec9-457">El lenguaje utilizado debe aparecer en la propiedad **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="74ec9-458">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="74ec9-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="74ec9-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="74ec9-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="74ec9-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="74ec9-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="74ec9-466"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="74ec9-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="74ec9-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="74ec9-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="74ec9-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="74ec9-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="74ec9-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="74ec9-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Datos de línea** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-474">LineData</span><span class="sxs-lookup"><span data-stu-id="74ec9-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="74ec9-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-476">DODCA</span><span class="sxs-lookup"><span data-stu-id="74ec9-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="74ec9-477"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="74ec9-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="74ec9-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="74ec9-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="74ec9-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="74ec9-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="74ec9-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="74ec9-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="74ec9-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="74ec9-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="74ec9-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="74ec9-485"><span id="WPS"></span><span id="wps"></span>**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="74ec9-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="74ec9-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="74ec9-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="74ec9-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="74ec9-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="74ec9-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="74ec9-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="74ec9-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="74ec9-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="74ec9-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="74ec9-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="74ec9-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simple** (31)</span><span class="sxs-lookup"><span data-stu-id="74ec9-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-492">SimpleText</span><span class="sxs-lookup"><span data-stu-id="74ec9-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="74ec9-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="74ec9-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="74ec9-494"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="74ec9-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="74ec9-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**Impress** (34)</span><span class="sxs-lookup"><span data-stu-id="74ec9-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="74ec9-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="74ec9-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="74ec9-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="74ec9-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="74ec9-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="74ec9-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="74ec9-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automática** (38)</span><span class="sxs-lookup"><span data-stu-id="74ec9-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="74ec9-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="74ec9-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="74ec9-501"><span id="LIPS"></span><span id="lips"></span>**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="74ec9-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="74ec9-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="74ec9-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="74ec9-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="74ec9-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="74ec9-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Mayúsculas** (43)</span><span class="sxs-lookup"><span data-stu-id="74ec9-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="74ec9-505"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="74ec9-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="74ec9-506"><span id="LCDS"></span><span id="lcds"></span>**Pantallas LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="74ec9-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="74ec9-507"><span id="XES"></span><span id="xes"></span>**Dices** (46)</span><span class="sxs-lookup"><span data-stu-id="74ec9-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="74ec9-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="74ec9-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="74ec9-509">48</span><span class="sxs-lookup"><span data-stu-id="74ec9-509">48</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-510">XPS</span><span class="sxs-lookup"><span data-stu-id="74ec9-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-511">49</span><span class="sxs-lookup"><span data-stu-id="74ec9-511">49</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="74ec9-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-513">50</span><span class="sxs-lookup"><span data-stu-id="74ec9-513">50</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-514">PCLXL</span><span class="sxs-lookup"><span data-stu-id="74ec9-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-515">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="74ec9-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-516">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-517">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-518">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-519">Tipo MIME que se está usando actualmente si **CurrentLanguage** es un tipo MIME (valor = 47).</span><span class="sxs-lookup"><span data-stu-id="74ec9-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="74ec9-520">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-521">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="74ec9-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-522">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-523">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-524">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-525">Idioma que la impresora utiliza para la administración actualmente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="74ec9-526">El idioma que se muestra aquí también debe aparecer en la propiedad **NaturalLanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="74ec9-527">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-528">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="74ec9-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-529">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-531">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-532">Tipo de papel que está usando la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-532">Type of paper the printer is using.</span></span> <span data-ttu-id="74ec9-533">Se debe expresar en el formato especificado por la aplicación de impresión de documentos ISO/IEC 10175 (DPA), que se resume en el Apéndice C de RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="74ec9-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="74ec9-534">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-535">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="74ec9-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-536">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-538">Si es **true**, la impresora es la impresora predeterminada.</span><span class="sxs-lookup"><span data-stu-id="74ec9-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-539">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="74ec9-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-540">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-541">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-542">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-543">Matriz de las funciones de impresora utilizadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="74ec9-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="74ec9-544">Cada entrada de la matriz **DefaultCapabilities** también debe aparecer en la matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="74ec9-545">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="74ec9-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="74ec9-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="74ec9-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="74ec9-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="74ec9-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="74ec9-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="74ec9-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="74ec9-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="74ec9-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="74ec9-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="74ec9-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="74ec9-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="74ec9-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-561">Two-Sided borde largo</span><span class="sxs-lookup"><span data-stu-id="74ec9-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="74ec9-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-563">Two-Sided borde corto</span><span class="sxs-lookup"><span data-stu-id="74ec9-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="74ec9-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="74ec9-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="74ec9-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="74ec9-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="74ec9-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="74ec9-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="74ec9-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-571">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="74ec9-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-572">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-573">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-574">Número de copias producidas para un trabajo, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="74ec9-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="74ec9-575">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="74ec9-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-577">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-578">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-579">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). LanguagesSupported ","**\_ impresora CIM**.**DefaultMimeType**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-580">Idioma de impresora predeterminado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-580">Default printer language.</span></span> <span data-ttu-id="74ec9-581">El idioma que se muestra aquí también debe aparecer en la propiedad **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="74ec9-582">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="74ec9-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="74ec9-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="74ec9-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="74ec9-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="74ec9-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="74ec9-590"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="74ec9-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="74ec9-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="74ec9-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="74ec9-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="74ec9-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="74ec9-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="74ec9-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Datos de línea** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-598">LineData</span><span class="sxs-lookup"><span data-stu-id="74ec9-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="74ec9-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-600">DODCA</span><span class="sxs-lookup"><span data-stu-id="74ec9-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="74ec9-601"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="74ec9-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="74ec9-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="74ec9-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="74ec9-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="74ec9-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="74ec9-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="74ec9-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="74ec9-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="74ec9-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="74ec9-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="74ec9-609"><span id="WPS"></span><span id="wps"></span>**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="74ec9-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="74ec9-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="74ec9-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="74ec9-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="74ec9-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="74ec9-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="74ec9-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="74ec9-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="74ec9-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="74ec9-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="74ec9-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="74ec9-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simple** (31)</span><span class="sxs-lookup"><span data-stu-id="74ec9-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-616">SimpleText</span><span class="sxs-lookup"><span data-stu-id="74ec9-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="74ec9-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="74ec9-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="74ec9-618"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="74ec9-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="74ec9-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**Impress** (34)</span><span class="sxs-lookup"><span data-stu-id="74ec9-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="74ec9-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="74ec9-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="74ec9-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="74ec9-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="74ec9-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="74ec9-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="74ec9-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automática** (38)</span><span class="sxs-lookup"><span data-stu-id="74ec9-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="74ec9-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="74ec9-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="74ec9-625"><span id="LIPS"></span><span id="lips"></span>**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="74ec9-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="74ec9-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="74ec9-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="74ec9-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="74ec9-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="74ec9-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Mayúsculas** (43)</span><span class="sxs-lookup"><span data-stu-id="74ec9-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="74ec9-629"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="74ec9-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="74ec9-630"><span id="LCDS"></span><span id="lcds"></span>**Pantallas LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="74ec9-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="74ec9-631"><span id="XES"></span><span id="xes"></span>**Dices** (46)</span><span class="sxs-lookup"><span data-stu-id="74ec9-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="74ec9-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="74ec9-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="74ec9-633">48</span><span class="sxs-lookup"><span data-stu-id="74ec9-633">48</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-634">XPS</span><span class="sxs-lookup"><span data-stu-id="74ec9-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-635">49</span><span class="sxs-lookup"><span data-stu-id="74ec9-635">49</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="74ec9-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-637">50</span><span class="sxs-lookup"><span data-stu-id="74ec9-637">50</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-638">PCLXL</span><span class="sxs-lookup"><span data-stu-id="74ec9-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-639">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="74ec9-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-640">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-641">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-642">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-643">Tipo MIME que se está usando actualmente, si el valor **DefaultLanguage** es un tipo MIME (valor = 47).</span><span class="sxs-lookup"><span data-stu-id="74ec9-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="74ec9-644">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-645">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="74ec9-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-646">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-647">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-648">Número de páginas de secuencia de impresión que la impresora representa en una hoja de medios, a menos que un trabajo especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="74ec9-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="74ec9-649">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-650">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="74ec9-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-651">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-652">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-653">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-654">Tipo de papel que utiliza la impresora, a menos que un trabajo de impresión especifique un tipo de papel diferente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="74ec9-655">La cadena se debe expresar en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 1017, que se resume en el Apéndice C de [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="74ec9-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="74ec9-656">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-657">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="74ec9-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-658">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-659">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-660">Valor de prioridad predeterminado asignado a cada trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-661">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="74ec9-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-662">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-663">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-664">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="74ec9-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-665">Descripción de un objeto.</span><span class="sxs-lookup"><span data-stu-id="74ec9-665">Description of an object.</span></span>

<span data-ttu-id="74ec9-666">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-667">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="74ec9-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-668">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-669">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-670">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-671">Información de error de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-671">Printer error information.</span></span>

<span data-ttu-id="74ec9-672">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-673">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-674">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="74ec9-675">**Sin errores** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="74ec9-676">**Papel bajo** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="74ec9-677">**Sin papel** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="74ec9-678">**Tóner bajo** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="74ec9-679">**Sin tóner** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="74ec9-680">**Puerta abierta** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="74ec9-681">**Atascado** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="74ec9-682">**Sin conexión** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="74ec9-683">**Servicio solicitado** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="74ec9-684">**Bandeja de salida llena** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-685">**ID**</span><span class="sxs-lookup"><span data-stu-id="74ec9-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-686">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-687">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-688">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74ec9-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-689">Identificador único de la impresora en un sistema.</span><span class="sxs-lookup"><span data-stu-id="74ec9-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="74ec9-690">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-691">**Direct**</span><span class="sxs-lookup"><span data-stu-id="74ec9-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-692">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-693">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-694">Si es **true**, el trabajo de impresión se envía directamente a la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="74ec9-695">Si es **false**, el trabajo de impresión se pone en cola.</span><span class="sxs-lookup"><span data-stu-id="74ec9-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-696">**DoCompleteFirst**</span><span class="sxs-lookup"><span data-stu-id="74ec9-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-697">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-698">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-699">Si **es true**, la impresora inicia los trabajos que han terminado de poner en cola.</span><span class="sxs-lookup"><span data-stu-id="74ec9-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="74ec9-700">Si **es false**, la impresora inicia los trabajos en el orden en que se reciben los trabajos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-701">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-702">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-703">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-704">Nombre del controlador de impresora de Windows.</span><span class="sxs-lookup"><span data-stu-id="74ec9-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="74ec9-705">Ejemplo: controlador de fax de Windows</span><span class="sxs-lookup"><span data-stu-id="74ec9-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-706">**EnableBIDI**</span><span class="sxs-lookup"><span data-stu-id="74ec9-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-707">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-708">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-709">Si **es true**, la impresora puede imprimir bidireccionalmente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-710">**EnableDevQueryPrint**</span><span class="sxs-lookup"><span data-stu-id="74ec9-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-711">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-712">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-713">Si **es true**, la impresora contiene documentos en la cola cuando las configuraciones de documento e impresora no coinciden.</span><span class="sxs-lookup"><span data-stu-id="74ec9-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-714">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="74ec9-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-715">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-716">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-717">Si **es true**, se ha borrado el error comunicado en **LastErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="74ec9-718">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="74ec9-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-720">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-721">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-722">Información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="74ec9-723">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-724">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="74ec9-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-725">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-726">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-727">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md).**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="74ec9-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-728">Matriz de información complementaria para el estado de error actual indicado en **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="74ec9-729">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-730">**ExtendedDetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="74ec9-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-731">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-732">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-733">Notifica información de error estándar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-733">Reports standard error information.</span></span> <span data-ttu-id="74ec9-734">Se debe registrar información adicional en **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="74ec9-735">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="74ec9-735">Values are:</span></span>

<dt>

<span data-ttu-id="74ec9-736">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-737">Unknown</span><span class="sxs-lookup"><span data-stu-id="74ec9-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-738">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-739">Otros</span><span class="sxs-lookup"><span data-stu-id="74ec9-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-740">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-741">Sin errores</span><span class="sxs-lookup"><span data-stu-id="74ec9-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-742">3 (0X3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-743">Falta papel</span><span class="sxs-lookup"><span data-stu-id="74ec9-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-744">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-745">No hay papel</span><span class="sxs-lookup"><span data-stu-id="74ec9-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-746">5 (0X5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-747">Falta tóner</span><span class="sxs-lookup"><span data-stu-id="74ec9-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-748">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-749">Sin tóner</span><span class="sxs-lookup"><span data-stu-id="74ec9-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-750">7 (0X7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-751">Puerta abierta</span><span class="sxs-lookup"><span data-stu-id="74ec9-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-752">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-753">Papel atascado</span><span class="sxs-lookup"><span data-stu-id="74ec9-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-754">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-755">Servicio solicitado</span><span class="sxs-lookup"><span data-stu-id="74ec9-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-756">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="74ec9-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-757">Bandeja de salida llena</span><span class="sxs-lookup"><span data-stu-id="74ec9-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-758">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="74ec9-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-759">Problema de papel</span><span class="sxs-lookup"><span data-stu-id="74ec9-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-760">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="74ec9-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-761">No se puede imprimir la página</span><span class="sxs-lookup"><span data-stu-id="74ec9-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-762">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="74ec9-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-763">Intervención del usuario requerida</span><span class="sxs-lookup"><span data-stu-id="74ec9-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-764">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="74ec9-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-765">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="74ec9-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-766">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="74ec9-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-767">Servidor desconocido</span><span class="sxs-lookup"><span data-stu-id="74ec9-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-768">**ExtendedPrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="74ec9-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-769">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-770">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-771">Información de estado de una impresora diferente de la especificada en la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="74ec9-772">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-773">Otros</span><span class="sxs-lookup"><span data-stu-id="74ec9-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-774">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-775">Unknown</span><span class="sxs-lookup"><span data-stu-id="74ec9-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-776">3 (0X3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-777">Inactivo</span><span class="sxs-lookup"><span data-stu-id="74ec9-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-778">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-779">Impresión</span><span class="sxs-lookup"><span data-stu-id="74ec9-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-780">5 (0X5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-781">Preparando</span><span class="sxs-lookup"><span data-stu-id="74ec9-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-782">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-783">Impresión detenida</span><span class="sxs-lookup"><span data-stu-id="74ec9-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-784">7</span><span class="sxs-lookup"><span data-stu-id="74ec9-784">7</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-785">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="74ec9-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-786">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-787">En pausa</span><span class="sxs-lookup"><span data-stu-id="74ec9-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-788">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-789">Error</span><span class="sxs-lookup"><span data-stu-id="74ec9-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-790">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="74ec9-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-791">Ocupado</span><span class="sxs-lookup"><span data-stu-id="74ec9-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-792">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="74ec9-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-793">No disponible</span><span class="sxs-lookup"><span data-stu-id="74ec9-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-794">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="74ec9-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-795">En espera</span><span class="sxs-lookup"><span data-stu-id="74ec9-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-796">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="74ec9-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-797">Processing</span><span class="sxs-lookup"><span data-stu-id="74ec9-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-798">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="74ec9-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-799">Inicialización</span><span class="sxs-lookup"><span data-stu-id="74ec9-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-800">15</span><span class="sxs-lookup"><span data-stu-id="74ec9-800">15</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-801">Ahorro de energía</span><span class="sxs-lookup"><span data-stu-id="74ec9-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-802">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-803">Eliminación pendiente</span><span class="sxs-lookup"><span data-stu-id="74ec9-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-804">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-805">E/s activa</span><span class="sxs-lookup"><span data-stu-id="74ec9-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-806">18 (0X12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-807">Alimentación manual</span><span class="sxs-lookup"><span data-stu-id="74ec9-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-808">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="74ec9-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-809">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-810">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-811">Si es **true**, la impresora está oculta para los usuarios de la red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="74ec9-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-813">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-814">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-815">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](../wmisdk/standard-qualifiers.md) ("píxeles por pulgada")</span><span class="sxs-lookup"><span data-stu-id="74ec9-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-816">Resolución horizontal de la impresora, en píxeles por pulgada.</span><span class="sxs-lookup"><span data-stu-id="74ec9-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="74ec9-817">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="74ec9-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-819">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74ec9-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-820">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-821">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-822">Fecha y hora en que se instaló un objeto.</span><span class="sxs-lookup"><span data-stu-id="74ec9-822">Date and time an object was installed.</span></span> <span data-ttu-id="74ec9-823">El objeto se puede instalar sin que se escriba un valor en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="74ec9-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="74ec9-824">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-825">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="74ec9-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-826">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-827">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-828">Calificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="74ec9-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-829">Número de trabajos de impresión desde la última vez que se restableció la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="74ec9-830">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-831">**KeepPrintedJobs**</span><span class="sxs-lookup"><span data-stu-id="74ec9-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-832">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-833">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-834">Si **es true**, el administrador de trabajos de impresión no elimina los trabajos completados.</span><span class="sxs-lookup"><span data-stu-id="74ec9-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-835">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-836">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-837">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-838">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ PrintService. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-839">Matriz de los idiomas de impresión admitidos de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="74ec9-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="74ec9-840">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="74ec9-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="74ec9-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="74ec9-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="74ec9-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="74ec9-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="74ec9-848"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="74ec9-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="74ec9-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="74ec9-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="74ec9-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="74ec9-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="74ec9-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="74ec9-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Datos de línea** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-856">LineData</span><span class="sxs-lookup"><span data-stu-id="74ec9-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="74ec9-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-858">DODCA</span><span class="sxs-lookup"><span data-stu-id="74ec9-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="74ec9-859"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="74ec9-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="74ec9-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="74ec9-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="74ec9-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="74ec9-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="74ec9-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="74ec9-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="74ec9-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="74ec9-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="74ec9-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="74ec9-867"><span id="WPS"></span><span id="wps"></span>**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="74ec9-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="74ec9-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="74ec9-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="74ec9-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="74ec9-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="74ec9-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="74ec9-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="74ec9-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="74ec9-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="74ec9-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="74ec9-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="74ec9-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simple** (31)</span><span class="sxs-lookup"><span data-stu-id="74ec9-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-874">SimpleText</span><span class="sxs-lookup"><span data-stu-id="74ec9-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="74ec9-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="74ec9-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="74ec9-876"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="74ec9-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="74ec9-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**Impress** (34)</span><span class="sxs-lookup"><span data-stu-id="74ec9-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="74ec9-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="74ec9-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="74ec9-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="74ec9-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="74ec9-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="74ec9-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="74ec9-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automática** (38)</span><span class="sxs-lookup"><span data-stu-id="74ec9-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="74ec9-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="74ec9-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="74ec9-883"><span id="LIPS"></span><span id="lips"></span>**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="74ec9-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="74ec9-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="74ec9-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="74ec9-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="74ec9-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="74ec9-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Mayúsculas** (43)</span><span class="sxs-lookup"><span data-stu-id="74ec9-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="74ec9-887"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="74ec9-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="74ec9-888"><span id="LCDS"></span><span id="lcds"></span>**Pantallas LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="74ec9-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="74ec9-889"><span id="XES"></span><span id="xes"></span>**Dices** (46)</span><span class="sxs-lookup"><span data-stu-id="74ec9-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="74ec9-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="74ec9-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="74ec9-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="74ec9-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="74ec9-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="74ec9-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="74ec9-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span><span class="sxs-lookup"><span data-stu-id="74ec9-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-894">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="74ec9-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-895">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-896">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-897">Último código de error que el dispositivo lógico informa.</span><span class="sxs-lookup"><span data-stu-id="74ec9-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="74ec9-898">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-899">**Local**</span><span class="sxs-lookup"><span data-stu-id="74ec9-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-900">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-901">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-902">Si es **true**, la impresora no está conectada a una red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="74ec9-903">Si las propiedades **local** y de **red** están establecidas en **true**, la impresora es una impresora de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-904">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="74ec9-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-905">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-906">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-907">Ubicación física de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-907">Physical location of the printer.</span></span>

<span data-ttu-id="74ec9-908">Ejemplo: Bldg.</span><span class="sxs-lookup"><span data-stu-id="74ec9-908">Example: Bldg.</span></span> <span data-ttu-id="74ec9-909">38, habitación 1164</span><span class="sxs-lookup"><span data-stu-id="74ec9-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-910">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="74ec9-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-911">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-912">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-913">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-914">Tecnología de marcado que utiliza la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="74ec9-915">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-916">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-917">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="74ec9-918">**LED electrográfico** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="74ec9-919">**Láser electrográfico** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="74ec9-920">**Otra fotografía** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="74ec9-921">**Impacto** de la matriz de puntos de encabezado de movimiento</span><span class="sxs-lookup"><span data-stu-id="74ec9-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="74ec9-922">**24pin de matriz de puntos de encabezado de movimiento impactante** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="74ec9-923">La **matriz de puntos de encabezado de movimiento de impacto** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="74ec9-924">La **cabeza de movimiento de impacto está totalmente formada** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="74ec9-925">**Banda de impacto** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="74ec9-926">**Impacto en otros** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="74ec9-927">**Inyección de tinta acuosa** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="74ec9-928">**Inyección de tinta sólida** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="74ec9-929">**Inyección de tinta** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="74ec9-930">**Lápiz** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="74ec9-931">**Transferencia térmica** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="74ec9-932">**Sensible térmica** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="74ec9-933">**Difusión térmica** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="74ec9-934">**Otro térmico** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="74ec9-935">**Electroerosión** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="74ec9-936">**Electrostática** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="74ec9-937">**Microficha fotográfica** (22)</span><span class="sxs-lookup"><span data-stu-id="74ec9-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="74ec9-938">**Filmadora fotográfica** (23)</span><span class="sxs-lookup"><span data-stu-id="74ec9-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="74ec9-939">**Otros fotográficos** (24)</span><span class="sxs-lookup"><span data-stu-id="74ec9-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="74ec9-940">Desposición de la **iones** (25)</span><span class="sxs-lookup"><span data-stu-id="74ec9-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="74ec9-941">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="74ec9-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="74ec9-942">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="74ec9-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-943">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="74ec9-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-944">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-945">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-946">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. copias")</span><span class="sxs-lookup"><span data-stu-id="74ec9-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-947">Número máximo de copias que la impresora puede producir para un trabajo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="74ec9-948">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-949">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="74ec9-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-950">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-951">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-952">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="74ec9-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-953">Número máximo de páginas de secuencia de impresión que la impresora puede representar en una hoja de medios, como papel.</span><span class="sxs-lookup"><span data-stu-id="74ec9-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="74ec9-954">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-955">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-956">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-957">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-958">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. jobs"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="74ec9-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-959">Trabajo más grande como un flujo de bytes, en kilobytes, que la impresora puede aceptar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="74ec9-960">Un valor de 0 (cero) indica que no se ha establecido ningún límite.</span><span class="sxs-lookup"><span data-stu-id="74ec9-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="74ec9-961">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-962">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-963">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-964">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-965">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impresora CIM**](cim-printer.md). LanguagesSupported "," CIM \_ PrintJob. MimeTypes "," CIM \_ PrintService. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-966">Matriz de explicaciones detalladas del tipo MIME que admite la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="74ec9-967">Si se proporcionan datos, el valor 47 ("MIME") debe incluirse en la propiedad **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="74ec9-968">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-969">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="74ec9-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-970">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-971">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-972">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="74ec9-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-973">Nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-973">Name of the printer.</span></span>

<span data-ttu-id="74ec9-974">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-975">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-976">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-977">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-978">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-979">Matriz de idiomas admitidos para las cadenas que la impresora utiliza para la salida de información de administración.</span><span class="sxs-lookup"><span data-stu-id="74ec9-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="74ec9-980">Debe ajustarse a [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span><span class="sxs-lookup"><span data-stu-id="74ec9-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="74ec9-981">Por ejemplo, "en" se utiliza para inglés.</span><span class="sxs-lookup"><span data-stu-id="74ec9-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="74ec9-982">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-983">**Network**</span><span class="sxs-lookup"><span data-stu-id="74ec9-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-984">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-985">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-986">Si es **true**, la impresora es una impresora de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="74ec9-987">Si las propiedades **local** y de **red** están establecidas en **true**, la impresora es una impresora de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-988">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-989">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-990">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-991">Matriz de los tipos de papel que admite la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="74ec9-992">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="74ec9-995"><span id="A"></span><span id="a"></span>**A** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="74ec9-996"><span id="B"></span><span id="b"></span>**B** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="74ec9-997"><span id="C"></span><span id="c"></span>**C** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="74ec9-998"><span id="D"></span><span id="d"></span>**D** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="74ec9-999"><span id="E"></span><span id="e"></span>**E** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="74ec9-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letra** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="74ec9-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="74ec9-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-Envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="74ec9-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-Envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="74ec9-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-número-10-sobre** (11)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="74ec9-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-Envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="74ec9-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-Envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="74ec9-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-Envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="74ec9-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-número-9-sobre** (15)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="74ec9-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-Envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="74ec9-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-Envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="74ec9-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="74ec9-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="74ec9-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="74ec9-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="74ec9-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="74ec9-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="74ec9-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="74ec9-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="74ec9-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="74ec9-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="74ec9-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="74ec9-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="74ec9-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="74ec9-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="74ec9-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="74ec9-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="74ec9-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="74ec9-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="74ec9-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="74ec9-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="74ec9-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="74ec9-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="74ec9-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="74ec9-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1035">C2</span><span class="sxs-lookup"><span data-stu-id="74ec9-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="74ec9-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1037">C3</span><span class="sxs-lookup"><span data-stu-id="74ec9-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="74ec9-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1039">C4</span><span class="sxs-lookup"><span data-stu-id="74ec9-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="74ec9-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1041">C5</span><span class="sxs-lookup"><span data-stu-id="74ec9-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="74ec9-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1043">C6</span><span class="sxs-lookup"><span data-stu-id="74ec9-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="74ec9-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1045">C7</span><span class="sxs-lookup"><span data-stu-id="74ec9-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="74ec9-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Designación ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1047">C8</span><span class="sxs-lookup"><span data-stu-id="74ec9-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="74ec9-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="74ec9-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="74ec9-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="74ec9-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="74ec9-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="74ec9-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="74ec9-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="74ec9-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="74ec9-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="74ec9-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="74ec9-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="74ec9-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="74ec9-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="74ec9-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="74ec9-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="74ec9-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="74ec9-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="74ec9-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="74ec9-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1067">JIS B8</span><span class="sxs-lookup"><span data-stu-id="74ec9-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="74ec9-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1069">JIS B9</span><span class="sxs-lookup"><span data-stu-id="74ec9-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="74ec9-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Letra na** (59)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1071">JIS B10</span><span class="sxs-lookup"><span data-stu-id="74ec9-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="74ec9-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-legal** (60)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="74ec9-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**Sobre B4** (61)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="74ec9-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**Sobre B5** (62)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="74ec9-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**Sobre C3** (63)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="74ec9-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**Sobre C4** (64)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="74ec9-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**Sobre C5** (65)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="74ec9-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**Sobre C6** (66)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="74ec9-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="74ec9-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Sobre monarca** (68)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="74ec9-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Ejecutivo** (69)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="74ec9-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="74ec9-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Factura** (71)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="74ec9-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Libro de contabilidad** (72)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="74ec9-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Cuarto** (73)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-1086">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1087">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1088">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1089">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ PrintService. PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1090">Matriz de tipos de papel que están disponibles actualmente en la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="74ec9-1091">Cada cadena se debe expresar en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 10175, que se resume en el Apéndice C de [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="74ec9-1092">Cualquier tamaño de papel identificado en esta propiedad también debe aparecer en la propiedad **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="74ec9-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="74ec9-1093">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="74ec9-1094">Ejemplo: ISO-A4-color</span><span class="sxs-lookup"><span data-stu-id="74ec9-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1095">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1096">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1097">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1098">Parámetros opcionales para el procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="74ec9-1099">Ejemplo: "copias = 2"</span><span class="sxs-lookup"><span data-stu-id="74ec9-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1101">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1102">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1103">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1104">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="74ec9-1105">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="74ec9-1106">Ejemplo: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="74ec9-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1107">**PortName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1108">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1109">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1110">Puerto que se usa para transmitir datos a una impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="74ec9-1111">Si una impresora está conectada a más de un puerto, los nombres de cada puerto se separan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="74ec9-1112">Ejemplo: LPT1:, LPT2:, LPT3:</span><span class="sxs-lookup"><span data-stu-id="74ec9-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1113">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1114">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1116">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="74ec9-1117">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="74ec9-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="74ec9-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="74ec9-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1122">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="74ec9-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1124">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="74ec9-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1126">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="74ec9-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="74ec9-1127">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="74ec9-1128">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="74ec9-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1130">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="74ec9-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1132">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="74ec9-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="74ec9-1133">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-1134">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1137">Si **es true**, se puede administrar la eficacia del dispositivo, lo que significa que se puede poner en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="74ec9-1138">La propiedad no indica que las características de administración de energía están habilitadas, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="74ec9-1139">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1140">**PrinterPaperNames**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1141">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1143">Matriz de tamaños de papel que admite la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="74ec9-1144">Los nombres especificados por la impresora se usan para representar los tamaños de papel compatibles.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="74ec9-1145">Ejemplo: B5 (JIS)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1146">**PrinterState**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1149">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1150">Uno de los Estados posibles relacionados con esta impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="74ec9-1151">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1151">This property is obsolete.</span></span> <span data-ttu-id="74ec9-1152">En lugar de esta propiedad, use **PrinterStatus**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="74ec9-1153">0</span><span class="sxs-lookup"><span data-stu-id="74ec9-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1154">Inactivo: para obtener más información, vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1155">1</span><span class="sxs-lookup"><span data-stu-id="74ec9-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1156">En pausa</span><span class="sxs-lookup"><span data-stu-id="74ec9-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1157">2</span><span class="sxs-lookup"><span data-stu-id="74ec9-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1158">Error</span><span class="sxs-lookup"><span data-stu-id="74ec9-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1159">3</span><span class="sxs-lookup"><span data-stu-id="74ec9-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1160">Eliminación pendiente</span><span class="sxs-lookup"><span data-stu-id="74ec9-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1161">4</span><span class="sxs-lookup"><span data-stu-id="74ec9-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1162">Atasco de papel</span><span class="sxs-lookup"><span data-stu-id="74ec9-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1163">5</span><span class="sxs-lookup"><span data-stu-id="74ec9-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1164">Papel de salida</span><span class="sxs-lookup"><span data-stu-id="74ec9-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1165">6</span><span class="sxs-lookup"><span data-stu-id="74ec9-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1166">Alimentación manual</span><span class="sxs-lookup"><span data-stu-id="74ec9-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1167">7</span><span class="sxs-lookup"><span data-stu-id="74ec9-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1168">Problema de papel</span><span class="sxs-lookup"><span data-stu-id="74ec9-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1169">8</span><span class="sxs-lookup"><span data-stu-id="74ec9-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1170">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="74ec9-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1171">9</span><span class="sxs-lookup"><span data-stu-id="74ec9-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1172">E/s activa</span><span class="sxs-lookup"><span data-stu-id="74ec9-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1173">10</span><span class="sxs-lookup"><span data-stu-id="74ec9-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1174">Ocupado</span><span class="sxs-lookup"><span data-stu-id="74ec9-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1175">11</span><span class="sxs-lookup"><span data-stu-id="74ec9-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1176">Impresión</span><span class="sxs-lookup"><span data-stu-id="74ec9-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1177">12</span><span class="sxs-lookup"><span data-stu-id="74ec9-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1178">Bandeja de salida llena</span><span class="sxs-lookup"><span data-stu-id="74ec9-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1179">13</span><span class="sxs-lookup"><span data-stu-id="74ec9-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1180">No disponible</span><span class="sxs-lookup"><span data-stu-id="74ec9-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1181">14</span><span class="sxs-lookup"><span data-stu-id="74ec9-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1182">En espera</span><span class="sxs-lookup"><span data-stu-id="74ec9-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1183">15</span><span class="sxs-lookup"><span data-stu-id="74ec9-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1184">Processing</span><span class="sxs-lookup"><span data-stu-id="74ec9-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1185">16</span><span class="sxs-lookup"><span data-stu-id="74ec9-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1186">Inicialización</span><span class="sxs-lookup"><span data-stu-id="74ec9-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1187">17</span><span class="sxs-lookup"><span data-stu-id="74ec9-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1188">Preparando</span><span class="sxs-lookup"><span data-stu-id="74ec9-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1189">18</span><span class="sxs-lookup"><span data-stu-id="74ec9-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1190">Tóner bajo</span><span class="sxs-lookup"><span data-stu-id="74ec9-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1191">19</span><span class="sxs-lookup"><span data-stu-id="74ec9-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1192">Sin tóner</span><span class="sxs-lookup"><span data-stu-id="74ec9-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1193">20</span><span class="sxs-lookup"><span data-stu-id="74ec9-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1194">Página aparcan</span><span class="sxs-lookup"><span data-stu-id="74ec9-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1195">21</span><span class="sxs-lookup"><span data-stu-id="74ec9-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1196">Intervención del usuario requerida</span><span class="sxs-lookup"><span data-stu-id="74ec9-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1197">22</span><span class="sxs-lookup"><span data-stu-id="74ec9-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1198">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="74ec9-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1199">23</span><span class="sxs-lookup"><span data-stu-id="74ec9-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1200">Puerta abierta</span><span class="sxs-lookup"><span data-stu-id="74ec9-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1201">24</span><span class="sxs-lookup"><span data-stu-id="74ec9-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1202">Servidor \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="74ec9-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1203">25</span><span class="sxs-lookup"><span data-stu-id="74ec9-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="74ec9-1204">Ahorro de energía</span><span class="sxs-lookup"><span data-stu-id="74ec9-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-1205">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1206">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1208">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1209">Información de estado de una impresora diferente de la especificada en la propiedad **disponibilidad** del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="74ec9-1210">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="74ec9-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1214">Inactivo: para obtener más información, vea la sección Comentarios a continuación.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="74ec9-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Impresión** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="74ec9-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Preparación** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74ec9-1217">Preparando</span><span class="sxs-lookup"><span data-stu-id="74ec9-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="74ec9-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Impresión detenida** (6)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="74ec9-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (7)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-1220">**PrintJobDataType**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1222">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1223">Tipo de datos de un trabajo de impresión en espera del dispositivo de impresión basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1224">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1227">Nombre del administrador de trabajos de impresión que controla los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="74ec9-1228">Ejemplo: SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="74ec9-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1229">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1230">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1231">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1232">Prioridad de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1232">Priority of the printer.</span></span> <span data-ttu-id="74ec9-1233">Los trabajos en una impresora de prioridad más alta se programan en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1234">**Publicado**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1235">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1236">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1237">Si es **true**, la impresora se publica en el servicio de directorio de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1238">**En cola**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1239">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1240">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1241">Si **es true**, el búfer de la impresora y pone en cola los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1242">**RawOnly**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1243">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1245">Si **es true**, la impresora solo acepta los datos sin procesar que se van a poner en cola.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1246">**SeparatorFile**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1248">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1249">Nombre del archivo utilizado para crear una página separadora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="74ec9-1250">Esta página se utiliza para separar los trabajos de impresión que se envían a la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1254">Nombre del servidor que controla la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="74ec9-1255">Si esta cadena es **null**, la impresora se controla localmente.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1256">**Compartido**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1257">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1258">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1259">Si es **true**, la impresora está disponible como un recurso compartido de red.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1260">**ShareName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1263">Nombre del recurso compartido del dispositivo de impresión basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="74ec9-1264">Ejemplo: " \\ \\ servidorimpresión1 \\ Printer2"</span><span class="sxs-lookup"><span data-stu-id="74ec9-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1265">**SpoolEnabled**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1266">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1268">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1269">Esta propiedad está obsoleta; No use.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="74ec9-1270">Si es **true**, la cola de impresión está habilitada para la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1272">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1273">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1274">Fecha y hora en que una impresora puede empezar a imprimir un trabajo: Si la impresora está limitada a imprimirse en momentos concretos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="74ec9-1275">Este valor se expresa como el tiempo transcurrido desde 12:00 AM GMT (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1276">**Estado**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1279">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1280">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1280">Current status of the object.</span></span> <span data-ttu-id="74ec9-1281">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="74ec9-1282">Los Estados operativos incluyen: **correcto**, **degradado** y **Pred FAIL** (un elemento, como una unidad de disco duro habilitada para Smart, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="74ec9-1283">Los Estados no operativo incluyen: **error**, **Inicio**, **detención** y **servicio**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="74ec9-1284">Este último **servicio** se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="74ec9-1285">No todo el trabajo está en línea, pero el elemento administrado no es **correcto** ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="74ec9-1286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="74ec9-1287">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="74ec9-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="74ec9-1288">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="74ec9-1289">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="74ec9-1290">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-1291">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="74ec9-1292">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="74ec9-1293">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="74ec9-1294">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="74ec9-1295">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="74ec9-1296">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="74ec9-1297">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="74ec9-1298">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="74ec9-1299">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1301">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1303">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1304">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1304">State of the logical device.</span></span> <span data-ttu-id="74ec9-1305">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (**no aplicable**).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="74ec9-1306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74ec9-1307">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74ec9-1308">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="74ec9-1309">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="74ec9-1310">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="74ec9-1311">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74ec9-1312">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1315">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1316">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="74ec9-1317">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1318">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1321">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74ec9-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1322">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1322">Name of the scoping system.</span></span>

<span data-ttu-id="74ec9-1323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1324">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1325">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1327">Fecha y hora en que se restableció por última vez la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="74ec9-1328">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1329">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1330">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1331">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1332">Fecha y hora en que una impresora puede imprimir el último trabajo: Si la impresora está limitada a imprimirse en momentos concretos.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="74ec9-1333">Este valor se expresa como el tiempo transcurrido desde 12:00 AM GMT (hora del meridiano de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1337">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](../wmisdk/standard-qualifiers.md) ("píxeles por pulgada")</span><span class="sxs-lookup"><span data-stu-id="74ec9-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1338">Resolución vertical, en píxeles por pulgada, de la impresora.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="74ec9-1339">Esta propiedad se hereda de [**la \_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="74ec9-1340">**WorkOffline**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74ec9-1341">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74ec9-1342">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74ec9-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="74ec9-1343">Si es **true**, puede poner en cola los trabajos de impresión en el equipo cuando la impresora está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74ec9-1344">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74ec9-1344">Remarks</span></span>

<span data-ttu-id="74ec9-1345">La clase de **\_ impresora de Win32** se deriva de la [**\_ impresora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="74ec9-1346">Antes de llamar a [**SWbemObject \_ . put**](../wmisdk/swbemobject-put-.md) o [**IWbemServices::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) para una instancia de **\_ impresora de Win32** , el privilegio **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** para Visual Basic y LoadDriver para los monikers de scripting) debe estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="74ec9-1347">Para obtener más información, vea [**constantes de privilegios**](../wmisdk/privilege-constants.md) y [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="74ec9-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="74ec9-1348">En el ejemplo de código de VBScript siguiente se muestra cómo habilitar el privilegio **SetLoadDriverPrivilege** en el script.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="74ec9-1349">Para trabajar con clústeres de impresora de MSCS, use el prnadmin.dll ensamblado, o bien el espacio de nombres [System. Printing](/dotnet/api/system.printing) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="74ec9-1350">Windows usa las credenciales del usuario que ejecuta el script para determinar cuáles son las impresoras disponibles.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="74ec9-1351">Por lo tanto, si está ejecutando un script de forma remota, es posible que solo pueda tener acceso a cualquier impresora que esté disponible para su cuenta de usuario en ese sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="74ec9-1352">No se puede usar la clase **\_ Printer de Win32** para impresoras en un clúster de impresión de MSCS.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="74ec9-1353">En su lugar, puede que necesite usar la herramienta PrinterAdmin (PrnAdmin.dll) o el espacio de nombres .NET Framework [System. Printing](/dotnet/api/system.printing) .</span><span class="sxs-lookup"><span data-stu-id="74ec9-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="74ec9-1354">Si va a recuperar **PrinterStatus** = 3 o **PrinterState** = 0, es posible que el controlador de impresora no alimente información precisa en WMI.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="74ec9-1355">WMI recupera la información de la impresora del proceso de spoolsv.exe.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="74ec9-1356">Es posible que el controlador de impresora no informe de su estado al administrador de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="74ec9-1357">En este caso, **la \_ impresora de Win32** informa de la impresora como **inactiva**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="74ec9-1358">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="74ec9-1358">Examples</span></span>

<span data-ttu-id="74ec9-1359">En el ejemplo de [creación de un dibujo de configuración de equipo con Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell en la galería de TechNet se usa la **\_ impresora Win32** para interactuar con el modelo de automatización de Visio con el fin de crear un dibujo de Visio.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="74ec9-1360">El [script de información del equipo remoto de PowerShell](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) usa una serie de clases, incluida la **\_ impresora Win32**, para recuperar información acerca de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="74ec9-1361">En el siguiente ejemplo de código de PowerShell se muestra cómo determinar la impresora predeterminada del equipo local.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="74ec9-1362">En el siguiente ejemplo de código de VBScript se describe cómo recuperar estadísticas de impresora de instancias de la **\_ impresora Win32**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="74ec9-1363">En el siguiente ejemplo de código Perl se describe cómo recuperar estadísticas de impresora de instancias de la **\_ impresora Win32**.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


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



<span data-ttu-id="74ec9-1364">En el ejemplo de código de VBScript siguiente se muestra cómo obtener el nombre de la impresora predeterminada de un equipo.</span><span class="sxs-lookup"><span data-stu-id="74ec9-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="74ec9-1365">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74ec9-1365">Requirements</span></span>



| <span data-ttu-id="74ec9-1366">Requisito</span><span class="sxs-lookup"><span data-stu-id="74ec9-1366">Requirement</span></span> | <span data-ttu-id="74ec9-1367">Value</span><span class="sxs-lookup"><span data-stu-id="74ec9-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ec9-1368">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ec9-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="74ec9-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74ec9-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="74ec9-1370">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74ec9-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="74ec9-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74ec9-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="74ec9-1372">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74ec9-1372">Namespace</span></span><br/>                | <span data-ttu-id="74ec9-1373">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="74ec9-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="74ec9-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="74ec9-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74ec9-1375"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74ec9-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="74ec9-1376">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74ec9-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ec9-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74ec9-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="74ec9-1378">Vea también</span><span class="sxs-lookup"><span data-stu-id="74ec9-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ec9-1379">**\_Impresora CIM**</span><span class="sxs-lookup"><span data-stu-id="74ec9-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="74ec9-1380">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="74ec9-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="74ec9-1381">Tareas de WMI: impresoras e impresión</span><span class="sxs-lookup"><span data-stu-id="74ec9-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
