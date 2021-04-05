---
description: La \_ clase del ventilador CIM representa las capacidades y la administración de un dispositivo de refrigeración de ventilador.
ms.assetid: eddfb694-cba1-45e2-998f-f93355520c80
ms.tgt_platform: multiple
title: CIM_Fan (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan
- CIM_Fan.ActiveCooling
- CIM_Fan.Availability
- CIM_Fan.Caption
- CIM_Fan.ConfigManagerErrorCode
- CIM_Fan.ConfigManagerUserConfig
- CIM_Fan.CreationClassName
- CIM_Fan.Description
- CIM_Fan.DesiredSpeed
- CIM_Fan.DeviceID
- CIM_Fan.ErrorCleared
- CIM_Fan.ErrorDescription
- CIM_Fan.InstallDate
- CIM_Fan.LastErrorCode
- CIM_Fan.Name
- CIM_Fan.PNPDeviceID
- CIM_Fan.PowerManagementCapabilities
- CIM_Fan.PowerManagementSupported
- CIM_Fan.Status
- CIM_Fan.StatusInfo
- CIM_Fan.SystemCreationClassName
- CIM_Fan.SystemName
- CIM_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a06e0ddebbdadf7cb4e6dd61afa3fa7c178f661
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907296"
---
# <a name="cim_fan-class"></a><span data-ttu-id="b7f3a-103">\_Clase de ventilador CIM</span><span class="sxs-lookup"><span data-stu-id="b7f3a-103">CIM\_Fan class</span></span>

<span data-ttu-id="b7f3a-104">La clase del **\_ ventilador CIM** representa las capacidades y la administración de un dispositivo de refrigeración de ventilador.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-104">The **CIM\_Fan** class represents the capabilities and management of a fan cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7f3a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b7f3a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b7f3a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b7f3a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f3a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7f3a-109">Syntax</span></span>

``` syntax
[UUID("{0A59C856-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Fan : CIM_CoolingDevice
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="b7f3a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7f3a-110">Members</span></span>

<span data-ttu-id="b7f3a-111">La clase del **\_ ventilador CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b7f3a-111">The **CIM\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="b7f3a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b7f3a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b7f3a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7f3a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b7f3a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b7f3a-114">Methods</span></span>

<span data-ttu-id="b7f3a-115">La clase del **\_ ventilador CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-115">The **CIM\_Fan** class has these methods.</span></span>



| <span data-ttu-id="b7f3a-116">Método</span><span class="sxs-lookup"><span data-stu-id="b7f3a-116">Method</span></span>                                                         | <span data-ttu-id="b7f3a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7f3a-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7f3a-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-118">**Reset**</span></span>](reset-method-in-class-cim-fan.md)                 | <span data-ttu-id="b7f3a-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b7f3a-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b7f3a-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-fan.md) | <span data-ttu-id="b7f3a-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b7f3a-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="b7f3a-124">**SetSpeed**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-124">**SetSpeed**</span></span>](setspeed-method-in-class-cim-fan.md)           | <span data-ttu-id="b7f3a-125">Establece la velocidad del ventilador.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-125">Sets the fan speed.</span></span> <span data-ttu-id="b7f3a-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-126">Not implemented by WMI.</span></span><br/>                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="b7f3a-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7f3a-127">Properties</span></span>

<span data-ttu-id="b7f3a-128">La clase del **\_ ventilador CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-128">The **CIM\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7f3a-129">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-129">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-132">Si **es true**, el dispositivo de enfriamiento proporciona enfriamiento activo (en lugar de pasivo).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-132">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="b7f3a-133">Esta propiedad se hereda de [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-133">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-134">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-138">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-138">Availability and status of the device.</span></span>

<span data-ttu-id="b7f3a-139">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b7f3a-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7f3a-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b7f3a-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b7f3a-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b7f3a-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b7f3a-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b7f3a-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="b7f3a-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b7f3a-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="b7f3a-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b7f3a-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b7f3a-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b7f3a-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b7f3a-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b7f3a-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-153">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b7f3a-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-155">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b7f3a-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-157">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b7f3a-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b7f3a-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-160">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b7f3a-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-162">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b7f3a-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-164">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b7f3a-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-166">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b7f3a-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-168">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7f3a-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-172">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-173">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-173">Short textual description of the object.</span></span>

<span data-ttu-id="b7f3a-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-176">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-178">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-179">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-179">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b7f3a-180">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b7f3a-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b7f3a-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-183">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b7f3a-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b7f3a-185">(1)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-186">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b7f3a-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b7f3a-188">(2)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b7f3a-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b7f3a-190">(3)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-191">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b7f3a-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b7f3a-193">(4)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-194">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-194">Device is not working properly.</span></span> <span data-ttu-id="b7f3a-195">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b7f3a-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b7f3a-197">(5)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-198">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b7f3a-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b7f3a-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-201">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b7f3a-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b7f3a-203">(7)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b7f3a-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b7f3a-205">(8)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-206">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b7f3a-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b7f3a-208">(9)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-209">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b7f3a-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b7f3a-211">(10)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-212">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b7f3a-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b7f3a-214">(11)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-215">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b7f3a-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b7f3a-217">(12)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-218">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b7f3a-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b7f3a-220">(13)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-221">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b7f3a-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b7f3a-223">(14)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-224">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b7f3a-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b7f3a-226">(15)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-227">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b7f3a-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b7f3a-229">(16)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-230">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b7f3a-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b7f3a-232">(17)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-233">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b7f3a-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b7f3a-235">(18)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-236">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b7f3a-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b7f3a-238">(19)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b7f3a-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b7f3a-240">(20)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-241">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b7f3a-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b7f3a-243">(21)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-244">System failure.</span></span> <span data-ttu-id="b7f3a-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b7f3a-246">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b7f3a-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b7f3a-248">(22)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-249">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b7f3a-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b7f3a-251">(23)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-252">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-252">System failure.</span></span> <span data-ttu-id="b7f3a-253">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b7f3a-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b7f3a-255">(24)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-256">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b7f3a-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b7f3a-258">(25)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-259">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b7f3a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b7f3a-261">(26)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-262">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b7f3a-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b7f3a-264">(27)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-265">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b7f3a-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b7f3a-267">(28)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-268">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b7f3a-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b7f3a-270">(29)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-271">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b7f3a-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b7f3a-273">(30)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-274">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b7f3a-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b7f3a-276">31</span><span class="sxs-lookup"><span data-stu-id="b7f3a-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-277">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7f3a-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-279">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-281">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-282">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b7f3a-283">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-287">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-288">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b7f3a-289">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b7f3a-290">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-291">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-294">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-295">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-295">Textual description of the object.</span></span>

<span data-ttu-id="b7f3a-296">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-297">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-297">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-298">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-300">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("revoluciones por minuto")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-301">Velocidad de ventilador solicitada, definida en revoluciones por minuto, cuando se admite un ventilador de velocidad variable.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-301">Requested fan speed, defined in revolutions per minute, when a variable speed fan is supported.</span></span> <span data-ttu-id="b7f3a-302">La velocidad actual está determinada por un sensor ([**\_ tacómetro CIM**](cim-tachometer.md)) que está asociado con el ventilador mediante la [**relación \_ AssociatedSensor de CIM**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f3a-302">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="b7f3a-303">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-303">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-304">**ID**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-304">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-307">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-308">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-308">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b7f3a-309">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-311">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-313">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b7f3a-314">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-318">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b7f3a-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-320">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-320">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-321">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-321">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-323">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-324">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-324">Date and time the object was installed.</span></span> <span data-ttu-id="b7f3a-325">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-325">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b7f3a-326">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-327">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-327">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-328">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-330">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-330">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b7f3a-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-332">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-335">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-336">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-336">Label by which the object is known.</span></span> <span data-ttu-id="b7f3a-337">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-337">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b7f3a-338">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-342">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-343">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-343">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b7f3a-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b7f3a-345">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b7f3a-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-347">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-349">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b7f3a-350">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7f3a-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b7f3a-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-353">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-353">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b7f3a-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b7f3a-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-356">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b7f3a-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-358">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b7f3a-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-360">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b7f3a-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b7f3a-361">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b7f3a-362">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b7f3a-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-364">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b7f3a-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b7f3a-366">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b7f3a-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-368">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-370">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b7f3a-371">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b7f3a-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b7f3a-372">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b7f3a-373">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b7f3a-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b7f3a-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-375">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-375">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-378">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-378">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-379">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-379">Current status of the object.</span></span> <span data-ttu-id="b7f3a-380">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b7f3a-381">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b7f3a-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b7f3a-382">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b7f3a-383">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b7f3a-384">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7f3a-385">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b7f3a-386">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b7f3a-387">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b7f3a-388">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b7f3a-389">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b7f3a-390">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b7f3a-391">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b7f3a-392">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b7f3a-393">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b7f3a-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-395">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-397">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b7f3a-397">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-398">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-398">State of the logical device.</span></span> <span data-ttu-id="b7f3a-399">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-399">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b7f3a-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b7f3a-401">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-401">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7f3a-402">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-402">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b7f3a-403">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-403">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b7f3a-404">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-404">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b7f3a-405">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-405">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b7f3a-406">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-406">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-409">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-409">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-410">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-410">Scoping system's creation class name.</span></span>

<span data-ttu-id="b7f3a-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-412">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-412">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-413">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-415">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b7f3a-415">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-416">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-416">Scoping system's name.</span></span>

<span data-ttu-id="b7f3a-417">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7f3a-418">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-418">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7f3a-419">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-419">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7f3a-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7f3a-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7f3a-421">Si **es true**, el ventilador admite velocidades variables.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-421">If **TRUE**, the fan supports variable speeds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7f3a-422">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7f3a-422">Remarks</span></span>

<span data-ttu-id="b7f3a-423">La clase del **\_ ventilador CIM** se deriva [**de \_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-423">The **CIM\_Fan** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="b7f3a-424">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-424">WMI does not implement this class.</span></span> <span data-ttu-id="b7f3a-425">Para las clases derivadas del **\_ ventilador CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b7f3a-425">For classes derived from **CIM\_Fan**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b7f3a-426">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-426">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b7f3a-427">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b7f3a-427">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f3a-428">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f3a-428">Requirements</span></span>



| <span data-ttu-id="b7f3a-429">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f3a-429">Requirement</span></span> | <span data-ttu-id="b7f3a-430">Value</span><span class="sxs-lookup"><span data-stu-id="b7f3a-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f3a-431">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f3a-431">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f3a-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7f3a-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7f3a-433">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f3a-433">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f3a-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7f3a-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7f3a-435">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7f3a-435">Namespace</span></span><br/>                | <span data-ttu-id="b7f3a-436">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b7f3a-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7f3a-437">MOF</span><span class="sxs-lookup"><span data-stu-id="b7f3a-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7f3a-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7f3a-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7f3a-439">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7f3a-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f3a-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7f3a-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f3a-441">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f3a-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f3a-442">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b7f3a-442">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

