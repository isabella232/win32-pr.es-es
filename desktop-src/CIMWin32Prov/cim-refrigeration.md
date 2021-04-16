---
description: La \_ clase de refrigeración CIM representa las capacidades y la administración de un dispositivo de enfriamiento de refrigeración.
ms.assetid: 3ea557d8-6af3-4851-b667-a9afc1219cc7
ms.tgt_platform: multiple
title: CIM_Refrigeration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Refrigeration
- CIM_Refrigeration.ActiveCooling
- CIM_Refrigeration.Availability
- CIM_Refrigeration.Caption
- CIM_Refrigeration.ConfigManagerErrorCode
- CIM_Refrigeration.ConfigManagerUserConfig
- CIM_Refrigeration.CreationClassName
- CIM_Refrigeration.Description
- CIM_Refrigeration.DeviceID
- CIM_Refrigeration.ErrorCleared
- CIM_Refrigeration.ErrorDescription
- CIM_Refrigeration.InstallDate
- CIM_Refrigeration.LastErrorCode
- CIM_Refrigeration.Name
- CIM_Refrigeration.PNPDeviceID
- CIM_Refrigeration.PowerManagementCapabilities
- CIM_Refrigeration.PowerManagementSupported
- CIM_Refrigeration.Status
- CIM_Refrigeration.StatusInfo
- CIM_Refrigeration.SystemCreationClassName
- CIM_Refrigeration.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f714acdfeb1bab37093ed2a7dee7098188c31f48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659415"
---
# <a name="cim_refrigeration-class"></a><span data-ttu-id="90e2d-103">\_Clase de refrigeración CIM</span><span class="sxs-lookup"><span data-stu-id="90e2d-103">CIM\_Refrigeration class</span></span>

<span data-ttu-id="90e2d-104">La clase de **\_ refrigeración CIM** representa las capacidades y la administración de un dispositivo de enfriamiento de refrigeración.</span><span class="sxs-lookup"><span data-stu-id="90e2d-104">The **CIM\_Refrigeration** class represents the capabilities and management of a refrigeration cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90e2d-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="90e2d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="90e2d-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="90e2d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="90e2d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="90e2d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="90e2d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="90e2d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e2d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90e2d-109">Syntax</span></span>

``` syntax
[UUID("{F3A5233A-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Refrigeration : CIM_CoolingDevice
{
  boolean  ActiveCooling;
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="90e2d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="90e2d-110">Members</span></span>

<span data-ttu-id="90e2d-111">La clase de **\_ refrigeración CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="90e2d-111">The **CIM\_Refrigeration** class has these types of members:</span></span>

-   [<span data-ttu-id="90e2d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="90e2d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="90e2d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90e2d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="90e2d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="90e2d-114">Methods</span></span>

<span data-ttu-id="90e2d-115">La clase de **\_ refrigeración CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="90e2d-115">The **CIM\_Refrigeration** class has these methods.</span></span>



| <span data-ttu-id="90e2d-116">Método</span><span class="sxs-lookup"><span data-stu-id="90e2d-116">Method</span></span>                                                                   | <span data-ttu-id="90e2d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="90e2d-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90e2d-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="90e2d-118">**Reset**</span></span>](reset-method-in-class-cim-refrigeration.md)                 | <span data-ttu-id="90e2d-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="90e2d-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="90e2d-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="90e2d-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="90e2d-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="90e2d-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-refrigeration.md) | <span data-ttu-id="90e2d-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="90e2d-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="90e2d-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="90e2d-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90e2d-124">Properties</span></span>

<span data-ttu-id="90e2d-125">La clase de **\_ refrigeración CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="90e2d-125">The **CIM\_Refrigeration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90e2d-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="90e2d-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="90e2d-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-129">Si **es true**, el dispositivo de enfriamiento proporciona enfriamiento activo (en lugar de pasivo).</span><span class="sxs-lookup"><span data-stu-id="90e2d-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="90e2d-130">Esta propiedad se hereda de [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-130">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-131">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="90e2d-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e2d-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-134">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="90e2d-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-135">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-135">Availability and status of the device.</span></span>

<span data-ttu-id="90e2d-136">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="90e2d-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="90e2d-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90e2d-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="90e2d-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="90e2d-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="90e2d-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-140">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="90e2d-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="90e2d-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="90e2d-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="90e2d-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="90e2d-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="90e2d-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="90e2d-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="90e2d-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="90e2d-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="90e2d-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="90e2d-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="90e2d-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="90e2d-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="90e2d-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="90e2d-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="90e2d-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="90e2d-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="90e2d-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="90e2d-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="90e2d-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="90e2d-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-151">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="90e2d-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="90e2d-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="90e2d-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-153">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="90e2d-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="90e2d-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-155">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="90e2d-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="90e2d-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="90e2d-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="90e2d-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="90e2d-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-158">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="90e2d-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="90e2d-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="90e2d-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-160">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="90e2d-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="90e2d-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="90e2d-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-162">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="90e2d-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="90e2d-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-164">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="90e2d-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="90e2d-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-166">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="90e2d-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90e2d-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="90e2d-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="90e2d-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-171">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="90e2d-171">Short textual description of the object.</span></span>

<span data-ttu-id="90e2d-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="90e2d-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90e2d-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-176">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="90e2d-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-177">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="90e2d-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="90e2d-178">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="90e2d-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="90e2d-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="90e2d-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-181">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="90e2d-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="90e2d-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="90e2d-183">(1)</span><span class="sxs-lookup"><span data-stu-id="90e2d-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-184">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="90e2d-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="90e2d-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="90e2d-186">(2)</span><span class="sxs-lookup"><span data-stu-id="90e2d-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="90e2d-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="90e2d-188">(3)</span><span class="sxs-lookup"><span data-stu-id="90e2d-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-189">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="90e2d-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="90e2d-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="90e2d-191">(4)</span><span class="sxs-lookup"><span data-stu-id="90e2d-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-192">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="90e2d-192">Device is not working properly.</span></span> <span data-ttu-id="90e2d-193">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="90e2d-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="90e2d-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="90e2d-195">(5)</span><span class="sxs-lookup"><span data-stu-id="90e2d-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-196">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="90e2d-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="90e2d-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="90e2d-198"> (6)</span><span class="sxs-lookup"><span data-stu-id="90e2d-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-199">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="90e2d-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="90e2d-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="90e2d-201">(7)</span><span class="sxs-lookup"><span data-stu-id="90e2d-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="90e2d-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="90e2d-203">(8)</span><span class="sxs-lookup"><span data-stu-id="90e2d-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-204">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="90e2d-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="90e2d-206">(9)</span><span class="sxs-lookup"><span data-stu-id="90e2d-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-207">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="90e2d-207">Device is not working properly.</span></span> <span data-ttu-id="90e2d-208">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="90e2d-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="90e2d-210">(10)</span><span class="sxs-lookup"><span data-stu-id="90e2d-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-211">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="90e2d-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="90e2d-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="90e2d-213">(11)</span><span class="sxs-lookup"><span data-stu-id="90e2d-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-214">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="90e2d-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="90e2d-216">(12)</span><span class="sxs-lookup"><span data-stu-id="90e2d-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-217">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="90e2d-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="90e2d-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="90e2d-219">(13)</span><span class="sxs-lookup"><span data-stu-id="90e2d-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-220">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="90e2d-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="90e2d-222">(14)</span><span class="sxs-lookup"><span data-stu-id="90e2d-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-223">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="90e2d-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="90e2d-225">(15)</span><span class="sxs-lookup"><span data-stu-id="90e2d-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-226">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="90e2d-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="90e2d-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="90e2d-228">(16)</span><span class="sxs-lookup"><span data-stu-id="90e2d-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-229">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="90e2d-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="90e2d-231">(17)</span><span class="sxs-lookup"><span data-stu-id="90e2d-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-232">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="90e2d-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="90e2d-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="90e2d-234">(18)</span><span class="sxs-lookup"><span data-stu-id="90e2d-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-235">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="90e2d-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="90e2d-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="90e2d-237">(19)</span><span class="sxs-lookup"><span data-stu-id="90e2d-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="90e2d-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="90e2d-239">(20)</span><span class="sxs-lookup"><span data-stu-id="90e2d-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-240">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="90e2d-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="90e2d-242">(21)</span><span class="sxs-lookup"><span data-stu-id="90e2d-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-243">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="90e2d-243">System failure.</span></span> <span data-ttu-id="90e2d-244">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="90e2d-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="90e2d-245">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="90e2d-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="90e2d-247">(22)</span><span class="sxs-lookup"><span data-stu-id="90e2d-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-248">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="90e2d-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="90e2d-250">(23)</span><span class="sxs-lookup"><span data-stu-id="90e2d-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-251">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="90e2d-251">System failure.</span></span> <span data-ttu-id="90e2d-252">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="90e2d-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="90e2d-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="90e2d-254">(24)</span><span class="sxs-lookup"><span data-stu-id="90e2d-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-255">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="90e2d-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="90e2d-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="90e2d-257">(25)</span><span class="sxs-lookup"><span data-stu-id="90e2d-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-258">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="90e2d-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="90e2d-260">(26)</span><span class="sxs-lookup"><span data-stu-id="90e2d-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-261">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="90e2d-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="90e2d-263">(27)</span><span class="sxs-lookup"><span data-stu-id="90e2d-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-264">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="90e2d-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="90e2d-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="90e2d-266">(28)</span><span class="sxs-lookup"><span data-stu-id="90e2d-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-267">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="90e2d-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="90e2d-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="90e2d-269">(29)</span><span class="sxs-lookup"><span data-stu-id="90e2d-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-270">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-270">Device is disabled.</span></span> <span data-ttu-id="90e2d-271">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="90e2d-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="90e2d-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="90e2d-273">(30)</span><span class="sxs-lookup"><span data-stu-id="90e2d-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-274">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="90e2d-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="90e2d-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="90e2d-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="90e2d-276">31</span><span class="sxs-lookup"><span data-stu-id="90e2d-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-277">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="90e2d-277">Device is not working properly.</span></span> <span data-ttu-id="90e2d-278">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="90e2d-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90e2d-279">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="90e2d-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-280">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="90e2d-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-282">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="90e2d-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-283">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="90e2d-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="90e2d-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="90e2d-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-288">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="90e2d-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-289">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="90e2d-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="90e2d-290">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="90e2d-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="90e2d-291">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-292">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90e2d-292">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-295">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="90e2d-295">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-296">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="90e2d-296">Textual description of the object.</span></span>

<span data-ttu-id="90e2d-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-298">**ID**</span><span class="sxs-lookup"><span data-stu-id="90e2d-298">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-301">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="90e2d-301">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-302">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="90e2d-302">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="90e2d-303">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-304">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="90e2d-304">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-305">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="90e2d-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-307">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-307">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="90e2d-308">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-309">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="90e2d-309">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-312">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="90e2d-312">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="90e2d-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-314">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="90e2d-314">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-315">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="90e2d-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-317">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="90e2d-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-318">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="90e2d-318">Date and time the object was installed.</span></span> <span data-ttu-id="90e2d-319">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="90e2d-319">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="90e2d-320">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-320">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-321">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="90e2d-321">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-322">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="90e2d-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-324">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="90e2d-324">Last error code reported by the logical device.</span></span>

<span data-ttu-id="90e2d-325">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-326">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="90e2d-326">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-329">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="90e2d-329">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-330">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="90e2d-330">Label by which the object is known.</span></span> <span data-ttu-id="90e2d-331">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="90e2d-331">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="90e2d-332">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-333">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="90e2d-333">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-336">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="90e2d-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-337">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="90e2d-337">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="90e2d-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="90e2d-339">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="90e2d-339">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-340">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="90e2d-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-341">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e2d-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-343">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="90e2d-343">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="90e2d-344">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="90e2d-344">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90e2d-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="90e2d-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="90e2d-346"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="90e2d-346"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-347">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90e2d-347">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="90e2d-348"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="90e2d-348"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="90e2d-349"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="90e2d-349"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-350">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="90e2d-350">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="90e2d-351"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="90e2d-351"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-352">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="90e2d-352">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="90e2d-353"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="90e2d-353"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-354">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="90e2d-354">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="90e2d-355">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="90e2d-355">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="90e2d-356">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="90e2d-356">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="90e2d-357"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="90e2d-357"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-358">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="90e2d-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="90e2d-359"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="90e2d-359"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="90e2d-360">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="90e2d-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="90e2d-361">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="90e2d-361">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-362">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="90e2d-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-364">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="90e2d-364">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="90e2d-365">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="90e2d-365">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="90e2d-366">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="90e2d-366">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="90e2d-367">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="90e2d-367">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="90e2d-368">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-369">**Estado**</span><span class="sxs-lookup"><span data-stu-id="90e2d-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-372">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="90e2d-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-373">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="90e2d-373">Current status of the object.</span></span> <span data-ttu-id="90e2d-374">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-374">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="90e2d-375">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="90e2d-375">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="90e2d-376">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="90e2d-376">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="90e2d-377">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="90e2d-377">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="90e2d-378">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="90e2d-378">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90e2d-379">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="90e2d-379">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="90e2d-380">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="90e2d-380">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="90e2d-381">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="90e2d-381">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="90e2d-382">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="90e2d-382">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="90e2d-383">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="90e2d-383">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="90e2d-384">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="90e2d-384">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="90e2d-385">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="90e2d-385">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="90e2d-386">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="90e2d-386">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="90e2d-387">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="90e2d-387">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="90e2d-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="90e2d-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-389">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="90e2d-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-391">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="90e2d-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-392">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="90e2d-392">State of the logical device.</span></span> <span data-ttu-id="90e2d-393">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="90e2d-393">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="90e2d-394">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-394">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="90e2d-395">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="90e2d-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="90e2d-396">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="90e2d-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="90e2d-397">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="90e2d-397">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="90e2d-398">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="90e2d-398">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="90e2d-399">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="90e2d-399">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="90e2d-400">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="90e2d-400">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-403">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="90e2d-403">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-404">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="90e2d-404">Scoping system's creation class name.</span></span>

<span data-ttu-id="90e2d-405">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e2d-406">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="90e2d-406">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90e2d-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="90e2d-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="90e2d-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90e2d-409">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="90e2d-409">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="90e2d-410">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="90e2d-410">Scoping system's name.</span></span>

<span data-ttu-id="90e2d-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90e2d-412">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90e2d-412">Remarks</span></span>

<span data-ttu-id="90e2d-413">La clase de **\_ refrigeración CIM** se deriva de [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="90e2d-413">The **CIM\_Refrigeration** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="90e2d-414">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="90e2d-414">WMI does not implement this class.</span></span>

<span data-ttu-id="90e2d-415">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="90e2d-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="90e2d-416">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="90e2d-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e2d-417">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90e2d-417">Requirements</span></span>



| <span data-ttu-id="90e2d-418">Requisito</span><span class="sxs-lookup"><span data-stu-id="90e2d-418">Requirement</span></span> | <span data-ttu-id="90e2d-419">Value</span><span class="sxs-lookup"><span data-stu-id="90e2d-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90e2d-420">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90e2d-420">Minimum supported client</span></span><br/> | <span data-ttu-id="90e2d-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90e2d-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90e2d-422">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90e2d-422">Minimum supported server</span></span><br/> | <span data-ttu-id="90e2d-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90e2d-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90e2d-424">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="90e2d-424">Namespace</span></span><br/>                | <span data-ttu-id="90e2d-425">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="90e2d-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90e2d-426">MOF</span><span class="sxs-lookup"><span data-stu-id="90e2d-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90e2d-427"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90e2d-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90e2d-428">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90e2d-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90e2d-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90e2d-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e2d-430">Vea también</span><span class="sxs-lookup"><span data-stu-id="90e2d-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e2d-431">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="90e2d-431">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

