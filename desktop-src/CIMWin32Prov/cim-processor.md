---
description: La \_ clase de procesador de CIM representa las capacidades y la administración del dispositivo lógico del procesador.
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: CIM_Processor (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496001"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a><span data-ttu-id="e597a-103">CIM_Processor (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e597a-103">CIM_Processor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e597a-104">La clase de **\_ procesador de CIM** representa las capacidades y la administración del dispositivo lógico del procesador.</span><span class="sxs-lookup"><span data-stu-id="e597a-104">The **CIM\_Processor** class represents the capabilities and management of the processor logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e597a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e597a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e597a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e597a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e597a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e597a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e597a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e597a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e597a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e597a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a><span data-ttu-id="e597a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e597a-110">Members</span></span>

<span data-ttu-id="e597a-111">La clase de **\_ procesador de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e597a-111">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="e597a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e597a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e597a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e597a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e597a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e597a-114">Methods</span></span>

<span data-ttu-id="e597a-115">La clase de **\_ procesador de CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e597a-115">The **CIM\_Processor** class has these methods.</span></span>



| <span data-ttu-id="e597a-116">Método</span><span class="sxs-lookup"><span data-stu-id="e597a-116">Method</span></span>                                                               | <span data-ttu-id="e597a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e597a-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e597a-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e597a-118">**Reset**</span></span>](reset-method-in-class-cim-processor.md)                 | <span data-ttu-id="e597a-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e597a-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="e597a-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="e597a-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e597a-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e597a-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-processor.md) | <span data-ttu-id="e597a-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="e597a-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e597a-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="e597a-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e597a-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e597a-124">Properties</span></span>

<span data-ttu-id="e597a-125">La clase de **\_ procesador de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e597a-125">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e597a-126">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="e597a-126">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-129">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="e597a-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-130">Ancho de la dirección del procesador, en bits.</span><span class="sxs-lookup"><span data-stu-id="e597a-130">Processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-131">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="e597a-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-134">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e597a-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-135">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-135">Availability and status of the device.</span></span>

<span data-ttu-id="e597a-136">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e597a-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e597a-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="e597a-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e597a-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="e597a-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-140">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="e597a-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e597a-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="e597a-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e597a-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="e597a-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e597a-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="e597a-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e597a-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="e597a-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e597a-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="e597a-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e597a-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="e597a-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e597a-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="e597a-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e597a-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="e597a-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e597a-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="e597a-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e597a-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="e597a-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-151">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="e597a-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e597a-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="e597a-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-153">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="e597a-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e597a-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="e597a-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-155">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="e597a-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e597a-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="e597a-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e597a-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="e597a-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-158">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="e597a-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e597a-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="e597a-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-160">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="e597a-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e597a-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="e597a-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-162">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="e597a-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e597a-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="e597a-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-164">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="e597a-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e597a-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="e597a-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-166">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="e597a-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e597a-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e597a-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-171">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e597a-171">Short textual description of the object.</span></span>

<span data-ttu-id="e597a-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e597a-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e597a-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-176">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e597a-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-177">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="e597a-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e597a-178">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e597a-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="e597a-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e597a-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="e597a-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-181">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="e597a-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e597a-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="e597a-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e597a-183">(1)</span><span class="sxs-lookup"><span data-stu-id="e597a-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-184">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e597a-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e597a-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e597a-186">(2)</span><span class="sxs-lookup"><span data-stu-id="e597a-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e597a-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="e597a-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e597a-188">(3)</span><span class="sxs-lookup"><span data-stu-id="e597a-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-189">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="e597a-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e597a-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="e597a-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e597a-191">(4)</span><span class="sxs-lookup"><span data-stu-id="e597a-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-192">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="e597a-192">Device is not working properly.</span></span> <span data-ttu-id="e597a-193">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="e597a-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e597a-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="e597a-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e597a-195">(5)</span><span class="sxs-lookup"><span data-stu-id="e597a-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-196">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="e597a-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e597a-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="e597a-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e597a-198"> (6)</span><span class="sxs-lookup"><span data-stu-id="e597a-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-199">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e597a-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e597a-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="e597a-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e597a-201">(7)</span><span class="sxs-lookup"><span data-stu-id="e597a-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e597a-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e597a-203">(8)</span><span class="sxs-lookup"><span data-stu-id="e597a-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-204">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e597a-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="e597a-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e597a-206">(9)</span><span class="sxs-lookup"><span data-stu-id="e597a-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-207">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="e597a-207">Device is not working properly.</span></span> <span data-ttu-id="e597a-208">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e597a-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="e597a-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e597a-210">(10)</span><span class="sxs-lookup"><span data-stu-id="e597a-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-211">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="e597a-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e597a-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e597a-213">(11)</span><span class="sxs-lookup"><span data-stu-id="e597a-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-214">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e597a-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="e597a-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e597a-216">(12)</span><span class="sxs-lookup"><span data-stu-id="e597a-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-217">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="e597a-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e597a-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e597a-219">(13)</span><span class="sxs-lookup"><span data-stu-id="e597a-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-220">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e597a-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e597a-222">(14)</span><span class="sxs-lookup"><span data-stu-id="e597a-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-223">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="e597a-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e597a-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="e597a-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e597a-225">(15)</span><span class="sxs-lookup"><span data-stu-id="e597a-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-226">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="e597a-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e597a-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e597a-228">(16)</span><span class="sxs-lookup"><span data-stu-id="e597a-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-229">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e597a-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="e597a-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e597a-231">(17)</span><span class="sxs-lookup"><span data-stu-id="e597a-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-232">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="e597a-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e597a-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e597a-234">(18)</span><span class="sxs-lookup"><span data-stu-id="e597a-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-235">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e597a-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e597a-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="e597a-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e597a-237">(19)</span><span class="sxs-lookup"><span data-stu-id="e597a-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e597a-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="e597a-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e597a-239">(20)</span><span class="sxs-lookup"><span data-stu-id="e597a-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-240">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="e597a-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e597a-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e597a-242">(21)</span><span class="sxs-lookup"><span data-stu-id="e597a-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-243">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="e597a-243">System failure.</span></span> <span data-ttu-id="e597a-244">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="e597a-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e597a-245">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e597a-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="e597a-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e597a-247">(22)</span><span class="sxs-lookup"><span data-stu-id="e597a-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-248">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e597a-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e597a-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="e597a-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e597a-250">(23)</span><span class="sxs-lookup"><span data-stu-id="e597a-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-251">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="e597a-251">System failure.</span></span> <span data-ttu-id="e597a-252">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="e597a-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e597a-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="e597a-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e597a-254">(24)</span><span class="sxs-lookup"><span data-stu-id="e597a-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-255">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="e597a-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e597a-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e597a-257">(25)</span><span class="sxs-lookup"><span data-stu-id="e597a-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-258">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e597a-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e597a-260">(26)</span><span class="sxs-lookup"><span data-stu-id="e597a-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-261">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e597a-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e597a-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="e597a-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e597a-263">(27)</span><span class="sxs-lookup"><span data-stu-id="e597a-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-264">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="e597a-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e597a-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="e597a-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e597a-266">(28)</span><span class="sxs-lookup"><span data-stu-id="e597a-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-267">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="e597a-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e597a-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="e597a-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e597a-269">(29)</span><span class="sxs-lookup"><span data-stu-id="e597a-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-270">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e597a-270">Device is disabled.</span></span> <span data-ttu-id="e597a-271">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="e597a-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e597a-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="e597a-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e597a-273">(30)</span><span class="sxs-lookup"><span data-stu-id="e597a-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-274">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="e597a-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e597a-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e597a-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e597a-276">31</span><span class="sxs-lookup"><span data-stu-id="e597a-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-277">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="e597a-277">Device is not working properly.</span></span> <span data-ttu-id="e597a-278">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="e597a-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-279">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e597a-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-280">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e597a-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-282">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e597a-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-283">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e597a-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e597a-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e597a-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-288">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e597a-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-289">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e597a-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e597a-290">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="e597a-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e597a-291">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-292">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="e597a-292">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-293">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e597a-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-295">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Procesador DMTF \| 006,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" megahercios ")</span><span class="sxs-lookup"><span data-stu-id="e597a-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-296">Velocidad actual (en megahercios) del procesador.</span><span class="sxs-lookup"><span data-stu-id="e597a-296">Current speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-297">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="e597a-297">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-298">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-300">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="e597a-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-301">Ancho de datos del procesador, en bits.</span><span class="sxs-lookup"><span data-stu-id="e597a-301">Processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-302">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e597a-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-305">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="e597a-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-306">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e597a-306">Textual description of the object.</span></span>

<span data-ttu-id="e597a-307">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-308">**ID**</span><span class="sxs-lookup"><span data-stu-id="e597a-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-311">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e597a-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-312">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e597a-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e597a-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e597a-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-315">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e597a-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-317">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="e597a-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e597a-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e597a-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-322">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="e597a-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e597a-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-324">**Familia**</span><span class="sxs-lookup"><span data-stu-id="e597a-324">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-325">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-327">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Procesador DMTF \| 014,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ procesador CIM**.**OtherFamilyDescription**")</span><span class="sxs-lookup"><span data-stu-id="e597a-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|014.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-328">Tipo de familia de procesadores.</span><span class="sxs-lookup"><span data-stu-id="e597a-328">Processor family type.</span></span>

<span data-ttu-id="e597a-329">Esta propiedad se hereda del **\_ procesador CIM**.</span><span class="sxs-lookup"><span data-stu-id="e597a-329">This property is inherited from **CIM\_Processor**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e597a-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e597a-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="e597a-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="e597a-332"><span id="8086"></span>**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="e597a-332"><span id="8086"></span>**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="e597a-333"><span id="80286"></span>**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="e597a-333"><span id="80286"></span>**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="e597a-334"><span id="80386"></span>**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="e597a-334"><span id="80386"></span>**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="e597a-335"><span id="80486"></span>**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="e597a-335"><span id="80486"></span>**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="e597a-336"><span id="8087"></span>**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="e597a-336"><span id="8087"></span>**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="e597a-337"><span id="80287"></span>**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="e597a-337"><span id="80287"></span>**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="e597a-338"><span id="80387"></span>**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="e597a-338"><span id="80387"></span>**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="e597a-339"><span id="80487"></span>**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="e597a-339"><span id="80487"></span>**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="e597a-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Marca Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="e597a-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium(R) brand** (11)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-341">Marca de Pentium</span><span class="sxs-lookup"><span data-stu-id="e597a-341">Pentium brand</span></span>

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="e597a-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) Pro** (12)</span><span class="sxs-lookup"><span data-stu-id="e597a-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium(R) Pro** (12)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-343">Pentium Pro</span><span class="sxs-lookup"><span data-stu-id="e597a-343">Pentium Pro</span></span>

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="e597a-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="e597a-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium(R) II** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-345">Pentium II</span><span class="sxs-lookup"><span data-stu-id="e597a-345">Pentium II</span></span>

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="e597a-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Procesador Pentium (R) con tecnología MMX (TM)** (14)</span><span class="sxs-lookup"><span data-stu-id="e597a-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-347">Procesador Pentium con tecnología MMX</span><span class="sxs-lookup"><span data-stu-id="e597a-347">Pentium processor with MMX technology</span></span>

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="e597a-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="e597a-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron(TM)** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-349">Procesadores</span><span class="sxs-lookup"><span data-stu-id="e597a-349">Celeron</span></span>

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="e597a-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="e597a-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-351">Pentium II Xeon</span><span class="sxs-lookup"><span data-stu-id="e597a-351">Pentium II Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="e597a-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="e597a-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium(R) III** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-353">Pentium III</span><span class="sxs-lookup"><span data-stu-id="e597a-353">Pentium III</span></span>

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="e597a-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**Familia M1** (18)</span><span class="sxs-lookup"><span data-stu-id="e597a-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="e597a-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**Familia m2** (19)</span><span class="sxs-lookup"><span data-stu-id="e597a-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="e597a-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**Familia K5** (24)</span><span class="sxs-lookup"><span data-stu-id="e597a-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 Family** (24)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-357">Familia de procesadores AMD DURON</span><span class="sxs-lookup"><span data-stu-id="e597a-357">AMD Duron  Processor Family</span></span>

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="e597a-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**Familia K6** (25)</span><span class="sxs-lookup"><span data-stu-id="e597a-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 Family** (25)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-359">Familia K5</span><span class="sxs-lookup"><span data-stu-id="e597a-359">K5 Family</span></span>

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="e597a-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="e597a-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="e597a-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="e597a-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="e597a-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**Familia de procesadores AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="e597a-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-363">Familia de procesadores AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="e597a-363">AMD Athlon Processor Family</span></span>

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="e597a-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**Procesador AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="e597a-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-365">Procesador AMD DURON</span><span class="sxs-lookup"><span data-stu-id="e597a-365">AMD  Duron Processor</span></span>

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="e597a-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**Familia AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="e597a-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 Family** (30)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-367">Familia AMD2900</span><span class="sxs-lookup"><span data-stu-id="e597a-367">AMD2900 Family</span></span>

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="e597a-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="e597a-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="e597a-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Familia Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="e597a-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="e597a-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="e597a-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="e597a-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="e597a-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="e597a-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="e597a-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="e597a-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="e597a-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="e597a-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="e597a-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="e597a-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span><span class="sxs-lookup"><span data-stu-id="e597a-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="e597a-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="e597a-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="e597a-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Familia Alpha** (48)</span><span class="sxs-lookup"><span data-stu-id="e597a-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="e597a-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span><span class="sxs-lookup"><span data-stu-id="e597a-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="e597a-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span><span class="sxs-lookup"><span data-stu-id="e597a-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="e597a-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span><span class="sxs-lookup"><span data-stu-id="e597a-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="e597a-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span><span class="sxs-lookup"><span data-stu-id="e597a-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="e597a-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span><span class="sxs-lookup"><span data-stu-id="e597a-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="e597a-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span><span class="sxs-lookup"><span data-stu-id="e597a-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="e597a-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span><span class="sxs-lookup"><span data-stu-id="e597a-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="e597a-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**Familia MIPS** (64)</span><span class="sxs-lookup"><span data-stu-id="e597a-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="e597a-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span><span class="sxs-lookup"><span data-stu-id="e597a-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="e597a-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span><span class="sxs-lookup"><span data-stu-id="e597a-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="e597a-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span><span class="sxs-lookup"><span data-stu-id="e597a-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="e597a-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span><span class="sxs-lookup"><span data-stu-id="e597a-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="e597a-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span><span class="sxs-lookup"><span data-stu-id="e597a-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="e597a-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**Familia SPARC** (80)</span><span class="sxs-lookup"><span data-stu-id="e597a-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="e597a-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span><span class="sxs-lookup"><span data-stu-id="e597a-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="e597a-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**MICROSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="e597a-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="e597a-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**MicroSPARC IIep** (83)</span><span class="sxs-lookup"><span data-stu-id="e597a-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="e597a-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span><span class="sxs-lookup"><span data-stu-id="e597a-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="e597a-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**ULTRASPARC II** (85)</span><span class="sxs-lookup"><span data-stu-id="e597a-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="e597a-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (86)</span><span class="sxs-lookup"><span data-stu-id="e597a-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="e597a-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**ULTRASPARC III** (87)</span><span class="sxs-lookup"><span data-stu-id="e597a-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="e597a-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span><span class="sxs-lookup"><span data-stu-id="e597a-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="e597a-400"><span id="68040"></span>**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="e597a-400"><span id="68040"></span>**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="e597a-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**familia 68xxx** (97)</span><span class="sxs-lookup"><span data-stu-id="e597a-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="e597a-402"><span id="68000"></span>**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="e597a-402"><span id="68000"></span>**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="e597a-403"><span id="68010"></span>**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="e597a-403"><span id="68010"></span>**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="e597a-404"><span id="68020"></span>**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="e597a-404"><span id="68020"></span>**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="e597a-405"><span id="68030"></span>**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="e597a-405"><span id="68030"></span>**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="e597a-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Familia hobbit** (112)</span><span class="sxs-lookup"><span data-stu-id="e597a-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="e597a-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Familia Crusoe (TM) TM5000** (120)</span><span class="sxs-lookup"><span data-stu-id="e597a-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-408">Familia TM5000 de Crusoe</span><span class="sxs-lookup"><span data-stu-id="e597a-408">Crusoe TM5000 Family</span></span>

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="e597a-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Familia Crusoe (TM) TM3000** (121)</span><span class="sxs-lookup"><span data-stu-id="e597a-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-410">Familia TM3000 de Crusoe</span><span class="sxs-lookup"><span data-stu-id="e597a-410">Crusoe TM3000 Family</span></span>

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="e597a-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Familia Efficeon (TM) TM8000** (122)</span><span class="sxs-lookup"><span data-stu-id="e597a-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-412">Familia Efficeon8000</span><span class="sxs-lookup"><span data-stu-id="e597a-412">Efficeon8000 Family</span></span>

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="e597a-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span><span class="sxs-lookup"><span data-stu-id="e597a-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="e597a-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Procesador Itanium (TM)** (130)</span><span class="sxs-lookup"><span data-stu-id="e597a-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium(TM) Processor** (130)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-415">Procesador Itanium</span><span class="sxs-lookup"><span data-stu-id="e597a-415">Itanium  Processor</span></span>

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="e597a-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**Familia de procesadores AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="e597a-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-417">AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="e597a-417">AMD Athlon</span></span> 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span data-ttu-id="e597a-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**Familia AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="e597a-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD Opteron(TM) Family** (132)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-419">Familia AMD Opteron</span><span class="sxs-lookup"><span data-stu-id="e597a-419">AMD Opteron  Family</span></span>

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="e597a-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**Familia PA-RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="e597a-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="e597a-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="e597a-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="e597a-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="e597a-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="e597a-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="e597a-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="e597a-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="e597a-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="e597a-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="e597a-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="e597a-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="e597a-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="e597a-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**Familia V30** (160)</span><span class="sxs-lookup"><span data-stu-id="e597a-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="e597a-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="e597a-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-429">Pentium III Xeon</span><span class="sxs-lookup"><span data-stu-id="e597a-429">Pentium III Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="e597a-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Procesador Pentium (r) III con tecnología Intel (r) SpeedStep (** 177)</span><span class="sxs-lookup"><span data-stu-id="e597a-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-431">Procesador Pentium III con tecnología Intel SpeedStep</span><span class="sxs-lookup"><span data-stu-id="e597a-431">Pentium III Processor with Intel SpeedStep Technology</span></span>

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="e597a-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="e597a-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium(R) 4** (178)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-433">Pentium 4</span><span class="sxs-lookup"><span data-stu-id="e597a-433">Pentium 4</span></span>

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="e597a-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="e597a-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-435">Intel Xeon</span><span class="sxs-lookup"><span data-stu-id="e597a-435">Intel Xeon</span></span>

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="e597a-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**Familia AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="e597a-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="e597a-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**MP del procesador Intel (R) Xeon (TM)** (181)</span><span class="sxs-lookup"><span data-stu-id="e597a-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-438">Procesador Intel Xeon MP</span><span class="sxs-lookup"><span data-stu-id="e597a-438">Intel Xeon Processor MP</span></span>

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span data-ttu-id="e597a-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**Familia AMD AthlonXP (TM)** (182)</span><span class="sxs-lookup"><span data-stu-id="e597a-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP(TM) Family** (182)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-440">Familia AthlonXP de AMD</span><span class="sxs-lookup"><span data-stu-id="e597a-440">AMD AthlonXP Family</span></span>

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span data-ttu-id="e597a-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**Familia AMD AthlonMP (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="e597a-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP(TM) Family** (183)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-442">Familia AthlonMP de AMD</span><span class="sxs-lookup"><span data-stu-id="e597a-442">AMD AthlonMP Family</span></span>

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="e597a-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="e597a-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-444">Intel Itanium 2</span><span class="sxs-lookup"><span data-stu-id="e597a-444">Intel Itanium 2</span></span>

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span data-ttu-id="e597a-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Procesador Intel Pentium M** (185)</span><span class="sxs-lookup"><span data-stu-id="e597a-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M Processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="e597a-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="e597a-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span data-ttu-id="e597a-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**Familia IBM390** (200)</span><span class="sxs-lookup"><span data-stu-id="e597a-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span data-ttu-id="e597a-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span><span class="sxs-lookup"><span data-stu-id="e597a-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span data-ttu-id="e597a-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span><span class="sxs-lookup"><span data-stu-id="e597a-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span data-ttu-id="e597a-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span><span class="sxs-lookup"><span data-stu-id="e597a-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span data-ttu-id="e597a-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/arquitectura base** (204)</span><span class="sxs-lookup"><span data-stu-id="e597a-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/Architecture base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="e597a-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="e597a-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="e597a-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span><span class="sxs-lookup"><span data-stu-id="e597a-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="e597a-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span><span class="sxs-lookup"><span data-stu-id="e597a-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="e597a-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="e597a-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="e597a-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="e597a-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="e597a-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span><span class="sxs-lookup"><span data-stu-id="e597a-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="e597a-458"><span id="6x86"></span><span id="6X86"></span>**6 x86** (300)</span><span class="sxs-lookup"><span data-stu-id="e597a-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="e597a-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span><span class="sxs-lookup"><span data-stu-id="e597a-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="e597a-460"><span id="MII"></span><span id="mii"></span>**Mii** (302)</span><span class="sxs-lookup"><span data-stu-id="e597a-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="e597a-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span><span class="sxs-lookup"><span data-stu-id="e597a-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="e597a-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="e597a-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="e597a-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Procesador de vídeo** (500)</span><span class="sxs-lookup"><span data-stu-id="e597a-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Video Processor** (500)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-464">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e597a-464">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-465">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e597a-465">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-467">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="e597a-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-468">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="e597a-468">Date and time the object was installed.</span></span> <span data-ttu-id="e597a-469">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e597a-469">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e597a-470">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-470">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-471">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e597a-471">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-472">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e597a-472">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-473">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-473">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-474">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e597a-474">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e597a-475">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-476">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="e597a-476">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-477">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-478">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-479">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrProcessorLoad "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Percent ")</span><span class="sxs-lookup"><span data-stu-id="e597a-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-480">Carga del procesador, promediada en el último minuto, en un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="e597a-480">Loading of the processor, averaged over the last minute, in a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-481">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="e597a-481">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-482">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e597a-482">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-484">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Procesador DMTF \| 006,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" megahercios ")</span><span class="sxs-lookup"><span data-stu-id="e597a-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-485">Velocidad máxima (en megahercios) del procesador.</span><span class="sxs-lookup"><span data-stu-id="e597a-485">Maximum speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-486">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e597a-486">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-489">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e597a-489">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-490">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="e597a-490">Label by which the object is known.</span></span> <span data-ttu-id="e597a-491">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="e597a-491">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e597a-492">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-492">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-493">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="e597a-493">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-494">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-496">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ procesador CIM**.**Family**")</span><span class="sxs-lookup"><span data-stu-id="e597a-496">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-497">Descripción del tipo de familia de procesadores.</span><span class="sxs-lookup"><span data-stu-id="e597a-497">Description of the processor family type.</span></span> <span data-ttu-id="e597a-498">Esta propiedad se usa cuando la propiedad **Family** está establecida en 1 ("Other").</span><span class="sxs-lookup"><span data-stu-id="e597a-498">This property is used when the **Family** property is set to 1 ("Other").</span></span> <span data-ttu-id="e597a-499">Esta cadena debe establecerse en NULL cuando la propiedad **Family** es un valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="e597a-499">This string should be set to null when the **Family** property is a value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e597a-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-501">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-502">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-503">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e597a-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-504">Plug and Play identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e597a-504">Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e597a-505">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e597a-506">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e597a-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e597a-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e597a-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-508">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e597a-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-510">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e597a-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e597a-511">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="e597a-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e597a-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e597a-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="e597a-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e597a-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e597a-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e597a-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e597a-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-516">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e597a-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e597a-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="e597a-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-518">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="e597a-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e597a-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="e597a-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-520">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="e597a-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e597a-521">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="e597a-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e597a-522">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e597a-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e597a-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="e597a-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-524">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="e597a-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e597a-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="e597a-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-526">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="e597a-526">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-527">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e597a-527">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-528">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e597a-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-529">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-530">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="e597a-530">If **True**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e597a-531">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="e597a-531">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e597a-532">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="e597a-532">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e597a-533">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="e597a-533">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e597a-534">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-534">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-535">**Rol**</span><span class="sxs-lookup"><span data-stu-id="e597a-535">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-536">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-536">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-538">Cadena de forma libre que describe el rol del procesador.</span><span class="sxs-lookup"><span data-stu-id="e597a-538">Free-form string that describes the role of the processor.</span></span> <span data-ttu-id="e597a-539">Por ejemplo, "procesador central" o "procesador matemático".</span><span class="sxs-lookup"><span data-stu-id="e597a-539">For example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="e597a-540">**Estado**</span><span class="sxs-lookup"><span data-stu-id="e597a-540">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-541">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-543">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e597a-543">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-544">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="e597a-544">Current status of the object.</span></span>

<span data-ttu-id="e597a-545">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-545">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e597a-546">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e597a-546">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e597a-547">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="e597a-547">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e597a-548">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="e597a-548">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e597a-549">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e597a-549">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-550">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="e597a-550">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e597a-551">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="e597a-551">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e597a-552">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="e597a-552">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e597a-553">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="e597a-553">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e597a-554">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="e597a-554">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e597a-555">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="e597a-555">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e597a-556">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e597a-556">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e597a-557">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="e597a-557">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e597a-558">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="e597a-558">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-559">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e597a-559">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-560">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-560">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-561">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-562">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e597a-562">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-563">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e597a-563">State of the logical device.</span></span> <span data-ttu-id="e597a-564">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="e597a-564">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e597a-565">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-565">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e597a-566">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e597a-566">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-567">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="e597a-567">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e597a-568">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e597a-568">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e597a-569">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="e597a-569">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e597a-570">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="e597a-570">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-571">**Recorrido paso a paso**</span><span class="sxs-lookup"><span data-stu-id="e597a-571">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-572">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-572">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-573">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-573">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-574">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ procesador CIM**.**Family**")</span><span class="sxs-lookup"><span data-stu-id="e597a-574">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-575">Cadena de forma libre que indica el nivel de revisión del procesador dentro de la familia del procesador.</span><span class="sxs-lookup"><span data-stu-id="e597a-575">Free-form string that indicates the revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-576">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e597a-576">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-577">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-578">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-579">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e597a-579">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-580">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e597a-580">Scoping system's creation class name.</span></span>

<span data-ttu-id="e597a-581">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-581">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-582">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e597a-582">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-583">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-584">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-585">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e597a-585">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-586">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e597a-586">Scoping system's name.</span></span>

<span data-ttu-id="e597a-587">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-588">**UniqueId**</span><span class="sxs-lookup"><span data-stu-id="e597a-588">**UniqueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e597a-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-590">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-590">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-591">Identificador único global para el procesador.</span><span class="sxs-lookup"><span data-stu-id="e597a-591">Globally unique identifier for the processor.</span></span> <span data-ttu-id="e597a-592">Este identificador solo puede ser único dentro de una familia de procesadores.</span><span class="sxs-lookup"><span data-stu-id="e597a-592">This identifier can only be unique within a processor family.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-593">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="e597a-593">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-594">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e597a-594">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-595">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e597a-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-596">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Procesador DMTF \| 006,7 ")</span><span class="sxs-lookup"><span data-stu-id="e597a-596">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.7")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-597">Información del socket de la CPU, que incluye datos sobre cómo actualizar el procesador (si se admiten las actualizaciones).</span><span class="sxs-lookup"><span data-stu-id="e597a-597">CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e597a-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e597a-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="e597a-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="e597a-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Placa secundaria** (3)</span><span class="sxs-lookup"><span data-stu-id="e597a-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="e597a-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**Socket ZIF** (4)</span><span class="sxs-lookup"><span data-stu-id="e597a-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="e597a-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Reemplazo o reversión** (5)</span><span class="sxs-lookup"><span data-stu-id="e597a-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Replacement/Piggy Back** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-603">Sustitución o reversión</span><span class="sxs-lookup"><span data-stu-id="e597a-603">Replacement or piggy back</span></span>

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e597a-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (6)</span><span class="sxs-lookup"><span data-stu-id="e597a-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="e597a-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**Socket LIF** (7)</span><span class="sxs-lookup"><span data-stu-id="e597a-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="e597a-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Ranura 1** (8)</span><span class="sxs-lookup"><span data-stu-id="e597a-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="e597a-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Ranura 2** (9)</span><span class="sxs-lookup"><span data-stu-id="e597a-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="e597a-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**socket de Pin 370** (10)</span><span class="sxs-lookup"><span data-stu-id="e597a-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="e597a-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Ranura A** (11)</span><span class="sxs-lookup"><span data-stu-id="e597a-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="e597a-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Ranura M** (12)</span><span class="sxs-lookup"><span data-stu-id="e597a-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="e597a-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span><span class="sxs-lookup"><span data-stu-id="e597a-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="e597a-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (socket 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="e597a-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="e597a-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span><span class="sxs-lookup"><span data-stu-id="e597a-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="e597a-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span><span class="sxs-lookup"><span data-stu-id="e597a-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="e597a-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span><span class="sxs-lookup"><span data-stu-id="e597a-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="e597a-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span><span class="sxs-lookup"><span data-stu-id="e597a-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span></span>


<span data-ttu-id="e597a-617"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e597a-617"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e597a-618">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e597a-618">Remarks</span></span>

<span data-ttu-id="e597a-619">La clase de **\_ procesador de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-619">The **CIM\_Processor** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e597a-620">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e597a-620">WMI does not implement this class.</span></span> <span data-ttu-id="e597a-621">Para las clases WMI derivadas del **\_ procesador CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e597a-621">For WMI classes derived from **CIM\_Processor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e597a-622">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e597a-622">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e597a-623">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e597a-623">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e597a-624">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e597a-624">Requirements</span></span>



| <span data-ttu-id="e597a-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="e597a-625">Requirement</span></span> | <span data-ttu-id="e597a-626">Value</span><span class="sxs-lookup"><span data-stu-id="e597a-626">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e597a-627">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e597a-627">Minimum supported client</span></span><br/> | <span data-ttu-id="e597a-628">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e597a-628">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e597a-629">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e597a-629">Minimum supported server</span></span><br/> | <span data-ttu-id="e597a-630">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e597a-630">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e597a-631">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e597a-631">Namespace</span></span><br/>                | <span data-ttu-id="e597a-632">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e597a-632">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e597a-633">MOF</span><span class="sxs-lookup"><span data-stu-id="e597a-633">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e597a-634"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e597a-634"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e597a-635">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e597a-635">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e597a-636"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e597a-636"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e597a-637">Vea también</span><span class="sxs-lookup"><span data-stu-id="e597a-637">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e597a-638">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e597a-638">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

