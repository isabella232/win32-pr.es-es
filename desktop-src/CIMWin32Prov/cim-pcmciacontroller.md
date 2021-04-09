---
description: La \_ clase CIM PCMCIAController representa las capacidades y la administración de un controlador de la Asociación Internacional de tarjetas de memoria (PCMCIA) del equipo.
ms.assetid: 341cbc6c-dd25-4dea-bcce-cd4e3f4d5324
ms.tgt_platform: multiple
title: CIM_PCMCIAController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController
- CIM_PCMCIAController.Availability
- CIM_PCMCIAController.Caption
- CIM_PCMCIAController.ConfigManagerErrorCode
- CIM_PCMCIAController.ConfigManagerUserConfig
- CIM_PCMCIAController.CreationClassName
- CIM_PCMCIAController.Description
- CIM_PCMCIAController.DeviceID
- CIM_PCMCIAController.ErrorCleared
- CIM_PCMCIAController.ErrorDescription
- CIM_PCMCIAController.InstallDate
- CIM_PCMCIAController.LastErrorCode
- CIM_PCMCIAController.Manufacturer
- CIM_PCMCIAController.MaxNumberControlled
- CIM_PCMCIAController.Name
- CIM_PCMCIAController.PNPDeviceID
- CIM_PCMCIAController.PowerManagementCapabilities
- CIM_PCMCIAController.PowerManagementSupported
- CIM_PCMCIAController.ProtocolSupported
- CIM_PCMCIAController.Status
- CIM_PCMCIAController.StatusInfo
- CIM_PCMCIAController.SystemCreationClassName
- CIM_PCMCIAController.SystemName
- CIM_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95d05e11dd0c439708c477e3ec776bc7a2c333d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153008"
---
# <a name="cim_pcmciacontroller-class"></a><span data-ttu-id="b158d-103">\_Clase PCMCIAController de CIM</span><span class="sxs-lookup"><span data-stu-id="b158d-103">CIM\_PCMCIAController class</span></span>

<span data-ttu-id="b158d-104">La clase **CIM \_ PCMCIAController** representa las capacidades y la administración de un controlador de la Asociación Internacional de tarjetas de memoria (PCMCIA) del equipo.</span><span class="sxs-lookup"><span data-stu-id="b158d-104">The **CIM\_PCMCIAController** class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b158d-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b158d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b158d-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b158d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b158d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b158d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b158d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b158d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b158d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b158d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PCMCIAController : cim_controller
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="b158d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b158d-110">Members</span></span>

<span data-ttu-id="b158d-111">La clase **CIM \_ PCMCIAController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b158d-111">The **CIM\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="b158d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b158d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b158d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b158d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b158d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b158d-114">Methods</span></span>

<span data-ttu-id="b158d-115">La clase **CIM \_ PCMCIAController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b158d-115">The **CIM\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="b158d-116">Método</span><span class="sxs-lookup"><span data-stu-id="b158d-116">Method</span></span>                                                                      | <span data-ttu-id="b158d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b158d-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b158d-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b158d-118">**Reset**</span></span>](reset-method-in-class-cim-pcmciacontroller.md)                 | <span data-ttu-id="b158d-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b158d-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b158d-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b158d-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b158d-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b158d-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcmciacontroller.md) | <span data-ttu-id="b158d-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="b158d-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b158d-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b158d-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b158d-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b158d-124">Properties</span></span>

<span data-ttu-id="b158d-125">La clase **CIM \_ PCMCIAController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b158d-125">The **CIM\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b158d-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b158d-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b158d-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b158d-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-130">Availability and status of the device.</span></span> <span data-ttu-id="b158d-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b158d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b158d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-133">Otros.</span><span class="sxs-lookup"><span data-stu-id="b158d-133">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b158d-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b158d-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-135">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="b158d-135">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b158d-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b158d-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-137">En ejecución o completa.</span><span class="sxs-lookup"><span data-stu-id="b158d-137">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b158d-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="b158d-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-139">Advertencia.</span><span class="sxs-lookup"><span data-stu-id="b158d-139">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b158d-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="b158d-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-141">Pruebas.</span><span class="sxs-lookup"><span data-stu-id="b158d-141">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b158d-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="b158d-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-143">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="b158d-143">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b158d-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="b158d-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-145">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="b158d-145">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b158d-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="b158d-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-147">N.</span><span class="sxs-lookup"><span data-stu-id="b158d-147">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b158d-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="b158d-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-149">Fuera de servicio.</span><span class="sxs-lookup"><span data-stu-id="b158d-149">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b158d-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="b158d-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-151">Degradado.</span><span class="sxs-lookup"><span data-stu-id="b158d-151">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b158d-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="b158d-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-153">No instalado.</span><span class="sxs-lookup"><span data-stu-id="b158d-153">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b158d-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="b158d-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-155">Error de instalación.</span><span class="sxs-lookup"><span data-stu-id="b158d-155">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b158d-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="b158d-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-157">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto en este modo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="b158d-157">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b158d-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="b158d-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-159">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="b158d-159">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b158d-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="b158d-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-161">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="b158d-161">Device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b158d-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="b158d-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-163">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="b158d-163">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b158d-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="b158d-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-165">El dispositivo está en un estado de advertencia y también en un modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b158d-165">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b158d-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b158d-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-167">En pausa.</span><span class="sxs-lookup"><span data-stu-id="b158d-167">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b158d-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="b158d-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-169">No está listo.</span><span class="sxs-lookup"><span data-stu-id="b158d-169">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b158d-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="b158d-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-171">No configurado.</span><span class="sxs-lookup"><span data-stu-id="b158d-171">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b158d-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b158d-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-173">El controlador PCMCIA no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b158d-173">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b158d-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b158d-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-177">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b158d-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-178">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b158d-178">Short textual description of the object.</span></span>

<span data-ttu-id="b158d-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b158d-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-181">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b158d-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-183">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b158d-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-184">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="b158d-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b158d-185">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b158d-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="b158d-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b158d-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="b158d-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-188">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b158d-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b158d-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="b158d-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b158d-190">(1)</span><span class="sxs-lookup"><span data-stu-id="b158d-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-191">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b158d-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b158d-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b158d-193">(2)</span><span class="sxs-lookup"><span data-stu-id="b158d-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b158d-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="b158d-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b158d-195">(3)</span><span class="sxs-lookup"><span data-stu-id="b158d-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-196">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="b158d-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b158d-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="b158d-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b158d-198">(4)</span><span class="sxs-lookup"><span data-stu-id="b158d-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-199">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b158d-199">Device is not working properly.</span></span> <span data-ttu-id="b158d-200">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="b158d-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b158d-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="b158d-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b158d-202">(5)</span><span class="sxs-lookup"><span data-stu-id="b158d-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-203">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="b158d-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b158d-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="b158d-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b158d-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="b158d-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-206">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b158d-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b158d-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="b158d-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b158d-208">(7)</span><span class="sxs-lookup"><span data-stu-id="b158d-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b158d-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b158d-210">(8)</span><span class="sxs-lookup"><span data-stu-id="b158d-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-211">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b158d-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="b158d-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b158d-213">(9)</span><span class="sxs-lookup"><span data-stu-id="b158d-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-214">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b158d-214">Device is not working properly.</span></span> <span data-ttu-id="b158d-215">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b158d-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="b158d-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b158d-217">(10)</span><span class="sxs-lookup"><span data-stu-id="b158d-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-218">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="b158d-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b158d-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b158d-220">(11)</span><span class="sxs-lookup"><span data-stu-id="b158d-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-221">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b158d-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="b158d-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b158d-223">(12)</span><span class="sxs-lookup"><span data-stu-id="b158d-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-224">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="b158d-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b158d-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b158d-226">(13)</span><span class="sxs-lookup"><span data-stu-id="b158d-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-227">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b158d-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b158d-229">(14)</span><span class="sxs-lookup"><span data-stu-id="b158d-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-230">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="b158d-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b158d-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="b158d-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b158d-232">(15)</span><span class="sxs-lookup"><span data-stu-id="b158d-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-233">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="b158d-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b158d-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b158d-235">(16)</span><span class="sxs-lookup"><span data-stu-id="b158d-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-236">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b158d-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="b158d-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b158d-238">(17)</span><span class="sxs-lookup"><span data-stu-id="b158d-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-239">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="b158d-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b158d-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b158d-241">(18)</span><span class="sxs-lookup"><span data-stu-id="b158d-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-242">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b158d-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b158d-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="b158d-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b158d-244">(19)</span><span class="sxs-lookup"><span data-stu-id="b158d-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b158d-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="b158d-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b158d-246">(20)</span><span class="sxs-lookup"><span data-stu-id="b158d-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-247">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="b158d-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b158d-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b158d-249">(21)</span><span class="sxs-lookup"><span data-stu-id="b158d-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-250">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b158d-250">System failure.</span></span> <span data-ttu-id="b158d-251">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b158d-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b158d-252">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b158d-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="b158d-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b158d-254">(22)</span><span class="sxs-lookup"><span data-stu-id="b158d-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-255">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b158d-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b158d-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="b158d-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b158d-257">(23)</span><span class="sxs-lookup"><span data-stu-id="b158d-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-258">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b158d-258">System failure.</span></span> <span data-ttu-id="b158d-259">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b158d-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b158d-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="b158d-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b158d-261">(24)</span><span class="sxs-lookup"><span data-stu-id="b158d-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-262">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="b158d-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b158d-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b158d-264">(25)</span><span class="sxs-lookup"><span data-stu-id="b158d-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-265">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b158d-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b158d-267">(26)</span><span class="sxs-lookup"><span data-stu-id="b158d-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-268">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b158d-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b158d-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="b158d-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b158d-270">(27)</span><span class="sxs-lookup"><span data-stu-id="b158d-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-271">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="b158d-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b158d-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="b158d-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b158d-273">(28)</span><span class="sxs-lookup"><span data-stu-id="b158d-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-274">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="b158d-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b158d-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="b158d-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b158d-276">(29)</span><span class="sxs-lookup"><span data-stu-id="b158d-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-277">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b158d-277">Device is disabled.</span></span> <span data-ttu-id="b158d-278">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b158d-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b158d-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="b158d-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b158d-280">(30)</span><span class="sxs-lookup"><span data-stu-id="b158d-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-281">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b158d-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b158d-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b158d-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b158d-283">31</span><span class="sxs-lookup"><span data-stu-id="b158d-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-284">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b158d-284">Device is not working properly.</span></span> <span data-ttu-id="b158d-285">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b158d-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b158d-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b158d-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-287">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b158d-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-289">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b158d-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-290">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b158d-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b158d-291">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b158d-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-295">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b158d-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b158d-296">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b158d-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b158d-297">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b158d-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b158d-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-299">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b158d-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-302">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b158d-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-303">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b158d-303">Textual description of the object.</span></span>

<span data-ttu-id="b158d-304">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-305">**ID**</span><span class="sxs-lookup"><span data-stu-id="b158d-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-308">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b158d-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b158d-309">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b158d-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b158d-310">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b158d-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-312">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b158d-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b158d-314">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="b158d-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b158d-315">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b158d-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b158d-319">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="b158d-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b158d-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b158d-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-322">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b158d-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-324">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b158d-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-325">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b158d-325">Date and time the object was installed.</span></span> <span data-ttu-id="b158d-326">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b158d-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b158d-327">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b158d-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-329">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b158d-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b158d-331">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b158d-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b158d-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-333">**Le**</span><span class="sxs-lookup"><span data-stu-id="b158d-333">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-336">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b158d-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-337">Nombre del fabricante del controlador PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="b158d-337">Name of the PCMCIA controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b158d-338">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="b158d-338">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-339">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b158d-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-341">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="b158d-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-342">Número máximo de entidades directamente direccionables admitidas por el controlador.</span><span class="sxs-lookup"><span data-stu-id="b158d-342">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="b158d-343">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="b158d-343">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="b158d-344">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-344">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-345">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b158d-345">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-348">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b158d-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-349">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b158d-349">Label by which the object is known.</span></span> <span data-ttu-id="b158d-350">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b158d-350">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b158d-351">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-351">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b158d-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-355">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b158d-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-356">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b158d-356">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b158d-357">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b158d-358">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b158d-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b158d-359">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b158d-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-360">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b158d-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b158d-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b158d-362">Capacidades específicas relacionadas con la energía del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b158d-362">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="b158d-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b158d-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b158d-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-365">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="b158d-365">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b158d-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="b158d-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-367">No se admite.</span><span class="sxs-lookup"><span data-stu-id="b158d-367">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b158d-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b158d-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-369">Deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b158d-369">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b158d-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b158d-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-371">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b158d-371">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b158d-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b158d-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-373">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="b158d-373">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b158d-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="b158d-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-375">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="b158d-375">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b158d-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="b158d-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-377">El método [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="b158d-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b158d-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="b158d-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b158d-379">El método [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="b158d-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b158d-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b158d-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-381">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b158d-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b158d-383">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b158d-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b158d-384">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b158d-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b158d-385">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="b158d-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b158d-386">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b158d-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b158d-387">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-388">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="b158d-388">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-389">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b158d-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-391">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b158d-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-392">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="b158d-392">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="b158d-393">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-393">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="b158d-394">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="b158d-394">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b158d-395">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b158d-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b158d-396">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b158d-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="b158d-397">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="b158d-397">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="b158d-398">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="b158d-398">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="b158d-399">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="b158d-399">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="b158d-400">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="b158d-400">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="b158d-401">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="b158d-401">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="b158d-402">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="b158d-402">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="b158d-403">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="b158d-403">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="b158d-404">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="b158d-404">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="b158d-405">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="b158d-405">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="b158d-406">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="b158d-406">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="b158d-407">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="b158d-407">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="b158d-408">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="b158d-408">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="b158d-409">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="b158d-409">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="b158d-410">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="b158d-410">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="b158d-411">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="b158d-411">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="b158d-412">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="b158d-412">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="b158d-413">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="b158d-413">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="b158d-414">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="b158d-414">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="b158d-415">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="b158d-415">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="b158d-416">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="b158d-416">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="b158d-417">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="b158d-417">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="b158d-418">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="b158d-418">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="b158d-419">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="b158d-419">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="b158d-420">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="b158d-420">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="b158d-421">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="b158d-421">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="b158d-422">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="b158d-422">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="b158d-423">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="b158d-423">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="b158d-424">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="b158d-424">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="b158d-425">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="b158d-425">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="b158d-426">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="b158d-426">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="b158d-427">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="b158d-427">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="b158d-428">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="b158d-428">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="b158d-429">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="b158d-429">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="b158d-430">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="b158d-430">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="b158d-431">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="b158d-431">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="b158d-432">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="b158d-432">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="b158d-433">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="b158d-433">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="b158d-434">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="b158d-434">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="b158d-435">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="b158d-435">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="b158d-436">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="b158d-436">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="b158d-437">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="b158d-437">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="b158d-438">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="b158d-438">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="b158d-439">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="b158d-439">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="b158d-440">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="b158d-440">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="b158d-441">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="b158d-441">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b158d-442">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b158d-442">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-445">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b158d-445">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-446">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b158d-446">Current status of the object.</span></span> <span data-ttu-id="b158d-447">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b158d-448">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b158d-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b158d-449">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b158d-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b158d-450">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b158d-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b158d-451">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b158d-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b158d-452">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b158d-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b158d-453">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b158d-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b158d-454">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b158d-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b158d-455">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b158d-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b158d-456">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b158d-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b158d-457">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b158d-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b158d-458">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b158d-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b158d-459">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b158d-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b158d-460">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b158d-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b158d-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b158d-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-462">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b158d-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-464">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b158d-464">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b158d-465">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b158d-465">State of the logical device.</span></span> <span data-ttu-id="b158d-466">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="b158d-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b158d-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b158d-468">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b158d-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b158d-469">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b158d-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b158d-470">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b158d-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b158d-471">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="b158d-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b158d-472">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="b158d-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b158d-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b158d-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-476">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b158d-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b158d-477">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b158d-477">Scoping system's creation class name.</span></span>

<span data-ttu-id="b158d-478">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b158d-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-480">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b158d-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b158d-482">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b158d-482">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b158d-483">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b158d-483">Scoping system's name.</span></span>

<span data-ttu-id="b158d-484">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b158d-485">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="b158d-485">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b158d-486">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b158d-486">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b158d-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b158d-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b158d-488">Fecha y hora en que se restableció por última vez este controlador, lo que significa que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="b158d-488">Date and time this controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="b158d-489">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-489">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b158d-490">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b158d-490">Remarks</span></span>

<span data-ttu-id="b158d-491">La clase **CIM \_ PCMCIAController** se deriva del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-491">The **CIM\_PCMCIAController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="b158d-492">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b158d-492">WMI does not implement this class.</span></span> <span data-ttu-id="b158d-493">Para las clases WMI que se derivan de **\_ PCMCIAController CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b158d-493">For WMI classes that are derived from **CIM\_PCMCIAController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b158d-494">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b158d-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b158d-495">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b158d-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b158d-496">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b158d-496">Requirements</span></span>



| <span data-ttu-id="b158d-497">Requisito</span><span class="sxs-lookup"><span data-stu-id="b158d-497">Requirement</span></span> | <span data-ttu-id="b158d-498">Value</span><span class="sxs-lookup"><span data-stu-id="b158d-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b158d-499">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b158d-499">Minimum supported client</span></span><br/> | <span data-ttu-id="b158d-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b158d-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b158d-501">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b158d-501">Minimum supported server</span></span><br/> | <span data-ttu-id="b158d-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b158d-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b158d-503">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b158d-503">Namespace</span></span><br/>                | <span data-ttu-id="b158d-504">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b158d-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b158d-505">MOF</span><span class="sxs-lookup"><span data-stu-id="b158d-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b158d-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b158d-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b158d-507">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b158d-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b158d-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b158d-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b158d-509">Vea también</span><span class="sxs-lookup"><span data-stu-id="b158d-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b158d-510">**\_controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="b158d-510">**cim\_controller**</span></span>](cim-controller.md)
</dt> </dl>

 

