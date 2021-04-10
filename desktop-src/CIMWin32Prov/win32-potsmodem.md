---
description: La \_ clase WMI POTSModem de Win32 representa los servicios y las características de un módem de servicio de teléfono anterior (POTS) sin formato en un equipo que ejecuta Windows.
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Clase Win32_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907257"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="aa3c4-103">\_Clase Win32 POTSModem</span><span class="sxs-lookup"><span data-stu-id="aa3c4-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="aa3c4-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ POTSModem de Win32** representa los servicios y las características de un módem de servicio de teléfono anterior (POTS) sin formato en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="aa3c4-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aa3c4-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3c4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa3c4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="aa3c4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa3c4-108">Members</span></span>

<span data-ttu-id="aa3c4-109">La **clase \_ POTSModem de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aa3c4-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="aa3c4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa3c4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aa3c4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa3c4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aa3c4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa3c4-112">Methods</span></span>

<span data-ttu-id="aa3c4-113">La clase **Win32 \_ POTSModem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="aa3c4-114">Método</span><span class="sxs-lookup"><span data-stu-id="aa3c4-114">Method</span></span>            | <span data-ttu-id="aa3c4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa3c4-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3c4-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-116">**Reset**</span></span>         | <span data-ttu-id="aa3c4-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-117">Not implemented.</span></span> <span data-ttu-id="aa3c4-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="aa3c4-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-119">**SetPowerState**</span></span> | <span data-ttu-id="aa3c4-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-120">Not implemented.</span></span> <span data-ttu-id="aa3c4-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ PotsModem**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aa3c4-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa3c4-122">Properties</span></span>

<span data-ttu-id="aa3c4-123">La **clase \_ POTSModem de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa3c4-124">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-127">Configuración actual de la respuesta automática o la devolución de llamada para el módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="aa3c4-128">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-129">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-130">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa3c4-131">**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="aa3c4-132">**Respuesta manual** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="aa3c4-133">**Respuesta automática** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="aa3c4-134">**Respuesta automática con devolución de llamada** (5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-138">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| AttachedTo")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-139">Puerto al que está conectado el módem de POTS.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="aa3c4-140">Ejemplo: "COM1"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-141">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-144">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-145">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-145">Availability and status of the device.</span></span>

<span data-ttu-id="aa3c4-146">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="aa3c4-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-150">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="aa3c4-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="aa3c4-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="aa3c4-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aa3c4-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="aa3c4-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="aa3c4-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="aa3c4-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="aa3c4-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="aa3c4-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa3c4-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="aa3c4-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="aa3c4-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="aa3c4-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-161">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="aa3c4-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-163">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="aa3c4-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-165">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="aa3c4-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="aa3c4-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-168">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aa3c4-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-170">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="aa3c4-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-172">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="aa3c4-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-174">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="aa3c4-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-176">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-177">**BlindOff**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-180">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| BlindOff")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-181">Cadena de comandos que se usa para detectar un tono de marcado antes de marcar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="aa3c4-182">Ejemplo: "x4"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-183">**Persianaon**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-186">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| blindon")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-187">Cadena de comandos que se usa para marcar si hay o no un tono de marcado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="aa3c4-188">Ejemplo: "x3"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-192">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-193">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-193">Short description of the object.</span></span>

<span data-ttu-id="aa3c4-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-198">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| CompatibilityFlags")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-199">Todos los protocolos de conexión de módem con los que este dispositivo de módem es compatible.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-200">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-201">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-203">Características de compresión de datos del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="aa3c4-204">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-207">Unknown</span><span class="sxs-lookup"><span data-stu-id="aa3c4-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="aa3c4-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Sin compresión** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-209">Otros</span><span class="sxs-lookup"><span data-stu-id="aa3c4-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="aa3c4-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-211">Sin compresión</span><span class="sxs-lookup"><span data-stu-id="aa3c4-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="aa3c4-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-213">MNP 5</span><span class="sxs-lookup"><span data-stu-id="aa3c4-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="aa3c4-214"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-215">V. 42bis</span><span class="sxs-lookup"><span data-stu-id="aa3c4-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-216">**CompressionOff**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-219">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| del sistema \\ \\ CurrentControlSet \\ \\ control \\ \\ \| Compression \_ OFF")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-220">Cadena de comandos que se usa para deshabilitar la compresión de datos de hardware.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="aa3c4-221">Ejemplo: "S46 = 136"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-222">**CompressionOn**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-225">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| del sistema \\ \\ CurrentControlSet \\ \\ control \\ \\ \| Compression \_ on")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-226">Cadena de comandos que se usa para habilitar la compresión de datos de hardware.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="aa3c4-227">Ejemplo: "S46 = 138"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-228">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-229">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-231">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-232">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="aa3c4-233">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="aa3c4-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="aa3c4-235"> (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-236">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="aa3c4-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="aa3c4-238">(1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-239">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa3c4-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="aa3c4-241">(2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="aa3c4-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="aa3c4-243">(3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-244">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aa3c4-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="aa3c4-246">(4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-247">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-247">Device is not working properly.</span></span> <span data-ttu-id="aa3c4-248">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="aa3c4-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="aa3c4-250">(5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-251">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="aa3c4-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="aa3c4-253"> (6)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-254">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="aa3c4-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="aa3c4-256">(7)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="aa3c4-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="aa3c4-258">(8)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-259">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="aa3c4-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="aa3c4-261">(9)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-262">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-262">Device is not working properly.</span></span> <span data-ttu-id="aa3c4-263">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="aa3c4-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="aa3c4-265">(10)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-266">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="aa3c4-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="aa3c4-268">(11)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-269">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="aa3c4-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="aa3c4-271">(12)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-272">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="aa3c4-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="aa3c4-274">(13)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-275">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="aa3c4-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="aa3c4-277">(14)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-278">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="aa3c4-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="aa3c4-280">(15)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-281">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="aa3c4-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="aa3c4-283">(16)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-284">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="aa3c4-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="aa3c4-286">(17)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-287">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa3c4-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="aa3c4-289">(18)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-290">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="aa3c4-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="aa3c4-292">(19)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aa3c4-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="aa3c4-294">(20)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-295">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="aa3c4-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="aa3c4-297">(21)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-298">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-298">System failure.</span></span> <span data-ttu-id="aa3c4-299">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="aa3c4-300">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="aa3c4-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="aa3c4-302">(22)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-303">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="aa3c4-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="aa3c4-305">(23)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-306">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-306">System failure.</span></span> <span data-ttu-id="aa3c4-307">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="aa3c4-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="aa3c4-309">(24)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-310">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aa3c4-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aa3c4-312">(25)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-313">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aa3c4-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aa3c4-315">(26)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-316">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="aa3c4-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="aa3c4-318">(27)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-319">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="aa3c4-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="aa3c4-321">(28)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-322">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="aa3c4-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="aa3c4-324">(29)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-325">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-325">Device is disabled.</span></span> <span data-ttu-id="aa3c4-326">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="aa3c4-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="aa3c4-328">(30)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-329">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa3c4-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="aa3c4-331">31</span><span class="sxs-lookup"><span data-stu-id="aa3c4-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-332">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-332">Device is not working properly.</span></span> <span data-ttu-id="aa3c4-333">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-334">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-335">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-337">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-338">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="aa3c4-339">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-340">**ConfigurationDialog**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-341">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-343">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| ConfigDialog")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-344">Cadena de inicialización del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-344">Modem initialization string.</span></span> <span data-ttu-id="aa3c4-345">Esta propiedad se compone de cadenas de comandos de otras propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-346">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-347">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-349">Matriz de países o regiones en los que el módem puede operar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="aa3c4-350">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-351">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-354">País o región para el que el módem está programado actualmente.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="aa3c4-355">Cuando se admiten varios países o regiones, esta propiedad define cuál de ellas se selecciona actualmente para su uso.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="aa3c4-356">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-357">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-360">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-361">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="aa3c4-362">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aa3c4-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-364">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-365">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-367">Lista de contraseñas definidas actualmente para el módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="aa3c4-368">Esta matriz puede dejarse en blanco por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="aa3c4-369">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-371">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="aa3c4-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-373">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-374">Configuración del control para un dispositivo de comunicaciones serie, en este caso, el dispositivo de módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-375">**Valor predeterminado**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-376">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="aa3c4-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-378">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| default")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-379">Si es **true**, este módem de Pots es el módem predeterminado en el equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-380">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-383">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-384">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-384">Description of the object.</span></span>

<span data-ttu-id="aa3c4-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-386">**ID**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-389">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-390">Identificador único de este módem de POTS desde otros dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="aa3c4-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-392">**DeviceLoader**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-393">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-395">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| cargador de sistema")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-396">Nombre del cargador del dispositivo para el módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="aa3c4-397">Un cargador de dispositivos carga y administra los controladores y los enumeradores de dispositivos para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-399">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-401">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| DeviceType")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-402">Tipo físico del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-402">Physical type of the modem.</span></span>

<span data-ttu-id="aa3c4-403">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="aa3c4-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="aa3c4-404">"Módem nulo"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="aa3c4-405">"Módem interno"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="aa3c4-406">"Módem externo"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="aa3c4-407">"Módem PCMCIA"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="aa3c4-408">Unknown</span><span class="sxs-lookup"><span data-stu-id="aa3c4-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="aa3c4-409">**Módem nulo** ("módem nulo")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="aa3c4-410">**Módem interno** ("módem interno")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="aa3c4-411">**Módem externo** ("módem externo")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="aa3c4-412">**Módem PCMCIA** ("módem PCMCIA")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-413">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-414">**DialType**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-415">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-417">Tipo de método de marcado utilizado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-417">Type of dialing method used.</span></span>

<span data-ttu-id="aa3c4-418">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-419">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="aa3c4-420">**Tono** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="aa3c4-421">**Pulso** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-422">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-423">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-425">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-426">Fecha del controlador del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-428">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-430">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="aa3c4-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-432">**ErrorControlForced**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-435">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| ErrorControl \_ Forced")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-436">Cadena de comandos que se usa para habilitar el control de corrección de errores al establecer una conexión.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="aa3c4-437">Esto aumenta la confiabilidad de la conexión.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="aa3c4-438">Ejemplo: "+ Q5S36 = 4S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-439">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-440">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-442">Características de corrección de errores del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="aa3c4-443">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-444">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-445">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="aa3c4-446">**Sin corrección de errores** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="aa3c4-447">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="aa3c4-448">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-449">**ErrorControlOff**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-450">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-452">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| ErrorControl \_ OFF")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-453">Cadena de comandos que se usa para deshabilitar el control de errores.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-453">Command string used to disable error control.</span></span>

<span data-ttu-id="aa3c4-454">Ejemplo: "+ Q6S36 = 3S48 = 128"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-455">**ErrorControlOn**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-456">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-458">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| ErrorControl \_ on")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-459">Cadena de comandos que se usa para habilitar el control de errores.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-459">Command string used to enable error control.</span></span>

<span data-ttu-id="aa3c4-460">Ejemplo: "+ Q5S36 = 7S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-462">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-464">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="aa3c4-465">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-466">**FlowControlHard**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-467">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-469">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| FlowControl \_ Hard")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-470">Cadena de comandos que se usa para habilitar el control de flujo de hardware.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="aa3c4-471">El control de flujo se compone de señales enviadas entre equipos que comprueban que ambos equipos están listos para transmitir o recibir datos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="aa3c4-472">Ejemplo: "&K1"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-473">**FlowControlOff**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-476">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| FlowControl \_ OFF")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-477">Cadena de comandos que se usa para deshabilitar el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-477">Command string used to disable flow control.</span></span> <span data-ttu-id="aa3c4-478">El control de flujo se compone de señales enviadas entre equipos que comprueban que ambos equipos están listos para transmitir o recibir datos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="aa3c4-479">Ejemplo: "&K0"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-480">**FlowControlSoft**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-483">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| FlowControl \_ soft")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-484">Cadena de comandos que se usa para habilitar el control de flujo de software.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="aa3c4-485">El control de flujo se compone de señales enviadas entre equipos que comprueban que ambos equipos están listos para transmitir o recibir datos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="aa3c4-486">Ejemplo: "&K2"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-487">**InactivityScale**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-488">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-490">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| InactivityScale")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-491">Multiplicador que se usa con la propiedad **InactivityTimeout** para calcular el período de tiempo de espera de una conexión.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-493">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-494">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-495">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-496">Límite de tiempo (en segundos) para la desconexión automática de la línea telefónica, si no se intercambia ningún dato.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="aa3c4-497">Un valor de 0 (cero) indica que esta característica está presente pero no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="aa3c4-498">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-500">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-501">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-502">Número de índice de este módem de POTS.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="aa3c4-503">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="aa3c4-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-504">**IndexEx**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-505">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-506">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-507">El identificador de instancia de dispositivo para este módem de POTS.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="aa3c4-508">Ejemplo: "1&08"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-508">Example: "1&08"</span></span>

<span data-ttu-id="aa3c4-509">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad está disponible a partir de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-511">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-513">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-514">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-514">Date and time the object was installed.</span></span> <span data-ttu-id="aa3c4-515">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aa3c4-516">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-517">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-518">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-520">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="aa3c4-521">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-522">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-523">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-525">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-526">Velocidad máxima de comunicación configurable para tener acceso al sistema telefónico.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="aa3c4-527">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-528">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-529">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-531">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-532">Velocidad máxima de comunicación configurable en el puerto COM para un módem externo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="aa3c4-533">Escriba 0 (cero) si no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="aa3c4-534">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-535">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-536">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-538">Número de contraseñas que se han definido en el propio módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="aa3c4-539">Si no se admite esta característica, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="aa3c4-540">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-541">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-542">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-543">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-544">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| Model")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-545">Modelo de este módem de POTS.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-545">Model of this POTS modem.</span></span>

<span data-ttu-id="aa3c4-546">Ejemplo: "Sportster 56K external"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-547">**ModemInfPath**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-548">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-549">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-550">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-551">Ruta de acceso al archivo. inf de este módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="aa3c4-552">Este archivo contiene información de inicialización para el módem y su controlador.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="aa3c4-553">Ejemplo: "C: \\ Windows \\ inf"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-554">**ModemInfSection**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-555">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-556">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-557">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-558">Nombre de la sección del archivo. inf del módem que contiene información sobre el módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-559">**ModulationBell**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-560">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-561">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-562">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| Modulation \_ Bell")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-563">Cadena de comandos que se usa para indicar al módem que use las modulaciones de campana para 300 y 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="aa3c4-564">Ejemplo: "B1"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-565">**ModulationCCITT**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-566">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-567">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-568">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| Modulation \_ CCITT")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-569">Cadena de comandos que se usa para indicar al módem que use las modulaciones CCITt para 300 y 1200 bps.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="aa3c4-570">Ejemplo: "B0"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-571">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-572">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-573">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-574">Esquema de modulación del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="aa3c4-575">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-576">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-577">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aa3c4-578">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="aa3c4-579">**Campana 103** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="aa3c4-580">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="aa3c4-581">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="aa3c4-582">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="aa3c4-583">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="aa3c4-584">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="aa3c4-585">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="aa3c4-586">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="aa3c4-587">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-588">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-590">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-591">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-592">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-592">Label by which the object is known.</span></span> <span data-ttu-id="aa3c4-593">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="aa3c4-594">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-596">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-597">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-598">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-599">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="aa3c4-600">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="aa3c4-601">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-602">**PortSubClass**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-603">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-604">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-605">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| PortSubClass"), **valor** ("puerto paralelo", "puerto serie", "módem")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-606">Definición del puerto usado para este módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="aa3c4-607">("00")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-608">Puerto paralelo</span><span class="sxs-lookup"><span data-stu-id="aa3c4-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="aa3c4-609">("01")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-610">Puerto serie</span><span class="sxs-lookup"><span data-stu-id="aa3c4-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="aa3c4-611">("02")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-612">Módem</span><span class="sxs-lookup"><span data-stu-id="aa3c4-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-613">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-614">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-615">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-616">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="aa3c4-617">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aa3c4-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa3c4-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa3c4-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-622">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="aa3c4-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-624">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="aa3c4-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-626">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="aa3c4-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="aa3c4-627">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="aa3c4-628">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="aa3c4-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-630">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="aa3c4-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aa3c4-632">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="aa3c4-632">Timed Power-On Supported</span></span>

<span data-ttu-id="aa3c4-633">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-634">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-635">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-636">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-637">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="aa3c4-638">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="aa3c4-639">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-640">**Prefijo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-641">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-642">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-643">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ \\ \\ \\ \\ Prefijo de clase de control System CurrentControlSet" \| )</span><span class="sxs-lookup"><span data-stu-id="aa3c4-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-644">Prefijo de marcado que se usa para tener acceso a una línea externa.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-645">**Propiedades**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-646">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="aa3c4-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-647">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-648">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| Properties")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-649">Lista de todas las propiedades (y sus valores) de este módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-651">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-652">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-653">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| providerName")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-654">Ruta de acceso de red al equipo que proporciona los servicios de módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-655">**Quatro**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-656">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-657">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-658">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| Pulse")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-659">Cadena de comandos que se usa para indicar al módem que use el modo por pulsos para el marcado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="aa3c4-660">El marcado por pulsos es necesario para las líneas telefónicas que no pueden controlar el marcado por tonos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="aa3c4-661">Ejemplo: "P"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-662">**Reset**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-663">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-664">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-665">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) (RESET), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| RESET")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-666">Cadena de comandos que se usa para restablecer el módem para la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="aa3c4-667">Ejemplo: "AT&F"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-668">**ResponsesKeyName**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-669">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-670">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-671">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| ResponsesKeyName")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-672">Respuesta: este módem podría informar al sistema operativo durante el proceso de conexión.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="aa3c4-673">Los dos primeros caracteres especifican el tipo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="aa3c4-674">Los dos segundos especifican información acerca de la conexión que se está realizando.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="aa3c4-675">Los dos caracteres siguientes se usan solo para la negociación de progreso o los códigos de respuesta de conexión.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="aa3c4-676">Los ocho caracteres siguientes especifican la velocidad de línea entre módem y módem negociada en bits por segundo (BPS).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="aa3c4-677">Los caracteres representan un formato de entero largo sin signo de 32 bits (byte y palabra inverso).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="aa3c4-678">Los últimos ocho caracteres indican que el módem está cambiando a un puerto diferente o a la velocidad del equipo terminal de datos (DTE).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="aa3c4-679">Normalmente, este campo no se usa porque los módems realizan conexiones en una velocidad de Puerto bloqueada, independientemente de la velocidad entre módems o equipos de comunicaciones de datos (DCE).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-680">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-681">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-682">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-683">Número de anillos antes de que el módem responda a una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="aa3c4-684">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-685">**SpeakerModeDial**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-686">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-687">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-688">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerModeDial")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-689">Cadena de comandos que se usa para activar el altavoz del módem después de marcar un número y desactivar el altavoz cuando se ha establecido una conexión.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="aa3c4-690">Ejemplo: "M1"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-691">**SpeakerModeOff**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-692">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-693">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-694">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerModeOff")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-695">Cadena de comandos que se usa para desactivar el altavoz del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="aa3c4-696">Ejemplo: "M0"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-697">**SpeakerModeOn**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-698">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-699">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-700">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerModeOn")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-701">Cadena de comandos que se usa para activar el altavoz del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="aa3c4-702">Ejemplo: "m2"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-703">**SpeakerModeSetup**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-704">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-705">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-706">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerModeSetup")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-707">Cadena de comandos que se usa para indicar al módem que active el altavoz (hasta que se establezca una conexión).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="aa3c4-708">Ejemplo: "m3"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-709">**SpeakerVolumeHigh**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-710">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-711">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-712">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerVolume \_ High")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-713">Cadena de comandos que se usa para establecer el altavoz del módem en el volumen más alto.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="aa3c4-714">Ejemplo: "L3"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-715">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-716">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-717">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-718">Describe el nivel de volumen de los tonos sonoros del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="aa3c4-719">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-720">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-721">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aa3c4-722">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="aa3c4-723">**Alto** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="aa3c4-724">**Medio** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="aa3c4-725">**Bajo** (5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="aa3c4-726">**Desactivado** (6)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="aa3c4-727">**Auto** (7)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-728">**SpeakerVolumeLow**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-729">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-730">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-731">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerVolume \_ Low")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-732">Cadena de comandos que se usa para establecer el altavoz del módem en el volumen más bajo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="aa3c4-733">Ejemplo: "L1"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-734">**SpeakerVolumeMed**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-735">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-736">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-737">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| SpeakerVolume \_ Med")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-738">Cadena de comandos que se usa para establecer el altavoz del módem en un volumen medio.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="aa3c4-739">Ejemplo: "L2"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-740">**Estado**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-741">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-742">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-743">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-744">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-744">Current status of the object.</span></span> <span data-ttu-id="aa3c4-745">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aa3c4-746">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aa3c4-747">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="aa3c4-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aa3c4-748">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aa3c4-749">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aa3c4-750">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aa3c4-751">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="aa3c4-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aa3c4-752">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aa3c4-753">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa3c4-754">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-755">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aa3c4-756">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aa3c4-757">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aa3c4-758">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aa3c4-759">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aa3c4-760">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aa3c4-761">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aa3c4-762">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aa3c4-763">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-765">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-766">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-767">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-768">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-768">State of the logical device.</span></span> <span data-ttu-id="aa3c4-769">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="aa3c4-770">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa3c4-771">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa3c4-772">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa3c4-773">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa3c4-774">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aa3c4-775">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-777">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-778">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-779">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("LINEDEVCAPS de la API de Win32 \_ \| estructuras de dispositivo \| \| dwStringFormat")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-780">Tipo de caracteres que se usa para el texto que se pasa a través del módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="aa3c4-781">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="aa3c4-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="aa3c4-782">"Formato de cadena ASCII"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="aa3c4-783">"Formato de cadena DBCS"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="aa3c4-784">"Formato de cadena Unicode"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="aa3c4-785">**Formato de cadena ASCII** ("formato de cadena ASCII")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="aa3c4-786">**Formato de cadena DBCS** ("formato de cadena DBCS")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="aa3c4-787">**Formato de cadena Unicode** ("formato de cadena Unicode")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa3c4-788">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-789">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-790">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-791">Si **es true**, el módem admite la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="aa3c4-792">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-793">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-794">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-795">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-796">Si es **true**, se admite la comunicación sincrónica y asincrónica.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="aa3c4-797">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-798">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-799">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-800">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-801">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-802">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="aa3c4-803">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-804">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-805">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-806">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-807">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aa3c4-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-808">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-808">Name of the scoping system.</span></span>

<span data-ttu-id="aa3c4-809">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-810">**Terminador**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-811">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-812">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-813">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| Terminator")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-814">Cadena que marca el final de una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="aa3c4-815">Ejemplo: "<CR"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-816">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-817">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-818">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-819">Fecha y hora de la última vez que se restableció el módem.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="aa3c4-820">Esta propiedad se hereda de [**\_ PotsModem CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-821">**Tonos**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-822">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-823">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-824">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| tone")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-825">Cadena de comandos que indica al módem que use el modo de tono para el marcado.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="aa3c4-826">La línea telefónica debe admitir el marcado por tonos.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="aa3c4-827">Ejemplo: "T"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="aa3c4-828">**VoiceSwitchFeature**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa3c4-829">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-830">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa3c4-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa3c4-831">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| VoiceSwitchFeature")</span><span class="sxs-lookup"><span data-stu-id="aa3c4-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="aa3c4-832">Cadenas de comandos que se usan para activar las funciones de voz de un módem de voz.</span><span class="sxs-lookup"><span data-stu-id="aa3c4-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="aa3c4-833">Ejemplo: "AT + V"</span><span class="sxs-lookup"><span data-stu-id="aa3c4-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa3c4-834">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa3c4-834">Remarks</span></span>

<span data-ttu-id="aa3c4-835">La **clase \_ POTSModem de Win32** se deriva de [**\_ POTSModem de CIM**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="aa3c4-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa3c4-836">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa3c4-836">Requirements</span></span>



| <span data-ttu-id="aa3c4-837">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa3c4-837">Requirement</span></span> | <span data-ttu-id="aa3c4-838">Value</span><span class="sxs-lookup"><span data-stu-id="aa3c4-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3c4-839">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa3c4-839">Minimum supported client</span></span><br/> | <span data-ttu-id="aa3c4-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa3c4-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa3c4-841">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa3c4-841">Minimum supported server</span></span><br/> | <span data-ttu-id="aa3c4-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa3c4-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa3c4-843">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa3c4-843">Namespace</span></span><br/>                | <span data-ttu-id="aa3c4-844">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aa3c4-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa3c4-845">MOF</span><span class="sxs-lookup"><span data-stu-id="aa3c4-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa3c4-846"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa3c4-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa3c4-847">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa3c4-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa3c4-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa3c4-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa3c4-849">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa3c4-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3c4-850">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="aa3c4-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="aa3c4-851">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="aa3c4-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
