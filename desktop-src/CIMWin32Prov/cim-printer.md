---
description: La \_ clase de impresora CIM representa las capacidades y la administración del dispositivo lógico de impresora.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: CIM_Printer (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153516"
---
# <a name="cim_printer-class"></a><span data-ttu-id="1d14c-103">\_Clase Printer de CIM</span><span class="sxs-lookup"><span data-stu-id="1d14c-103">CIM\_Printer class</span></span>

<span data-ttu-id="1d14c-104">La clase de **\_ impresora CIM** representa las capacidades y la administración del dispositivo lógico de impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d14c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1d14c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d14c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1d14c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d14c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1d14c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1d14c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1d14c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d14c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d14c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="1d14c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d14c-110">Members</span></span>

<span data-ttu-id="1d14c-111">La clase de **\_ impresora CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1d14c-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="1d14c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d14c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d14c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d14c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d14c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d14c-114">Methods</span></span>

<span data-ttu-id="1d14c-115">La clase de **\_ impresora CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1d14c-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="1d14c-116">Método</span><span class="sxs-lookup"><span data-stu-id="1d14c-116">Method</span></span>                                                             | <span data-ttu-id="1d14c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d14c-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d14c-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="1d14c-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="1d14c-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d14c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="1d14c-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="1d14c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="1d14c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1d14c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="1d14c-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1d14c-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="1d14c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1d14c-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d14c-124">Properties</span></span>

<span data-ttu-id="1d14c-125">La clase de **\_ impresora CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d14c-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d14c-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="1d14c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-130">Availability and status of the device.</span></span>

<span data-ttu-id="1d14c-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1d14c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-135">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="1d14c-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1d14c-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1d14c-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d14c-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1d14c-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="1d14c-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1d14c-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="1d14c-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1d14c-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d14c-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1d14c-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1d14c-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1d14c-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-146">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="1d14c-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1d14c-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-148">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1d14c-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-150">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="1d14c-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1d14c-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1d14c-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-153">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="1d14c-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1d14c-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-155">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="1d14c-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1d14c-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-157">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1d14c-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-159">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1d14c-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-161">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="1d14c-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-162">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="1d14c-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-163">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-165">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="1d14c-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-166">Describe todas las hojas de trabajo que están disponibles en la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="1d14c-167">También se puede usar para describir el banner que una impresora puede proporcionar al principio de cada trabajo, o puede describir otras opciones especificadas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1d14c-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-168">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="1d14c-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-169">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-171">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ impresora CIM**. CapabilityDescriptions "," CIM \_ PrintJob. Finishing "," CIM \_ PrintService. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-172">Capacidades de impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="1d14c-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="1d14c-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="1d14c-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="1d14c-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="1d14c-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="1d14c-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="1d14c-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="1d14c-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="1d14c-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="1d14c-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="1d14c-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-186">Un lado</span><span class="sxs-lookup"><span data-stu-id="1d14c-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="1d14c-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-188">Borde largo a dos caras</span><span class="sxs-lookup"><span data-stu-id="1d14c-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="1d14c-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-190">Borde corto a dos caras</span><span class="sxs-lookup"><span data-stu-id="1d14c-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="1d14c-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="1d14c-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="1d14c-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="1d14c-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="1d14c-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-196">Calidad alta</span><span class="sxs-lookup"><span data-stu-id="1d14c-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="1d14c-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-198">Calidad normal</span><span class="sxs-lookup"><span data-stu-id="1d14c-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="1d14c-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-200">Calidad baja</span><span class="sxs-lookup"><span data-stu-id="1d14c-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-201">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1d14c-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-202">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-204">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ impresora CIM**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-205">Cadenas de forma libre que proporcionan explicaciones detalladas para cualquiera de las características de impresora indicadas en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="1d14c-206">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="1d14c-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="1d14c-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1d14c-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-210">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1d14c-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-211">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d14c-211">Short textual description of the object.</span></span>

<span data-ttu-id="1d14c-212">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-213">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-214">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-216">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. charset"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-217">Juegos de caracteres disponibles para la salida de texto relacionado con la administración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="1d14c-218">Las cadenas proporcionadas en esta propiedad deben cumplir la semántica y la sintaxis que se especifican en la sección 4.1.2 ("charset Parameter") en RFC 2046 (MIME Part 2) y contenidas en el registro de juegos de caracteres de IANA.</span><span class="sxs-lookup"><span data-stu-id="1d14c-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="1d14c-219">Entre los ejemplos se incluyen "UTF-8", "US-ASCII" y "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="1d14c-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d14c-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-221">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-223">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d14c-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-224">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="1d14c-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1d14c-225">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1d14c-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1d14c-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-228">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d14c-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1d14c-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1d14c-230">(1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-231">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d14c-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d14c-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1d14c-233">(2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1d14c-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1d14c-235">(3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-236">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="1d14c-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d14c-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1d14c-238">(4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-239">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d14c-239">Device is not working properly.</span></span> <span data-ttu-id="1d14c-240">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="1d14c-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1d14c-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1d14c-242">(5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-243">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="1d14c-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1d14c-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1d14c-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-246">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1d14c-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1d14c-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1d14c-248">(7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1d14c-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1d14c-250">(8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-251">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1d14c-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1d14c-253">(9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-254">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d14c-254">Device is not working properly.</span></span> <span data-ttu-id="1d14c-255">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1d14c-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1d14c-257">(10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-258">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="1d14c-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1d14c-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1d14c-260">(11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-261">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1d14c-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1d14c-263">(12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-264">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="1d14c-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1d14c-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1d14c-266">(13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-267">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1d14c-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1d14c-269">(14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-270">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1d14c-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1d14c-272">(15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-273">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="1d14c-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1d14c-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1d14c-275">(16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-276">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1d14c-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1d14c-278">(17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-279">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="1d14c-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d14c-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1d14c-281">(18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-282">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1d14c-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1d14c-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1d14c-284">(19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d14c-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1d14c-286">(20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-287">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1d14c-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1d14c-289">(21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-290">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d14c-290">System failure.</span></span> <span data-ttu-id="1d14c-291">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="1d14c-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1d14c-292">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1d14c-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1d14c-294">(22)</span><span class="sxs-lookup"><span data-stu-id="1d14c-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-295">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1d14c-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1d14c-297">(23)</span><span class="sxs-lookup"><span data-stu-id="1d14c-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-298">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d14c-298">System failure.</span></span> <span data-ttu-id="1d14c-299">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="1d14c-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1d14c-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1d14c-301">(24)</span><span class="sxs-lookup"><span data-stu-id="1d14c-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-302">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="1d14c-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d14c-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d14c-304">(25)</span><span class="sxs-lookup"><span data-stu-id="1d14c-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-305">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d14c-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d14c-307">(26)</span><span class="sxs-lookup"><span data-stu-id="1d14c-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-308">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1d14c-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1d14c-310">(27)</span><span class="sxs-lookup"><span data-stu-id="1d14c-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-311">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="1d14c-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1d14c-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1d14c-313">(28)</span><span class="sxs-lookup"><span data-stu-id="1d14c-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-314">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="1d14c-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1d14c-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1d14c-316">(29)</span><span class="sxs-lookup"><span data-stu-id="1d14c-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-317">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-317">Device is disabled.</span></span> <span data-ttu-id="1d14c-318">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="1d14c-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1d14c-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1d14c-320">(30)</span><span class="sxs-lookup"><span data-stu-id="1d14c-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-321">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="1d14c-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d14c-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d14c-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1d14c-323">31</span><span class="sxs-lookup"><span data-stu-id="1d14c-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-324">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d14c-324">Device is not working properly.</span></span> <span data-ttu-id="1d14c-325">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="1d14c-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-326">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1d14c-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-327">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d14c-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-329">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d14c-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-330">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1d14c-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1d14c-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d14c-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-335">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d14c-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-336">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="1d14c-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d14c-337">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1d14c-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1d14c-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-339">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d14c-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-340">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-342">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-343">Finalizaciones y otras capacidades de la impresora que están actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="1d14c-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="1d14c-344">Cada entrada de esta propiedad también debe aparecer en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="1d14c-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="1d14c-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="1d14c-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="1d14c-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="1d14c-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="1d14c-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="1d14c-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="1d14c-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="1d14c-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="1d14c-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="1d14c-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-358">Un lado</span><span class="sxs-lookup"><span data-stu-id="1d14c-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="1d14c-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-360">Borde largo a dos caras</span><span class="sxs-lookup"><span data-stu-id="1d14c-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="1d14c-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-362">Borde corto a dos caras</span><span class="sxs-lookup"><span data-stu-id="1d14c-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="1d14c-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="1d14c-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="1d14c-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="1d14c-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="1d14c-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-368">Calidad alta</span><span class="sxs-lookup"><span data-stu-id="1d14c-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="1d14c-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-370">Calidad normal</span><span class="sxs-lookup"><span data-stu-id="1d14c-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="1d14c-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-372">Calidad baja</span><span class="sxs-lookup"><span data-stu-id="1d14c-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-373">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="1d14c-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-376">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-377">Juego de caracteres actual usado para la salida de texto relacionado con la administración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="1d14c-378">El juego de caracteres descrito por esta propiedad también debe aparecer en la propiedad **CharsetsSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="1d14c-379">La cadena especificada por esta propiedad debe ajustarse a la semántica y la sintaxis especificadas por la sección 4.1.2 ("parámetro charset") en RFC 2046 (MIME parte 2) y contenidas en el registro de juegos de caracteres de IANA.</span><span class="sxs-lookup"><span data-stu-id="1d14c-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="1d14c-380">Entre los ejemplos se incluyen "UTF-8", "US-ASCII" y "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="1d14c-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-381">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="1d14c-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-382">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-384">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**. LanguagesSupported "," CIM \_ printer. CurrentMimeType ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-385">Idioma de impresora actual que se está usando; el lenguaje también debe aparecer en la propiedad **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-386">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-387">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="1d14c-388">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="1d14c-389">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="1d14c-390">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="1d14c-391">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="1d14c-392">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="1d14c-393">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="1d14c-394">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="1d14c-395">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="1d14c-396">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="1d14c-397">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="1d14c-398">**Interpress** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="1d14c-399">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="1d14c-400">**Datos de línea** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="1d14c-401">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="1d14c-402">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="1d14c-403">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="1d14c-404">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="1d14c-405">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="1d14c-406">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="1d14c-407">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="1d14c-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="1d14c-408">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="1d14c-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="1d14c-409">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="1d14c-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="1d14c-410">**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="1d14c-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="1d14c-411">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="1d14c-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="1d14c-412">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="1d14c-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="1d14c-413">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="1d14c-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="1d14c-414">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="1d14c-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="1d14c-415">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="1d14c-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="1d14c-416">**Texto simple** (31)</span><span class="sxs-lookup"><span data-stu-id="1d14c-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="1d14c-417">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="1d14c-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="1d14c-418">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="1d14c-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="1d14c-419">**Impress** (34)</span><span class="sxs-lookup"><span data-stu-id="1d14c-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="1d14c-420">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="1d14c-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="1d14c-421">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="1d14c-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="1d14c-422">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="1d14c-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d14c-423">**Automática** (38)</span><span class="sxs-lookup"><span data-stu-id="1d14c-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="1d14c-424">**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="1d14c-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="1d14c-425">**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="1d14c-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="1d14c-426">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="1d14c-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1d14c-427">**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="1d14c-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="1d14c-428">**Mayúsculas** (43)</span><span class="sxs-lookup"><span data-stu-id="1d14c-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="1d14c-429">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="1d14c-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="1d14c-430">**Pantallas LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="1d14c-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="1d14c-431">**Dices** (46)</span><span class="sxs-lookup"><span data-stu-id="1d14c-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="1d14c-432">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="1d14c-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-433">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="1d14c-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-436">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-437">Tipo MIME actualmente en uso por la impresora cuando la propiedad **CurrentLanguage** está establecida para indicar que un tipo MIME está en uso.</span><span class="sxs-lookup"><span data-stu-id="1d14c-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-438">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="1d14c-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-441">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-442">Idioma actual en uso por la impresora para la administración.</span><span class="sxs-lookup"><span data-stu-id="1d14c-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="1d14c-443">El idioma que se muestra aquí también debe aparecer en **NaturalLanguagesSupported**.</span><span class="sxs-lookup"><span data-stu-id="1d14c-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-444">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="1d14c-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-447">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-448">Tipo de papel actualmente en uso por la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="1d14c-449">La cadena se debe expresar en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 10175, que también se resume en el Apéndice C de RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="1d14c-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-450">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d14c-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-451">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-453">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-454">Finalizaciones predeterminadas y otras capacidades de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="1d14c-455">Cada entrada de esta propiedad también debe aparecer en la matriz de **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="1d14c-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impresión en color** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="1d14c-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impresión dúplex** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="1d14c-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copias** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="1d14c-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Intercalación** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="1d14c-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grapado** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="1d14c-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impresión de transparencia** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="1d14c-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perforación** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="1d14c-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cubierta** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="1d14c-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="1d14c-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impresión en blanco y negro** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="1d14c-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lado** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-469">Un lado</span><span class="sxs-lookup"><span data-stu-id="1d14c-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="1d14c-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borde largo de dos caras** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-471">Borde largo a dos caras</span><span class="sxs-lookup"><span data-stu-id="1d14c-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="1d14c-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borde inferior de dos caras** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-473">Borde corto a dos caras</span><span class="sxs-lookup"><span data-stu-id="1d14c-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="1d14c-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Vertical** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="1d14c-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Horizontal** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="1d14c-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Vertical inversa** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="1d14c-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Horizontal inversa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="1d14c-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Calidad alta** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-479">Calidad alta</span><span class="sxs-lookup"><span data-stu-id="1d14c-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="1d14c-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Calidad normal** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-481">Calidad normal</span><span class="sxs-lookup"><span data-stu-id="1d14c-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="1d14c-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Calidad baja** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-483">Calidad baja</span><span class="sxs-lookup"><span data-stu-id="1d14c-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-484">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="1d14c-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-485">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-487">Número de copias que producirá un solo trabajo, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="1d14c-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="1d14c-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-489">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-491">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**. LanguagesSupported "," CIM \_ printer. DefaultMimeType ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-492">Idioma de impresora predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-492">Default printer language.</span></span> <span data-ttu-id="1d14c-493">El lenguaje también debe aparecer en la propiedad **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-494">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-495">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="1d14c-496">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="1d14c-497">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="1d14c-498">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="1d14c-499">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="1d14c-500">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="1d14c-501">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="1d14c-502">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="1d14c-503">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="1d14c-504">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="1d14c-505">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="1d14c-506">**Interpress** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="1d14c-507">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="1d14c-508">**Datos de línea** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="1d14c-509">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="1d14c-510">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="1d14c-511">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="1d14c-512">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="1d14c-513">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="1d14c-514">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="1d14c-515">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="1d14c-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="1d14c-516">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="1d14c-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="1d14c-517">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="1d14c-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="1d14c-518">**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="1d14c-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="1d14c-519">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="1d14c-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="1d14c-520">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="1d14c-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="1d14c-521">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="1d14c-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="1d14c-522">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="1d14c-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="1d14c-523">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="1d14c-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="1d14c-524">**Texto simple** (31)</span><span class="sxs-lookup"><span data-stu-id="1d14c-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="1d14c-525">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="1d14c-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="1d14c-526">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="1d14c-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="1d14c-527">**Impress** (34)</span><span class="sxs-lookup"><span data-stu-id="1d14c-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="1d14c-528">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="1d14c-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="1d14c-529">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="1d14c-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="1d14c-530">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="1d14c-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d14c-531">**Automática** (38)</span><span class="sxs-lookup"><span data-stu-id="1d14c-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="1d14c-532">**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="1d14c-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="1d14c-533">**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="1d14c-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="1d14c-534">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="1d14c-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1d14c-535">**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="1d14c-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="1d14c-536">**Mayúsculas** (43)</span><span class="sxs-lookup"><span data-stu-id="1d14c-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="1d14c-537">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="1d14c-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="1d14c-538">**Pantallas LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="1d14c-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="1d14c-539">**Dices** (46)</span><span class="sxs-lookup"><span data-stu-id="1d14c-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="1d14c-540">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="1d14c-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-541">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="1d14c-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-542">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-543">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-544">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-545">Tipo MIME predeterminado que usa la impresora cuando la propiedad **DefaultLanguage** está establecida para indicar que un tipo MIME está en uso.</span><span class="sxs-lookup"><span data-stu-id="1d14c-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-546">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="1d14c-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-547">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-549">Número de páginas de secuencia de impresión en las que la impresora se representará en una sola hoja de medios, a menos que un trabajo especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="1d14c-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-550">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="1d14c-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-551">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-552">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-553">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-554">Tipo de papel que utilizará la impresora si PrintJob no especifica un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="1d14c-555">La cadena se debe expresar en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 10175, que también se resume en el Apéndice C de RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="1d14c-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-556">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d14c-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-557">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-558">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-559">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="1d14c-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-560">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d14c-560">Textual description of the object.</span></span>

<span data-ttu-id="1d14c-561">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-562">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="1d14c-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-563">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-564">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-565">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-566">Información de error de la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-567">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-568">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="1d14c-569">**Sin errores** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="1d14c-570">**Papel bajo** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="1d14c-571">**Sin papel** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="1d14c-572">**Tóner bajo** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="1d14c-573">**Sin tóner** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="1d14c-574">**Puerta abierta** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="1d14c-575">**Atascado** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="1d14c-576">**Sin conexión** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="1d14c-577">**Servicio solicitado** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="1d14c-578">**Bandeja de salida llena** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-579">**ID**</span><span class="sxs-lookup"><span data-stu-id="1d14c-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-580">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-581">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-582">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d14c-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-583">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d14c-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1d14c-584">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-585">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1d14c-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-586">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d14c-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-587">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-588">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1d14c-589">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1d14c-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-591">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-592">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-593">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="1d14c-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1d14c-594">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-595">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="1d14c-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-596">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-597">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1d14c-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-598">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**.**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="1d14c-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-599">Matriz que proporciona información adicional sobre el estado de error actual, indicado en la propiedad **DetectedErrorState** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="1d14c-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-601">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-602">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-603">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles por pulgada")</span><span class="sxs-lookup"><span data-stu-id="1d14c-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-604">Resolución horizontal en píxeles por pulgada.</span><span class="sxs-lookup"><span data-stu-id="1d14c-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d14c-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-606">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d14c-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-607">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-608">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-609">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d14c-609">Date and time the object was installed.</span></span> <span data-ttu-id="1d14c-610">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d14c-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1d14c-611">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-612">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="1d14c-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-613">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-614">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-615">Calificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="1d14c-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-616">Trabajos de impresora procesados desde el último restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="1d14c-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="1d14c-617">Estos trabajos se pueden procesar desde una o varias colas de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d14c-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-618">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-619">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-620">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-621">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**. MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ PrintService. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-622">Idiomas de impresión que se admiten de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="1d14c-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-623">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-624">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="1d14c-625">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="1d14c-626">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="1d14c-627">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="1d14c-628">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="1d14c-629">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="1d14c-630">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="1d14c-631">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="1d14c-632">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="1d14c-633">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="1d14c-634">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="1d14c-635">**Interpress** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="1d14c-636">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="1d14c-637">**Datos de línea** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="1d14c-638">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="1d14c-639">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="1d14c-640">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="1d14c-641">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="1d14c-642">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="1d14c-643">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="1d14c-644">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="1d14c-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="1d14c-645">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="1d14c-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="1d14c-646">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="1d14c-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="1d14c-647">**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="1d14c-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="1d14c-648">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="1d14c-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="1d14c-649">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="1d14c-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="1d14c-650">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="1d14c-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="1d14c-651">**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="1d14c-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="1d14c-652">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="1d14c-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="1d14c-653">**Texto simple** (31)</span><span class="sxs-lookup"><span data-stu-id="1d14c-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="1d14c-654">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="1d14c-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="1d14c-655">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="1d14c-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="1d14c-656">**Impress** (34)</span><span class="sxs-lookup"><span data-stu-id="1d14c-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="1d14c-657">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="1d14c-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="1d14c-658">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="1d14c-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="1d14c-659">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="1d14c-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d14c-660">**Automática** (38)</span><span class="sxs-lookup"><span data-stu-id="1d14c-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="1d14c-661">**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="1d14c-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="1d14c-662">**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="1d14c-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="1d14c-663">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="1d14c-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1d14c-664">**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="1d14c-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="1d14c-665">**Mayúsculas** (43)</span><span class="sxs-lookup"><span data-stu-id="1d14c-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="1d14c-666">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="1d14c-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="1d14c-667">**Pantallas LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="1d14c-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="1d14c-668">**Dices** (46)</span><span class="sxs-lookup"><span data-stu-id="1d14c-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="1d14c-669">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="1d14c-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="1d14c-670">**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="1d14c-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="1d14c-671">**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="1d14c-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="1d14c-672">**PCLXL** (50)</span><span class="sxs-lookup"><span data-stu-id="1d14c-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-673">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d14c-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-674">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-675">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-676">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d14c-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1d14c-677">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-678">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="1d14c-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-679">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-680">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-681">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-682">Tecnología de marcado utilizada por la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-683">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-684">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="1d14c-685">**LED electrográfico** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="1d14c-686">**Láser electrográfico** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="1d14c-687">**Otra fotografía** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="1d14c-688">**Impacto** de la matriz de puntos de encabezado de movimiento</span><span class="sxs-lookup"><span data-stu-id="1d14c-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="1d14c-689">**24pin de matriz de puntos de encabezado de movimiento impactante** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="1d14c-690">La **matriz de puntos de encabezado de movimiento de impacto** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="1d14c-691">La **cabeza de movimiento de impacto está totalmente formada** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="1d14c-692">**Banda de impacto** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="1d14c-693">**Impacto en otros** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="1d14c-694">**Inyección de tinta acuosa** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="1d14c-695">**Inyección de tinta sólida** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="1d14c-696">**Inyección de tinta** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="1d14c-697">**Lápiz** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="1d14c-698">**Transferencia térmica** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="1d14c-699">**Sensible térmica** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="1d14c-700">**Difusión térmica** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="1d14c-701">**Otro térmico** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="1d14c-702">**Electroerosión** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="1d14c-703">**Electrostática** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="1d14c-704">**Microficha fotográfica** (22)</span><span class="sxs-lookup"><span data-stu-id="1d14c-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="1d14c-705">**Filmadora fotográfica** (23)</span><span class="sxs-lookup"><span data-stu-id="1d14c-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="1d14c-706">**Otros fotográficos** (24)</span><span class="sxs-lookup"><span data-stu-id="1d14c-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="1d14c-707">Desposición de la **iones** (25)</span><span class="sxs-lookup"><span data-stu-id="1d14c-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="1d14c-708">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="1d14c-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="1d14c-709">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="1d14c-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-710">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="1d14c-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-711">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-712">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-713">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. copias")</span><span class="sxs-lookup"><span data-stu-id="1d14c-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-714">Número máximo de copias que la impresora puede generar desde un único trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d14c-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-715">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="1d14c-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-716">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-717">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-718">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="1d14c-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-719">Número máximo de páginas de secuencia de impresión que la impresora puede representar en una sola hoja de medios.</span><span class="sxs-lookup"><span data-stu-id="1d14c-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-720">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-721">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-722">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-723">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. jobs"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="1d14c-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-724">Trabajo más grande (como un flujo de bytes) que la impresora aceptará en unidades de kilobytes.</span><span class="sxs-lookup"><span data-stu-id="1d14c-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="1d14c-725">Un valor de 0 (cero) indica que no se ha establecido ningún límite.</span><span class="sxs-lookup"><span data-stu-id="1d14c-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-726">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-727">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-728">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-729">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impresora CIM**. LanguagesSupported "," CIM \_ PrintJob. MimeTypes "," CIM \_ PrintService. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-730">Cadenas de forma libre que proporcionan explicaciones detalladas de los tipos MIME que admite la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="1d14c-731">Si se proporcionan datos para esta propiedad, el valor 47 ("MIME") debe incluirse en la propiedad **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-732">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1d14c-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-733">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-734">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-735">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1d14c-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-736">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d14c-736">Label by which the object is known.</span></span> <span data-ttu-id="1d14c-737">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="1d14c-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1d14c-738">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-739">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-740">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-741">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-742">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-743">Idiomas disponibles para las cadenas usadas por la impresora para la salida de información de administración.</span><span class="sxs-lookup"><span data-stu-id="1d14c-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="1d14c-744">Las cadenas deben ajustarse a RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="1d14c-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="1d14c-745">Por ejemplo, "en" se utiliza para inglés.</span><span class="sxs-lookup"><span data-stu-id="1d14c-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-746">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-747">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-748">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-749">Tipos de papel compatibles.</span><span class="sxs-lookup"><span data-stu-id="1d14c-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-750">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-751">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="1d14c-752">**A** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="1d14c-753">**B** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="1d14c-754">**C** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="1d14c-755">**D** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="1d14c-756">**E** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="1d14c-757">**Letra** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="1d14c-758">**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="1d14c-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="1d14c-759">**Na-10x13-Envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="1d14c-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="1d14c-760">**Na-9x12-Envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="1d14c-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="1d14c-761">**Na-número-10-sobre** (11)</span><span class="sxs-lookup"><span data-stu-id="1d14c-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="1d14c-762">**Na-7x9-Envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="1d14c-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="1d14c-763">**Na-9x11-Envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="1d14c-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="1d14c-764">**Na-10x14-Envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="1d14c-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="1d14c-765">**Na-número-9-sobre** (15)</span><span class="sxs-lookup"><span data-stu-id="1d14c-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="1d14c-766">**Na-6x9-Envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="1d14c-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="1d14c-767">**Na-10x15-Envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="1d14c-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="1d14c-768">**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="1d14c-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="1d14c-769">**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="1d14c-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="1d14c-770">**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="1d14c-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="1d14c-771">**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="1d14c-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="1d14c-772">**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="1d14c-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="1d14c-773">**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="1d14c-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="1d14c-774">**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="1d14c-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="1d14c-775">**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="1d14c-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="1d14c-776">**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="1d14c-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="1d14c-777">**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="1d14c-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="1d14c-778">**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="1d14c-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="1d14c-779">**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="1d14c-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="1d14c-780">**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="1d14c-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="1d14c-781">**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="1d14c-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="1d14c-782">**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="1d14c-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="1d14c-783">**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="1d14c-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="1d14c-784">**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="1d14c-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="1d14c-785">**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="1d14c-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="1d14c-786">**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="1d14c-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="1d14c-787">**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="1d14c-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="1d14c-788">**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="1d14c-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="1d14c-789">**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="1d14c-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="1d14c-790">**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="1d14c-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="1d14c-791">**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="1d14c-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="1d14c-792">**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="1d14c-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="1d14c-793">**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="1d14c-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="1d14c-794">**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="1d14c-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="1d14c-795">**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="1d14c-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="1d14c-796">**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="1d14c-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="1d14c-797">**Designación ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="1d14c-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="1d14c-798">**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="1d14c-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="1d14c-799">**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="1d14c-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="1d14c-800">**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="1d14c-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="1d14c-801">**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="1d14c-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="1d14c-802">**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="1d14c-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="1d14c-803">**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="1d14c-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="1d14c-804">**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="1d14c-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="1d14c-805">**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="1d14c-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="1d14c-806">**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="1d14c-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="1d14c-807">**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="1d14c-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="1d14c-808">**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="1d14c-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="1d14c-809">**Letra na** (59)</span><span class="sxs-lookup"><span data-stu-id="1d14c-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="1d14c-810">**Na-legal** (60)</span><span class="sxs-lookup"><span data-stu-id="1d14c-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="1d14c-811">**Sobre B4** (61)</span><span class="sxs-lookup"><span data-stu-id="1d14c-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="1d14c-812">**Sobre B5** (62)</span><span class="sxs-lookup"><span data-stu-id="1d14c-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="1d14c-813">**Sobre C3** (63)</span><span class="sxs-lookup"><span data-stu-id="1d14c-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="1d14c-814">**Sobre C4** (64)</span><span class="sxs-lookup"><span data-stu-id="1d14c-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="1d14c-815">**Sobre C5** (65)</span><span class="sxs-lookup"><span data-stu-id="1d14c-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="1d14c-816">**Sobre C6** (66)</span><span class="sxs-lookup"><span data-stu-id="1d14c-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="1d14c-817">**Designated-Long-Envelope** (67)</span><span class="sxs-lookup"><span data-stu-id="1d14c-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="1d14c-818">**Sobre monarca** (68)</span><span class="sxs-lookup"><span data-stu-id="1d14c-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="1d14c-819">**Ejecutivo** (69)</span><span class="sxs-lookup"><span data-stu-id="1d14c-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="1d14c-820">**Folio** (70)</span><span class="sxs-lookup"><span data-stu-id="1d14c-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="1d14c-821">**Factura** (71)</span><span class="sxs-lookup"><span data-stu-id="1d14c-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="1d14c-822">**Libro de contabilidad** (72)</span><span class="sxs-lookup"><span data-stu-id="1d14c-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="1d14c-823">**Cuarto** (73)</span><span class="sxs-lookup"><span data-stu-id="1d14c-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-824">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="1d14c-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-825">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1d14c-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-826">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-827">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ PrintService. PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-828">Cadenas de forma libre que especifican los tipos de papel que están disponibles actualmente para la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="1d14c-829">Cada cadena debe expresarse en el formato especificado por la aplicación de impresión de documentos (DPA) ISO/IEC 10175, que también se resume en el Apéndice C de RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="1d14c-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="1d14c-830">Ejemplos de cadenas válidas son "ISO-A4-color" y "na-10x14-Envelope".</span><span class="sxs-lookup"><span data-stu-id="1d14c-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="1d14c-831">Por definición, un tamaño de papel que está disponible y que aparece en la propiedad **PaperTypesAvailable** también debe aparecer en la propiedad **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d14c-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-833">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-834">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-835">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d14c-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-836">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d14c-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="1d14c-837">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1d14c-838">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1d14c-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-839">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d14c-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-840">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-841">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-842">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d14c-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1d14c-843">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="1d14c-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d14c-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1d14c-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d14c-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d14c-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-848">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1d14c-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1d14c-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-850">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="1d14c-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1d14c-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-852">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1d14c-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1d14c-853">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="1d14c-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1d14c-854">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1d14c-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1d14c-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-856">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="1d14c-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1d14c-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1d14c-858">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="1d14c-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-859">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1d14c-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-860">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1d14c-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-861">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-862">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="1d14c-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1d14c-863">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1d14c-864">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="1d14c-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1d14c-865">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1d14c-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="1d14c-866">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-867">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="1d14c-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-868">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-869">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-870">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-871">Información de estado, más allá de la especificada en la propiedad **Availability** , para una impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-872">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-873">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="1d14c-874">**Inactivo** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="1d14c-875">**Impresión** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="1d14c-876">**Preparación** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="1d14c-877">**Impresión detenida** (6)</span><span class="sxs-lookup"><span data-stu-id="1d14c-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="1d14c-878">**Sin conexión** (7)</span><span class="sxs-lookup"><span data-stu-id="1d14c-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-879">**Estado**</span><span class="sxs-lookup"><span data-stu-id="1d14c-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-880">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-881">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-882">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1d14c-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-883">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="1d14c-883">Current status of the object.</span></span> <span data-ttu-id="1d14c-884">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d14c-885">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d14c-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1d14c-886">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="1d14c-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1d14c-887">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="1d14c-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d14c-888">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1d14c-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-889">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="1d14c-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1d14c-890">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="1d14c-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1d14c-891">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="1d14c-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1d14c-892">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="1d14c-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1d14c-893">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="1d14c-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1d14c-894">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="1d14c-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1d14c-895">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1d14c-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1d14c-896">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="1d14c-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1d14c-897">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="1d14c-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1d14c-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-899">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d14c-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-900">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-901">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1d14c-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-902">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d14c-902">State of the logical device.</span></span> <span data-ttu-id="1d14c-903">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="1d14c-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1d14c-904">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d14c-905">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d14c-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d14c-906">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d14c-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d14c-907">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d14c-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d14c-908">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="1d14c-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d14c-909">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="1d14c-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d14c-910">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d14c-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-911">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-912">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-913">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d14c-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-914">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d14c-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="1d14c-915">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-916">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d14c-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-917">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1d14c-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-918">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-919">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1d14c-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-920">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1d14c-920">Scoping system's name.</span></span>

<span data-ttu-id="1d14c-921">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-922">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="1d14c-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-923">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d14c-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-924">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-925">Hora de la última vez que se restableció la impresora.</span><span class="sxs-lookup"><span data-stu-id="1d14c-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="1d14c-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="1d14c-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d14c-927">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d14c-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-928">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d14c-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d14c-929">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles por pulgada")</span><span class="sxs-lookup"><span data-stu-id="1d14c-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="1d14c-930">Resolución vertical en píxeles por pulgada.</span><span class="sxs-lookup"><span data-stu-id="1d14c-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d14c-931">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d14c-931">Remarks</span></span>

<span data-ttu-id="1d14c-932">La clase de **\_ impresora CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1d14c-933">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="1d14c-933">WMI does not implement this class.</span></span> <span data-ttu-id="1d14c-934">En el caso de la clase WMI derivada de la **\_ impresora CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1d14c-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1d14c-935">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1d14c-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d14c-936">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1d14c-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d14c-937">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d14c-937">Requirements</span></span>



| <span data-ttu-id="1d14c-938">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d14c-938">Requirement</span></span> | <span data-ttu-id="1d14c-939">Value</span><span class="sxs-lookup"><span data-stu-id="1d14c-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d14c-940">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d14c-940">Minimum supported client</span></span><br/> | <span data-ttu-id="1d14c-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d14c-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d14c-942">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d14c-942">Minimum supported server</span></span><br/> | <span data-ttu-id="1d14c-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d14c-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d14c-944">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d14c-944">Namespace</span></span><br/>                | <span data-ttu-id="1d14c-945">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1d14c-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d14c-946">MOF</span><span class="sxs-lookup"><span data-stu-id="1d14c-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d14c-947"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d14c-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d14c-948">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d14c-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d14c-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d14c-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d14c-950">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d14c-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d14c-951">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="1d14c-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

