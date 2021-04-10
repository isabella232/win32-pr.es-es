---
description: La \_ clase CIM Networking es una clase abstracta que define los conceptos generales de hardware de red (por ejemplo, la dirección permanente o la velocidad de funcionamiento). La información se transmite mediante la \_ Asociación DeviceSAPImplementation de CIM.
ms.assetid: dd44e05a-1124-42c2-aa69-340c06da35a2
ms.tgt_platform: multiple
title: CIM_NetworkAdapter (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter
- CIM_NetworkAdapter.AutoSense
- CIM_NetworkAdapter.Availability
- CIM_NetworkAdapter.Caption
- CIM_NetworkAdapter.ConfigManagerErrorCode
- CIM_NetworkAdapter.ConfigManagerUserConfig
- CIM_NetworkAdapter.CreationClassName
- CIM_NetworkAdapter.Description
- CIM_NetworkAdapter.DeviceID
- CIM_NetworkAdapter.ErrorCleared
- CIM_NetworkAdapter.ErrorDescription
- CIM_NetworkAdapter.InstallDate
- CIM_NetworkAdapter.LastErrorCode
- CIM_NetworkAdapter.MaxSpeed
- CIM_NetworkAdapter.Name
- CIM_NetworkAdapter.NetworkAddresses
- CIM_NetworkAdapter.PermanentAddress
- CIM_NetworkAdapter.PNPDeviceID
- CIM_NetworkAdapter.PowerManagementCapabilities
- CIM_NetworkAdapter.PowerManagementSupported
- CIM_NetworkAdapter.Speed
- CIM_NetworkAdapter.Status
- CIM_NetworkAdapter.StatusInfo
- CIM_NetworkAdapter.SystemCreationClassName
- CIM_NetworkAdapter.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76ec70bb74d74514dfe037c9e67604b29aee541a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153224"
---
# <a name="cim_networkadapter-class"></a><span data-ttu-id="9b85a-104">CIM ( \_ clase)</span><span class="sxs-lookup"><span data-stu-id="9b85a-104">CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="9b85a-105">La **clase \_ CIM** Networking es una clase abstracta que define los conceptos generales de hardware de red (por ejemplo, la dirección permanente o la velocidad de funcionamiento).</span><span class="sxs-lookup"><span data-stu-id="9b85a-105">The **CIM\_NetworkAdapter** class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="9b85a-106">La información se transmite mediante la Asociación [**\_ DeviceSAPImplementation de CIM**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="9b85a-106">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

<span data-ttu-id="9b85a-107">Los adaptadores de red y los puntos de conexión relacionados representan el potencial de conectividad entre los equipos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="9b85a-107">Network adapters and related endpoints represent the potential for connectivity among peers.</span></span> <span data-ttu-id="9b85a-108">La posibilidad de conectividad es significativamente diferente de las relaciones maestra, subordinada y controlada por del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-108">The potential for connectivity is significantly different from the master or subordinate and controller or controlled-by relationships of [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="9b85a-109">Sin embargo, en ocasiones, un único dispositivo actúa como adaptador de red y como controlador, por ejemplo, cuando un adaptador de canal de fibra funciona como controlador SCSI de un equipo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-109">Occasionally, however, a single device acts as both a network adapter and a controller, for example, when a fiber channel adapter operates as a computer system's SCSI controller.</span></span> <span data-ttu-id="9b85a-110">En ese caso, los aspectos del dispositivo están orientados a la red y otros están orientados a los controladores.</span><span class="sxs-lookup"><span data-stu-id="9b85a-110">In which case, aspects of the device are network oriented and others are controller oriented.</span></span> <span data-ttu-id="9b85a-111">Se debe crear una instancia de las clases de controlador y adaptador y también se debe crear una relación de identidad de dispositivo para vincular los distintos aspectos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-111">The controller and adapter classes should be instantiated and a device identity relationship should also be created to link the different aspects of the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b85a-112">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9b85a-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b85a-113">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b85a-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b85a-114">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b85a-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9b85a-115">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9b85a-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b85a-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b85a-116">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C532-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_NetworkAdapter : CIM_LogicalDevice
{
  boolean  AutoSense;
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
  uint64   MaxSpeed;
  string   Name;
  string   NetworkAddresses[];
  string   PermanentAddress;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9b85a-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b85a-117">Members</span></span>

<span data-ttu-id="9b85a-118">La clase **CIM \_ adaptador** de tipo tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b85a-118">The **CIM\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="9b85a-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b85a-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="9b85a-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b85a-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9b85a-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b85a-121">Methods</span></span>

<span data-ttu-id="9b85a-122">La clase **CIM \_ adaptador** de la clase tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9b85a-122">The **CIM\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="9b85a-123">Método</span><span class="sxs-lookup"><span data-stu-id="9b85a-123">Method</span></span>                                                                    | <span data-ttu-id="9b85a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b85a-124">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b85a-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9b85a-125">**Reset**</span></span>](reset-method-in-class-cim-networkadapter.md)                 | <span data-ttu-id="9b85a-126">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b85a-126">Requests a reset of the logical device.</span></span> <span data-ttu-id="9b85a-127">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="9b85a-127">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9b85a-128">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9b85a-128">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-networkadapter.md) | <span data-ttu-id="9b85a-129">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-129">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9b85a-130">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="9b85a-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9b85a-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b85a-131">Properties</span></span>

<span data-ttu-id="9b85a-132">La clase **CIM \_ adaptador** de clase tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b85a-132">The **CIM\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b85a-133">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="9b85a-133">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b85a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-136">Si **es true**, el adaptador de red puede determinar automáticamente la velocidad u otras características de comunicación del medio de red conectado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-136">If **TRUE**, the network adapter can automatically determine the speed or other communications characteristics of the attached network media.</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-137">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="9b85a-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-138">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b85a-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9b85a-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-141">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-141">Availability and status of the device.</span></span>

<span data-ttu-id="9b85a-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b85a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9b85a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b85a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9b85a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9b85a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9b85a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9b85a-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="9b85a-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9b85a-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="9b85a-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9b85a-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9b85a-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9b85a-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="9b85a-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9b85a-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="9b85a-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9b85a-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="9b85a-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b85a-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="9b85a-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9b85a-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="9b85a-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9b85a-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="9b85a-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9b85a-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="9b85a-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-156">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="9b85a-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9b85a-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="9b85a-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-158">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9b85a-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="9b85a-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-160">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="9b85a-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9b85a-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="9b85a-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9b85a-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="9b85a-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-163">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="9b85a-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9b85a-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9b85a-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-165">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9b85a-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9b85a-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="9b85a-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-167">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9b85a-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="9b85a-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-169">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9b85a-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9b85a-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-171">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="9b85a-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b85a-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9b85a-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-175">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9b85a-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-176">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b85a-176">Short textual description of the object.</span></span>

<span data-ttu-id="9b85a-177">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9b85a-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-179">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b85a-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-181">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b85a-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-182">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9b85a-182">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9b85a-183">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9b85a-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9b85a-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="9b85a-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-186">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b85a-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9b85a-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9b85a-188">(1)</span><span class="sxs-lookup"><span data-stu-id="9b85a-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-189">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b85a-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b85a-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9b85a-191">(2)</span><span class="sxs-lookup"><span data-stu-id="9b85a-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9b85a-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9b85a-193">(3)</span><span class="sxs-lookup"><span data-stu-id="9b85a-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-194">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="9b85a-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9b85a-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9b85a-196">(4)</span><span class="sxs-lookup"><span data-stu-id="9b85a-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-197">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9b85a-197">Device is not working properly.</span></span> <span data-ttu-id="9b85a-198">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="9b85a-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9b85a-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9b85a-200">(5)</span><span class="sxs-lookup"><span data-stu-id="9b85a-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-201">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="9b85a-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9b85a-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9b85a-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="9b85a-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-204">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9b85a-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9b85a-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9b85a-206">(7)</span><span class="sxs-lookup"><span data-stu-id="9b85a-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9b85a-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9b85a-208">(8)</span><span class="sxs-lookup"><span data-stu-id="9b85a-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-209">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9b85a-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9b85a-211">(9)</span><span class="sxs-lookup"><span data-stu-id="9b85a-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-212">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9b85a-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9b85a-214">(10)</span><span class="sxs-lookup"><span data-stu-id="9b85a-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-215">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="9b85a-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9b85a-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9b85a-217">(11)</span><span class="sxs-lookup"><span data-stu-id="9b85a-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-218">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9b85a-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9b85a-220">(12)</span><span class="sxs-lookup"><span data-stu-id="9b85a-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-221">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="9b85a-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9b85a-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9b85a-223">(13)</span><span class="sxs-lookup"><span data-stu-id="9b85a-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-224">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9b85a-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9b85a-226">(14)</span><span class="sxs-lookup"><span data-stu-id="9b85a-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-227">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9b85a-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9b85a-229">(15)</span><span class="sxs-lookup"><span data-stu-id="9b85a-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-230">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="9b85a-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9b85a-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9b85a-232">(16)</span><span class="sxs-lookup"><span data-stu-id="9b85a-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-233">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9b85a-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9b85a-235">(17)</span><span class="sxs-lookup"><span data-stu-id="9b85a-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-236">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="9b85a-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b85a-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9b85a-238">(18)</span><span class="sxs-lookup"><span data-stu-id="9b85a-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-239">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9b85a-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9b85a-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9b85a-241">(19)</span><span class="sxs-lookup"><span data-stu-id="9b85a-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9b85a-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9b85a-243">(20)</span><span class="sxs-lookup"><span data-stu-id="9b85a-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-244">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9b85a-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9b85a-246">(21)</span><span class="sxs-lookup"><span data-stu-id="9b85a-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-247">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="9b85a-247">System failure.</span></span> <span data-ttu-id="9b85a-248">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="9b85a-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9b85a-249">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9b85a-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9b85a-251">(22)</span><span class="sxs-lookup"><span data-stu-id="9b85a-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-252">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9b85a-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9b85a-254">(23)</span><span class="sxs-lookup"><span data-stu-id="9b85a-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-255">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="9b85a-255">System failure.</span></span> <span data-ttu-id="9b85a-256">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="9b85a-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9b85a-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9b85a-258">(24)</span><span class="sxs-lookup"><span data-stu-id="9b85a-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-259">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="9b85a-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9b85a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9b85a-261">(25)</span><span class="sxs-lookup"><span data-stu-id="9b85a-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-262">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9b85a-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9b85a-264">(26)</span><span class="sxs-lookup"><span data-stu-id="9b85a-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-265">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b85a-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9b85a-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9b85a-267">(27)</span><span class="sxs-lookup"><span data-stu-id="9b85a-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-268">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="9b85a-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9b85a-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9b85a-270">(28)</span><span class="sxs-lookup"><span data-stu-id="9b85a-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-271">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="9b85a-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9b85a-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9b85a-273">(29)</span><span class="sxs-lookup"><span data-stu-id="9b85a-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-274">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9b85a-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9b85a-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9b85a-276">(30)</span><span class="sxs-lookup"><span data-stu-id="9b85a-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-277">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="9b85a-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9b85a-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9b85a-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9b85a-279">31</span><span class="sxs-lookup"><span data-stu-id="9b85a-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-280">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9b85a-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b85a-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9b85a-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-282">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b85a-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-284">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b85a-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-285">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9b85a-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9b85a-286">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9b85a-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-290">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b85a-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-291">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="9b85a-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9b85a-292">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="9b85a-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9b85a-293">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-294">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9b85a-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-297">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9b85a-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-298">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b85a-298">Textual description of the object.</span></span>

<span data-ttu-id="9b85a-299">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-300">**ID**</span><span class="sxs-lookup"><span data-stu-id="9b85a-300">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-303">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b85a-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-304">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b85a-304">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9b85a-305">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-306">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9b85a-306">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-307">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b85a-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-309">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-309">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9b85a-310">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-311">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9b85a-311">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-314">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="9b85a-314">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9b85a-315">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-316">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9b85a-316">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-317">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b85a-317">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-319">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9b85a-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-320">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9b85a-320">Date and time the object was installed.</span></span> <span data-ttu-id="9b85a-321">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9b85a-321">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9b85a-322">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-323">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9b85a-323">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-324">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b85a-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-326">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b85a-326">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9b85a-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-328">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="9b85a-328">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-329">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b85a-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-331">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="9b85a-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-332">Velocidad máxima, en bits por segundo (BPS), del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b85a-332">Maximum speed, in bits per second (BPS), for the network adapter.</span></span>

<span data-ttu-id="9b85a-333">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b85a-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-334">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9b85a-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-335">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-337">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9b85a-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-338">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9b85a-338">Label by which the object is known.</span></span> <span data-ttu-id="9b85a-339">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="9b85a-339">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9b85a-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-341">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="9b85a-341">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-342">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9b85a-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-344">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de red DMTF 802 puerto \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="9b85a-344">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-345">Lista de direcciones de red de un adaptador.</span><span class="sxs-lookup"><span data-stu-id="9b85a-345">List of network addresses for an adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-346">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="9b85a-346">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-349">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de red DMTF 802 puerto \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="9b85a-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-350">Dirección de red codificada de forma rígida en un adaptador.</span><span class="sxs-lookup"><span data-stu-id="9b85a-350">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="9b85a-351">La dirección codificada de forma rígida se puede cambiar con una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="9b85a-351">The hard-coded address can be changed with a firmware upgrade or software configuration.</span></span> <span data-ttu-id="9b85a-352">Si se cambia, el campo debe actualizarse cuando se realiza el cambio.</span><span class="sxs-lookup"><span data-stu-id="9b85a-352">If changed, the field should be updated when the change is made.</span></span> <span data-ttu-id="9b85a-353">Esta propiedad debe dejarse en blanco si no existe ninguna dirección codificada de forma rígida para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="9b85a-353">This property should be left blank if no hard-coded address exists for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-354">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9b85a-354">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-357">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9b85a-357">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-358">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b85a-358">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9b85a-359">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9b85a-360">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9b85a-360">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-361">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9b85a-361">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-362">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b85a-362">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-364">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b85a-364">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9b85a-365">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="9b85a-365">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b85a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9b85a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9b85a-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="9b85a-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b85a-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9b85a-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b85a-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9b85a-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-370">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9b85a-370">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9b85a-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9b85a-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-372">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="9b85a-372">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9b85a-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="9b85a-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-374">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="9b85a-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9b85a-375">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="9b85a-375">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9b85a-376">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9b85a-376">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9b85a-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="9b85a-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-378">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="9b85a-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9b85a-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="9b85a-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9b85a-380">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="9b85a-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9b85a-381">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9b85a-381">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-382">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9b85a-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-384">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="9b85a-384">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9b85a-385">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9b85a-385">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9b85a-386">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="9b85a-386">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9b85a-387">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9b85a-387">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9b85a-388">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-388">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-389">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="9b85a-389">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-390">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9b85a-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-392">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Adaptador de red DMTF 802 puerto \| 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits por segundo ")</span><span class="sxs-lookup"><span data-stu-id="9b85a-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-393">Estimación del ancho de banda actual, en BPS.</span><span class="sxs-lookup"><span data-stu-id="9b85a-393">Estimate of the current bandwidth, in BPS.</span></span> <span data-ttu-id="9b85a-394">En el caso de los puntos de conexión que varían en ancho de banda o para aquellos en los que no se puede realizar una estimación precisa, esta propiedad debe contener el ancho de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="9b85a-394">For endpoints that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="9b85a-395">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9b85a-395">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-396">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9b85a-396">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-397">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-399">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9b85a-399">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-400">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b85a-400">Current status of the object.</span></span>

<span data-ttu-id="9b85a-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9b85a-402">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b85a-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9b85a-403">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9b85a-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9b85a-404">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9b85a-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9b85a-405">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9b85a-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b85a-406">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9b85a-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9b85a-407">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9b85a-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9b85a-408">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9b85a-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9b85a-409">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9b85a-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b85a-410">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9b85a-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9b85a-411">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9b85a-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9b85a-412">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9b85a-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9b85a-413">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9b85a-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9b85a-414">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9b85a-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b85a-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9b85a-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-416">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9b85a-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-418">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9b85a-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-419">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9b85a-419">State of the logical device.</span></span> <span data-ttu-id="9b85a-420">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="9b85a-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9b85a-421">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9b85a-422">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9b85a-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9b85a-423">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9b85a-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b85a-424">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9b85a-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b85a-425">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="9b85a-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9b85a-426">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9b85a-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b85a-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9b85a-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-430">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b85a-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-431">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9b85a-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="9b85a-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b85a-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9b85a-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b85a-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9b85a-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b85a-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b85a-436">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b85a-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b85a-437">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9b85a-437">Scoping system's name.</span></span>

<span data-ttu-id="9b85a-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b85a-439">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b85a-439">Remarks</span></span>

<span data-ttu-id="9b85a-440">La clase de **\_ adaptador** de la CIM se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-440">The **CIM\_NetworkAdapter** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9b85a-441">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9b85a-441">WMI does not implement this class.</span></span> <span data-ttu-id="9b85a-442">Para las clases que se derivan de la **\_ adaptador** de la clase CIM, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9b85a-442">For classes that are derived from **CIM\_NetworkAdapter**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9b85a-443">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b85a-443">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b85a-444">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9b85a-444">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b85a-445">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b85a-445">Requirements</span></span>



| <span data-ttu-id="9b85a-446">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b85a-446">Requirement</span></span> | <span data-ttu-id="9b85a-447">Value</span><span class="sxs-lookup"><span data-stu-id="9b85a-447">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b85a-448">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b85a-448">Minimum supported client</span></span><br/> | <span data-ttu-id="9b85a-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b85a-449">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b85a-450">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b85a-450">Minimum supported server</span></span><br/> | <span data-ttu-id="9b85a-451">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b85a-451">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b85a-452">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b85a-452">Namespace</span></span><br/>                | <span data-ttu-id="9b85a-453">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9b85a-453">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b85a-454">MOF</span><span class="sxs-lookup"><span data-stu-id="9b85a-454">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b85a-455"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b85a-455"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b85a-456">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b85a-456">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b85a-457"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b85a-457"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b85a-458">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b85a-458">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b85a-459">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9b85a-459">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

