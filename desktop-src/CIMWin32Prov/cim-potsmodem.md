---
description: La \_ clase CIM POTSModem representa un dispositivo que traduce los datos binarios en modulaciones de onda para la transmisión basada en sonido mediante la conexión a la red de sistema telefónico anterior (POTS).
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: CIM_POTSModem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000649"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="84154-103">\_Clase POTSModem de CIM</span><span class="sxs-lookup"><span data-stu-id="84154-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="84154-104">La clase **CIM \_ POTSModem** representa un dispositivo que traduce los datos binarios en modulaciones de onda para la transmisión basada en sonido mediante la conexión a la red de sistema telefónico anterior (POTS).</span><span class="sxs-lookup"><span data-stu-id="84154-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84154-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="84154-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="84154-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="84154-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="84154-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="84154-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="84154-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="84154-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84154-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84154-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="84154-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="84154-110">Members</span></span>

<span data-ttu-id="84154-111">La clase **CIM \_ POTSModem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="84154-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="84154-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="84154-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="84154-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84154-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84154-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="84154-114">Methods</span></span>

<span data-ttu-id="84154-115">La clase **CIM \_ POTSModem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="84154-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="84154-116">Método</span><span class="sxs-lookup"><span data-stu-id="84154-116">Method</span></span>                                                               | <span data-ttu-id="84154-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="84154-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84154-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="84154-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="84154-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84154-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="84154-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="84154-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="84154-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="84154-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="84154-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="84154-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="84154-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="84154-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="84154-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84154-124">Properties</span></span>

<span data-ttu-id="84154-125">La clase **CIM \_ POTSModem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="84154-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84154-126">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="84154-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-129">Configuración actual de la respuesta automática o la devolución de llamada para el módem.</span><span class="sxs-lookup"><span data-stu-id="84154-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-130">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-131">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="84154-132">**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="84154-133">**Respuesta manual** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="84154-134">**Respuesta automática** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="84154-135">**Respuesta automática con devolución de llamada** (5)</span><span class="sxs-lookup"><span data-stu-id="84154-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-136">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="84154-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="84154-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="84154-140">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-140">Availability and status of the device.</span></span>

<span data-ttu-id="84154-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="84154-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="84154-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="84154-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="84154-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="84154-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="84154-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="84154-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="84154-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="84154-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="84154-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="84154-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="84154-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84154-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="84154-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="84154-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="84154-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="84154-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="84154-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="84154-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="84154-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="84154-155">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="84154-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="84154-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="84154-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="84154-157">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="84154-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="84154-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="84154-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="84154-159">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="84154-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="84154-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="84154-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="84154-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="84154-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="84154-162">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="84154-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="84154-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="84154-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="84154-164">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="84154-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="84154-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="84154-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="84154-166">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="84154-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="84154-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="84154-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="84154-168">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="84154-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="84154-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="84154-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="84154-170">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="84154-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-171">**Caption**</span><span class="sxs-lookup"><span data-stu-id="84154-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-174">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="84154-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="84154-175">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="84154-175">Short textual description of the object.</span></span>

<span data-ttu-id="84154-176">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84154-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-177">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="84154-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-180">Características de compresión de datos del módem.</span><span class="sxs-lookup"><span data-stu-id="84154-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-181">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-182">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="84154-183">**Sin compresión** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="84154-184">**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="84154-185">**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="84154-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84154-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84154-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-189">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="84154-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="84154-190">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="84154-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="84154-191">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="84154-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="84154-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="84154-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="84154-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="84154-194">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="84154-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="84154-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="84154-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="84154-196">(1)</span><span class="sxs-lookup"><span data-stu-id="84154-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="84154-197">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="84154-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="84154-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="84154-199">(2)</span><span class="sxs-lookup"><span data-stu-id="84154-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="84154-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="84154-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="84154-201">(3)</span><span class="sxs-lookup"><span data-stu-id="84154-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="84154-202">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="84154-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="84154-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="84154-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="84154-204">(4)</span><span class="sxs-lookup"><span data-stu-id="84154-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="84154-205">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="84154-205">Device is not working properly.</span></span> <span data-ttu-id="84154-206">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="84154-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="84154-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="84154-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="84154-208">(5)</span><span class="sxs-lookup"><span data-stu-id="84154-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="84154-209">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="84154-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="84154-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="84154-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="84154-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="84154-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="84154-212">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="84154-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="84154-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="84154-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="84154-214">(7)</span><span class="sxs-lookup"><span data-stu-id="84154-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="84154-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="84154-216">(8)</span><span class="sxs-lookup"><span data-stu-id="84154-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="84154-217">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="84154-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="84154-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="84154-219">(9)</span><span class="sxs-lookup"><span data-stu-id="84154-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="84154-220">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="84154-220">Device is not working properly.</span></span> <span data-ttu-id="84154-221">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="84154-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="84154-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="84154-223">(10)</span><span class="sxs-lookup"><span data-stu-id="84154-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="84154-224">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="84154-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="84154-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="84154-226">(11)</span><span class="sxs-lookup"><span data-stu-id="84154-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="84154-227">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="84154-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="84154-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="84154-229">(12)</span><span class="sxs-lookup"><span data-stu-id="84154-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="84154-230">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="84154-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="84154-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="84154-232">(13)</span><span class="sxs-lookup"><span data-stu-id="84154-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="84154-233">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="84154-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="84154-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="84154-235">(14)</span><span class="sxs-lookup"><span data-stu-id="84154-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="84154-236">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="84154-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="84154-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="84154-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="84154-238">(15)</span><span class="sxs-lookup"><span data-stu-id="84154-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="84154-239">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="84154-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="84154-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="84154-241">(16)</span><span class="sxs-lookup"><span data-stu-id="84154-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="84154-242">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="84154-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="84154-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="84154-244">(17)</span><span class="sxs-lookup"><span data-stu-id="84154-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="84154-245">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="84154-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="84154-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="84154-247">(18)</span><span class="sxs-lookup"><span data-stu-id="84154-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="84154-248">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="84154-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="84154-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="84154-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="84154-250">(19)</span><span class="sxs-lookup"><span data-stu-id="84154-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="84154-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="84154-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="84154-252">(20)</span><span class="sxs-lookup"><span data-stu-id="84154-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="84154-253">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="84154-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="84154-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="84154-255">(21)</span><span class="sxs-lookup"><span data-stu-id="84154-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="84154-256">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="84154-256">System failure.</span></span> <span data-ttu-id="84154-257">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="84154-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="84154-258">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="84154-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="84154-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="84154-260">(22)</span><span class="sxs-lookup"><span data-stu-id="84154-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="84154-261">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="84154-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="84154-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="84154-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="84154-263">(23)</span><span class="sxs-lookup"><span data-stu-id="84154-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="84154-264">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="84154-264">System failure.</span></span> <span data-ttu-id="84154-265">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="84154-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="84154-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="84154-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="84154-267">(24)</span><span class="sxs-lookup"><span data-stu-id="84154-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="84154-268">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="84154-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="84154-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="84154-270">(25)</span><span class="sxs-lookup"><span data-stu-id="84154-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="84154-271">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="84154-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="84154-273">(26)</span><span class="sxs-lookup"><span data-stu-id="84154-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="84154-274">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84154-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="84154-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="84154-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="84154-276">(27)</span><span class="sxs-lookup"><span data-stu-id="84154-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="84154-277">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="84154-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="84154-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="84154-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="84154-279">(28)</span><span class="sxs-lookup"><span data-stu-id="84154-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="84154-280">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="84154-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="84154-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="84154-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="84154-282">(29)</span><span class="sxs-lookup"><span data-stu-id="84154-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="84154-283">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="84154-283">Device is disabled.</span></span> <span data-ttu-id="84154-284">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="84154-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="84154-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="84154-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="84154-286">(30)</span><span class="sxs-lookup"><span data-stu-id="84154-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="84154-287">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="84154-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="84154-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="84154-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="84154-289">31</span><span class="sxs-lookup"><span data-stu-id="84154-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="84154-290">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="84154-290">Device is not working properly.</span></span> <span data-ttu-id="84154-291">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="84154-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-292">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="84154-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-293">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="84154-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84154-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-295">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="84154-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="84154-296">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="84154-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="84154-297">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-298">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="84154-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-299">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="84154-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84154-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-301">Países o regiones en los que el módem puede operar.</span><span class="sxs-lookup"><span data-stu-id="84154-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="84154-302">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="84154-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-305">País o región para el que el módem está programado actualmente.</span><span class="sxs-lookup"><span data-stu-id="84154-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="84154-306">Cuando se admiten varios países o regiones, esta propiedad define cuál de ellas se selecciona actualmente para su uso.</span><span class="sxs-lookup"><span data-stu-id="84154-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="84154-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84154-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-310">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="84154-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="84154-311">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="84154-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="84154-312">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="84154-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="84154-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-314">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="84154-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-315">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="84154-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84154-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-317">Contraseñas definidas actualmente para el módem.</span><span class="sxs-lookup"><span data-stu-id="84154-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="84154-318">Esta matriz puede dejarse en blanco por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="84154-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="84154-319">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84154-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-322">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="84154-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="84154-323">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="84154-323">Textual description of the object.</span></span>

<span data-ttu-id="84154-324">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84154-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-325">**ID**</span><span class="sxs-lookup"><span data-stu-id="84154-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-328">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="84154-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="84154-329">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84154-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="84154-330">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-331">**DialType**</span><span class="sxs-lookup"><span data-stu-id="84154-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-332">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-334">Tipo de marcado que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="84154-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-335">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="84154-336">**Tono** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="84154-337">**Pulso** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-338">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="84154-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-339">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="84154-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84154-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-341">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="84154-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="84154-342">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-343">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="84154-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-346">Características de corrección de errores del módem.</span><span class="sxs-lookup"><span data-stu-id="84154-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-347">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-348">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="84154-349">**Sin corrección de errores** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="84154-350">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="84154-351">**LAPM** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="84154-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-355">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="84154-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="84154-356">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="84154-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-358">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84154-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84154-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-360">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="84154-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="84154-361">Límite de tiempo (en segundos) para la desconexión automática de la línea telefónica si no se intercambia ningún dato.</span><span class="sxs-lookup"><span data-stu-id="84154-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="84154-362">Un valor de 0 (cero) indica que esta característica está presente pero no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="84154-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="84154-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84154-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-364">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84154-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84154-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-366">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="84154-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="84154-367">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="84154-367">Date and time the object was installed.</span></span> <span data-ttu-id="84154-368">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="84154-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="84154-369">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84154-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="84154-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-371">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84154-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84154-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-373">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84154-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="84154-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-375">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="84154-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-376">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84154-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84154-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-378">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="84154-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="84154-379">Velocidad máxima de comunicación configurable para tener acceso al sistema telefónico.</span><span class="sxs-lookup"><span data-stu-id="84154-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="84154-380">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="84154-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-381">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84154-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84154-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-383">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="84154-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="84154-384">Velocidad máxima de comunicación configurable en el puerto COM para un módem externo.</span><span class="sxs-lookup"><span data-stu-id="84154-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="84154-385">Escriba 0 (cero) si no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="84154-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="84154-386">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="84154-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-387">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-389">Número máximo de contraseñas que se han definido en el propio módem.</span><span class="sxs-lookup"><span data-stu-id="84154-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="84154-390">Si no se admite esta característica, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="84154-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="84154-391">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="84154-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-392">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-394">Esquema de modulación del módem.</span><span class="sxs-lookup"><span data-stu-id="84154-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-395">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-396">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="84154-397">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="84154-398">**Campana 103** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="84154-399">**Bell 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="84154-400">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="84154-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="84154-401">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="84154-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="84154-402">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="84154-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="84154-403">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="84154-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="84154-404">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="84154-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="84154-405">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="84154-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="84154-406">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="84154-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-407">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="84154-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-408">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-410">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="84154-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="84154-411">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="84154-411">Label by which the object is known.</span></span> <span data-ttu-id="84154-412">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="84154-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="84154-413">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84154-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="84154-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-417">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="84154-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="84154-418">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84154-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="84154-419">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="84154-420">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="84154-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="84154-421">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="84154-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-422">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84154-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-424">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84154-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="84154-425">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="84154-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="84154-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="84154-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="84154-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="84154-430">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="84154-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="84154-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="84154-432">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="84154-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="84154-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="84154-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="84154-434">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="84154-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="84154-435">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="84154-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="84154-436">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="84154-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="84154-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="84154-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="84154-438">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="84154-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="84154-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="84154-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="84154-440">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="84154-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-441">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="84154-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-442">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="84154-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84154-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-444">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="84154-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="84154-445">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="84154-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="84154-446">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="84154-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="84154-447">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="84154-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="84154-448">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-449">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="84154-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-450">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="84154-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="84154-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-452">Número de anillos antes de que el módem responda a una llamada entrante.</span><span class="sxs-lookup"><span data-stu-id="84154-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="84154-453">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="84154-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-454">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-456">Nivel de volumen de los tonos sonoros del módem.</span><span class="sxs-lookup"><span data-stu-id="84154-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="84154-457">Por ejemplo, se puede informar de un volumen alto, medio o bajo.</span><span class="sxs-lookup"><span data-stu-id="84154-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-458">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="84154-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-459">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="84154-460">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="84154-461">**Alto** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="84154-462">**Medio** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="84154-463">**Bajo** (5)</span><span class="sxs-lookup"><span data-stu-id="84154-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="84154-464">**Desactivado** (6)</span><span class="sxs-lookup"><span data-stu-id="84154-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="84154-465">**Auto** (7)</span><span class="sxs-lookup"><span data-stu-id="84154-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-466">**Estado**</span><span class="sxs-lookup"><span data-stu-id="84154-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-467">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-469">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="84154-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="84154-470">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="84154-470">Current status of the object.</span></span> <span data-ttu-id="84154-471">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84154-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="84154-472">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="84154-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="84154-473">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="84154-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="84154-474">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="84154-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84154-475">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="84154-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-476">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="84154-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="84154-477">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="84154-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="84154-478">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="84154-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="84154-479">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="84154-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84154-480">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="84154-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="84154-481">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="84154-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="84154-482">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="84154-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="84154-483">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="84154-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="84154-484">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="84154-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="84154-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-486">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84154-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84154-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-488">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="84154-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="84154-489">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="84154-489">State of the logical device.</span></span> <span data-ttu-id="84154-490">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="84154-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="84154-491">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84154-492">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="84154-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84154-493">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="84154-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="84154-494">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="84154-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="84154-495">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="84154-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="84154-496">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="84154-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84154-497">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="84154-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-498">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="84154-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84154-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-500">Si **es true**, el módem admite la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="84154-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="84154-501">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="84154-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-502">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="84154-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84154-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-504">Si es **true**, se admite la comunicación sincrónica y asincrónica.</span><span class="sxs-lookup"><span data-stu-id="84154-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="84154-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84154-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-506">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-508">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="84154-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="84154-509">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="84154-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="84154-510">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="84154-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-512">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="84154-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84154-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84154-514">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="84154-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="84154-515">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="84154-515">Scoping system's name.</span></span>

<span data-ttu-id="84154-516">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="84154-517">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="84154-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84154-518">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84154-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84154-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="84154-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84154-520">Fecha y hora en que se restableció por última vez este controlador.</span><span class="sxs-lookup"><span data-stu-id="84154-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="84154-521">Esto podría significar que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="84154-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84154-522">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84154-522">Remarks</span></span>

<span data-ttu-id="84154-523">La **clase \_ POTSModem de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="84154-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="84154-524">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="84154-524">WMI does not implement this class.</span></span> <span data-ttu-id="84154-525">Para las clases WMI derivadas de **CIM \_ POTSModem**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="84154-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="84154-526">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="84154-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="84154-527">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="84154-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="84154-528">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84154-528">Requirements</span></span>



| <span data-ttu-id="84154-529">Requisito</span><span class="sxs-lookup"><span data-stu-id="84154-529">Requirement</span></span> | <span data-ttu-id="84154-530">Value</span><span class="sxs-lookup"><span data-stu-id="84154-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84154-531">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84154-531">Minimum supported client</span></span><br/> | <span data-ttu-id="84154-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84154-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84154-533">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84154-533">Minimum supported server</span></span><br/> | <span data-ttu-id="84154-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84154-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84154-535">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84154-535">Namespace</span></span><br/>                | <span data-ttu-id="84154-536">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="84154-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84154-537">MOF</span><span class="sxs-lookup"><span data-stu-id="84154-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84154-538"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84154-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84154-539">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84154-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84154-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84154-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84154-541">Vea también</span><span class="sxs-lookup"><span data-stu-id="84154-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84154-542">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="84154-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

