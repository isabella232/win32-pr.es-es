---
description: La \_ Asociación ParallelController de CIM se relaciona con las capacidades y la administración del dispositivo lógico de puerto paralelo.
ms.assetid: c05e79b6-f3a6-48cc-a831-b67e216f43eb
ms.tgt_platform: multiple
title: CIM_ParallelController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParallelController
- CIM_ParallelController.Availability
- CIM_ParallelController.Capabilities
- CIM_ParallelController.CapabilityDescriptions
- CIM_ParallelController.Caption
- CIM_ParallelController.ConfigManagerErrorCode
- CIM_ParallelController.ConfigManagerUserConfig
- CIM_ParallelController.CreationClassName
- CIM_ParallelController.Description
- CIM_ParallelController.DeviceID
- CIM_ParallelController.DMASupport
- CIM_ParallelController.ErrorCleared
- CIM_ParallelController.ErrorDescription
- CIM_ParallelController.InstallDate
- CIM_ParallelController.LastErrorCode
- CIM_ParallelController.MaxNumberControlled
- CIM_ParallelController.Name
- CIM_ParallelController.PNPDeviceID
- CIM_ParallelController.PowerManagementCapabilities
- CIM_ParallelController.PowerManagementSupported
- CIM_ParallelController.ProtocolSupported
- CIM_ParallelController.Status
- CIM_ParallelController.StatusInfo
- CIM_ParallelController.SystemCreationClassName
- CIM_ParallelController.SystemName
- CIM_ParallelController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc21290de08b6e22c0bc69ec127f3c996ee5b65e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539171"
---
# <a name="cim_parallelcontroller-class"></a><span data-ttu-id="5e1b6-103">\_Clase ParallelController de CIM</span><span class="sxs-lookup"><span data-stu-id="5e1b6-103">CIM\_ParallelController class</span></span>

<span data-ttu-id="5e1b6-104">La **Asociación \_ ParallelController de CIM** se relaciona con las capacidades y la administración del dispositivo lógico de puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-104">The **CIM\_ParallelController** association relates to the capabilities and management of the parallel port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e1b6-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5e1b6-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5e1b6-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5e1b6-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1b6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e1b6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C552-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ParallelController : CIM_Controller
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
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

## <a name="members"></a><span data-ttu-id="5e1b6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e1b6-110">Members</span></span>

<span data-ttu-id="5e1b6-111">La clase **CIM \_ ParallelController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e1b6-111">The **CIM\_ParallelController** class has these types of members:</span></span>

-   [<span data-ttu-id="5e1b6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e1b6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="5e1b6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e1b6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5e1b6-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5e1b6-114">Methods</span></span>

<span data-ttu-id="5e1b6-115">La clase **CIM \_ ParallelController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-115">The **CIM\_ParallelController** class has these methods.</span></span>



| <span data-ttu-id="5e1b6-116">Método</span><span class="sxs-lookup"><span data-stu-id="5e1b6-116">Method</span></span>                                                                        | <span data-ttu-id="5e1b6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e1b6-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e1b6-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-118">**Reset**</span></span>](reset-method-in-class-cim-parallelcontroller.md)                 | <span data-ttu-id="5e1b6-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="5e1b6-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="5e1b6-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-parallelcontroller.md) | <span data-ttu-id="5e1b6-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="5e1b6-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5e1b6-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e1b6-124">Properties</span></span>

<span data-ttu-id="5e1b6-125">La clase **CIM \_ ParallelController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-125">The **CIM\_ParallelController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e1b6-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-130">Availability and status of the device.</span></span>

<span data-ttu-id="5e1b6-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5e1b6-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b6-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5e1b6-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5e1b6-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5e1b6-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5e1b6-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5e1b6-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="5e1b6-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5e1b6-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="5e1b6-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5e1b6-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5e1b6-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5e1b6-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5e1b6-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5e1b6-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5e1b6-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5e1b6-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-149">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5e1b6-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5e1b6-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5e1b6-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5e1b6-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5e1b6-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5e1b6-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-162">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-164">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puertos paralelos \| de DMTF 003,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-165">Capacidades del controlador paralelo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-165">Capabilities of the parallel controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b6-166">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5e1b6-167">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="5e1b6-168">**XT/at compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="5e1b6-169">**Compatible con PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="5e1b6-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="5e1b6-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="5e1b6-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="5e1b6-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="5e1b6-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-176">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-178">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-178">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-179">Cadenas de forma libre que proporcionan explicaciones detalladas para las características del controlador paralelo indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="5e1b6-179">Free-form strings that provide detailed explanations for the parallel controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="5e1b6-180">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **funciones** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-180">Each entry of this array is related to the entry in the **Capabilities** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="5e1b6-181">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-184">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-185">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-185">Short textual description of the object.</span></span>

<span data-ttu-id="5e1b6-186">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-188">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-190">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-190">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-191">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5e1b6-192">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5e1b6-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5e1b6-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-195">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5e1b6-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5e1b6-197">(1)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-198">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5e1b6-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5e1b6-200">(2)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5e1b6-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5e1b6-202">(3)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-203">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5e1b6-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5e1b6-205">(4)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-206">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-206">Device is not working properly.</span></span> <span data-ttu-id="5e1b6-207">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5e1b6-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5e1b6-209">(5)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-210">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5e1b6-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5e1b6-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-213">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5e1b6-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5e1b6-215">(7)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5e1b6-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5e1b6-217">(8)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-218">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5e1b6-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5e1b6-220">(9)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-221">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-221">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5e1b6-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5e1b6-223">(10)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-224">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5e1b6-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5e1b6-226">(11)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-227">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5e1b6-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5e1b6-229">(12)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-230">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5e1b6-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5e1b6-232">(13)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-233">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5e1b6-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5e1b6-235">(14)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-236">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5e1b6-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5e1b6-238">(15)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-239">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5e1b6-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5e1b6-241">(16)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-242">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5e1b6-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5e1b6-244">(17)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-245">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5e1b6-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5e1b6-247">(18)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-248">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5e1b6-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5e1b6-250">(19)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5e1b6-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5e1b6-252">(20)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-253">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5e1b6-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5e1b6-255">(21)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-256">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-256">System failure.</span></span> <span data-ttu-id="5e1b6-257">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5e1b6-258">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5e1b6-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5e1b6-260">(22)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-261">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5e1b6-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5e1b6-263">(23)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-264">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-264">System failure.</span></span> <span data-ttu-id="5e1b6-265">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5e1b6-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5e1b6-267">(24)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-268">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5e1b6-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5e1b6-270">(25)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-271">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5e1b6-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5e1b6-273">(26)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-274">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5e1b6-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5e1b6-276">(27)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-277">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5e1b6-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5e1b6-279">(28)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-280">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5e1b6-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5e1b6-282">(29)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-283">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5e1b6-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5e1b6-285">(30)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-286">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5e1b6-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5e1b6-288">31</span><span class="sxs-lookup"><span data-stu-id="5e1b6-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-289">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-289">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-291">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-293">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-294">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5e1b6-295">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-299">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-300">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5e1b6-301">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5e1b6-302">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-303">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-306">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-307">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-307">Textual description of the object.</span></span>

<span data-ttu-id="5e1b6-308">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-309">**ID**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-312">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-313">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5e1b6-314">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-315">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-315">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-316">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-318">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puertos paralelos de DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-319">Si es **true**, se admite el acceso directo a memoria (DMA).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-319">If **TRUE**, direct memory access (DMA) is supported.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-321">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-323">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5e1b6-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-328">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5e1b6-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-331">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-333">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-334">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-334">Date and time the object was installed.</span></span> <span data-ttu-id="5e1b6-335">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5e1b6-336">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-338">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-340">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5e1b6-341">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-342">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-342">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-343">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-345">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-346">Número máximo de entidades directamente direccionables admitidas por el controlador.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-346">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="5e1b6-347">Se debe utilizar un valor de 0 (cero) si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-347">A value of 0 (zero) should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="5e1b6-348">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-348">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-349">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-349">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-352">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-352">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-353">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-353">Label by which the object is known.</span></span> <span data-ttu-id="5e1b6-354">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-354">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5e1b6-355">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-355">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-356">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-356">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-357">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-359">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-359">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-360">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-360">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="5e1b6-361">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5e1b6-362">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5e1b6-362">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-364">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-366">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-366">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5e1b6-367">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-367">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b6-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5e1b6-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5e1b6-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5e1b6-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-372">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-372">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5e1b6-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-374">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-374">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5e1b6-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-376">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5e1b6-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5e1b6-377">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-377">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5e1b6-378">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-378">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5e1b6-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-380">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5e1b6-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5e1b6-382">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-383">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-383">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-384">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-386">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-386">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5e1b6-387">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5e1b6-387">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5e1b6-388">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-388">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5e1b6-389">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5e1b6-389">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="5e1b6-390">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-391">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-391">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-392">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-395">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="5e1b6-395">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="5e1b6-396">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-396">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="5e1b6-397">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="5e1b6-397">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5e1b6-398">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b6-399">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="5e1b6-400">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-400">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="5e1b6-401">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-401">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="5e1b6-402">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-402">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="5e1b6-403">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-403">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="5e1b6-404">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-404">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="5e1b6-405">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-405">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="5e1b6-406">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-406">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="5e1b6-407">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-407">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="5e1b6-408">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-408">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="5e1b6-409">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-409">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="5e1b6-410">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-410">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="5e1b6-411">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-411">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="5e1b6-412">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-412">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="5e1b6-413">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-413">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="5e1b6-414">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-414">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="5e1b6-415">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-415">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="5e1b6-416">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-416">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="5e1b6-417">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-417">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="5e1b6-418">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-418">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="5e1b6-419">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-419">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="5e1b6-420">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-420">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="5e1b6-421">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-421">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="5e1b6-422">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-422">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="5e1b6-423">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-423">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="5e1b6-424">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-424">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="5e1b6-425">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-425">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="5e1b6-426">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-426">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="5e1b6-427">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-427">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="5e1b6-428">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-428">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="5e1b6-429">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-429">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="5e1b6-430">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-430">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="5e1b6-431">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-431">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="5e1b6-432">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-432">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="5e1b6-433">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-433">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="5e1b6-434">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-434">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="5e1b6-435">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-435">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="5e1b6-436">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-436">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="5e1b6-437">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-437">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="5e1b6-438">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-438">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="5e1b6-439">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-439">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="5e1b6-440">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-440">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="5e1b6-441">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-441">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="5e1b6-442">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-442">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="5e1b6-443">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-443">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="5e1b6-444">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-444">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-445">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-446">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-448">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-449">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-449">Current status of the object.</span></span> <span data-ttu-id="5e1b6-450">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5e1b6-451">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5e1b6-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5e1b6-452">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5e1b6-453">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5e1b6-454">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b6-455">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5e1b6-456">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5e1b6-457">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5e1b6-458">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5e1b6-459">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5e1b6-460">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5e1b6-461">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5e1b6-462">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5e1b6-463">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-465">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-467">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5e1b6-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-468">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-468">State of the logical device.</span></span> <span data-ttu-id="5e1b6-469">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5e1b6-470">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5e1b6-471">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b6-472">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5e1b6-473">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5e1b6-474">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5e1b6-475">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b6-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-477">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-478">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-479">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-480">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="5e1b6-481">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-483">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-484">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-485">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5e1b6-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-486">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-486">Scoping system's name.</span></span>

<span data-ttu-id="5e1b6-487">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b6-488">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-488">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b6-489">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b6-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e1b6-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b6-491">Fecha y hora de la última vez que se restableció el controlador, lo que significa que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-491">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="5e1b6-492">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-492">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e1b6-493">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e1b6-493">Remarks</span></span>

<span data-ttu-id="5e1b6-494">La clase **CIM \_ ParallelController** se deriva del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-494">The **CIM\_ParallelController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="5e1b6-495">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-495">WMI does not implement this class.</span></span> <span data-ttu-id="5e1b6-496">Para las clases WMI que se derivan de **\_ ParallelController CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b6-496">For WMI classes that are derived from **CIM\_ParallelController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5e1b6-497">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-497">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5e1b6-498">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5e1b6-498">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1b6-499">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e1b6-499">Requirements</span></span>



| <span data-ttu-id="5e1b6-500">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e1b6-500">Requirement</span></span> | <span data-ttu-id="5e1b6-501">Value</span><span class="sxs-lookup"><span data-stu-id="5e1b6-501">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e1b6-502">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e1b6-502">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1b6-503">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e1b6-503">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e1b6-504">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e1b6-504">Minimum supported server</span></span><br/> | <span data-ttu-id="5e1b6-505">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e1b6-505">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e1b6-506">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e1b6-506">Namespace</span></span><br/>                | <span data-ttu-id="5e1b6-507">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5e1b6-507">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e1b6-508">MOF</span><span class="sxs-lookup"><span data-stu-id="5e1b6-508">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e1b6-509"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e1b6-509"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e1b6-510">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e1b6-510">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e1b6-511"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e1b6-511"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e1b6-512">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e1b6-512">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e1b6-513">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="5e1b6-513">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

