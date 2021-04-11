---
description: La \_ clase CIM DesktopMonitor representa las capacidades y la administración del dispositivo lógico monitor de escritorio (CRT).
ms.assetid: dc65aa38-5255-4a40-8ffc-f05f9af71dc6
ms.tgt_platform: multiple
title: CIM_DesktopMonitor (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.Caption
- CIM_DesktopMonitor.Description
- CIM_DesktopMonitor.InstallDate
- CIM_DesktopMonitor.Name
- CIM_DesktopMonitor.Status
- CIM_DesktopMonitor.Availability
- CIM_DesktopMonitor.ConfigManagerErrorCode
- CIM_DesktopMonitor.ConfigManagerUserConfig
- CIM_DesktopMonitor.CreationClassName
- CIM_DesktopMonitor.DeviceID
- CIM_DesktopMonitor.PowerManagementCapabilities
- CIM_DesktopMonitor.ErrorCleared
- CIM_DesktopMonitor.ErrorDescription
- CIM_DesktopMonitor.LastErrorCode
- CIM_DesktopMonitor.PNPDeviceID
- CIM_DesktopMonitor.PowerManagementSupported
- CIM_DesktopMonitor.StatusInfo
- CIM_DesktopMonitor.SystemCreationClassName
- CIM_DesktopMonitor.SystemName
- CIM_DesktopMonitor.IsLocked
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b22d0b681491bbddf0ee357b394da5f1a77aa0e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275001"
---
# <a name="cim_desktopmonitor-class-cimwin32-wmi-providers"></a><span data-ttu-id="600ae-103">CIM_DesktopMonitor (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="600ae-103">CIM_DesktopMonitor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="600ae-104">La clase **CIM \_ DesktopMonitor** representa las capacidades y la administración del dispositivo lógico monitor de escritorio (CRT).</span><span class="sxs-lookup"><span data-stu-id="600ae-104">The **CIM\_DesktopMonitor** class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="600ae-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="600ae-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="600ae-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="600ae-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="600ae-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="600ae-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="600ae-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="600ae-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="600ae-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="600ae-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE8-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_DesktopMonitor : CIM_Display
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  IsLocked;
  uint32   Bandwidth;
  uint16   DisplayType;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="600ae-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="600ae-110">Members</span></span>

<span data-ttu-id="600ae-111">La clase **CIM \_ DesktopMonitor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="600ae-111">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="600ae-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="600ae-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="600ae-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="600ae-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="600ae-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="600ae-114">Methods</span></span>

<span data-ttu-id="600ae-115">La clase **CIM \_ DesktopMonitor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="600ae-115">The **CIM\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="600ae-116">Método</span><span class="sxs-lookup"><span data-stu-id="600ae-116">Method</span></span>                                                                    | <span data-ttu-id="600ae-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="600ae-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="600ae-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="600ae-118">**Reset**</span></span>](reset-method-in-class-cim-desktopmonitor.md)                 | <span data-ttu-id="600ae-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="600ae-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="600ae-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="600ae-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="600ae-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="600ae-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-desktopmonitor.md) | <span data-ttu-id="600ae-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="600ae-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="600ae-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="600ae-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="600ae-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="600ae-124">Properties</span></span>

<span data-ttu-id="600ae-125">La clase **CIM \_ DesktopMonitor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="600ae-125">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="600ae-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="600ae-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="600ae-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="600ae-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="600ae-130">Availability and status of the device.</span></span>

<span data-ttu-id="600ae-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="600ae-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="600ae-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="600ae-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="600ae-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="600ae-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="600ae-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="600ae-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="600ae-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="600ae-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="600ae-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="600ae-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="600ae-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="600ae-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="600ae-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="600ae-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="600ae-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="600ae-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="600ae-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="600ae-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="600ae-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="600ae-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="600ae-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="600ae-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="600ae-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="600ae-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="600ae-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="600ae-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="600ae-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="600ae-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="600ae-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="600ae-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="600ae-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-149">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="600ae-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="600ae-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="600ae-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="600ae-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="600ae-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="600ae-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="600ae-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="600ae-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="600ae-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="600ae-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="600ae-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="600ae-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="600ae-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="600ae-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="600ae-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="600ae-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="600ae-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="600ae-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="600ae-161">**Ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="600ae-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="600ae-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-164">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios")</span><span class="sxs-lookup"><span data-stu-id="600ae-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-165">Ancho de banda del monitor en MHz.</span><span class="sxs-lookup"><span data-stu-id="600ae-165">Monitor's bandwidth in MHz.</span></span> <span data-ttu-id="600ae-166">Si es desconocido, use 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="600ae-166">If unknown, use 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="600ae-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="600ae-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-171">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="600ae-171">A short textual description of the object.</span></span>

<span data-ttu-id="600ae-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="600ae-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="600ae-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-176">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="600ae-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-177">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="600ae-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="600ae-178">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="600ae-179">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="600ae-179">**This device is working properly.**</span></span> <span data-ttu-id="600ae-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="600ae-180">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="600ae-181">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="600ae-181">**This device is not configured correctly.**</span></span> <span data-ttu-id="600ae-182">(1)</span><span class="sxs-lookup"><span data-stu-id="600ae-182">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="600ae-183">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-183">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="600ae-184">(2)</span><span class="sxs-lookup"><span data-stu-id="600ae-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="600ae-185">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="600ae-185">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="600ae-186">(3)</span><span class="sxs-lookup"><span data-stu-id="600ae-186">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="600ae-187">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="600ae-187">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="600ae-188">(4)</span><span class="sxs-lookup"><span data-stu-id="600ae-188">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="600ae-189">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="600ae-189">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="600ae-190">(5)</span><span class="sxs-lookup"><span data-stu-id="600ae-190">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="600ae-191">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="600ae-191">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="600ae-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="600ae-192">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="600ae-193">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="600ae-193">**Cannot filter.**</span></span> <span data-ttu-id="600ae-194">(7)</span><span class="sxs-lookup"><span data-stu-id="600ae-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="600ae-195">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-195">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="600ae-196">(8)</span><span class="sxs-lookup"><span data-stu-id="600ae-196">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="600ae-197">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="600ae-197">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="600ae-198">(9)</span><span class="sxs-lookup"><span data-stu-id="600ae-198">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="600ae-199">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="600ae-199">**This device cannot start.**</span></span> <span data-ttu-id="600ae-200">(10)</span><span class="sxs-lookup"><span data-stu-id="600ae-200">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="600ae-201">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-201">**This device failed.**</span></span> <span data-ttu-id="600ae-202">(11)</span><span class="sxs-lookup"><span data-stu-id="600ae-202">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="600ae-203">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="600ae-203">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="600ae-204">(12)</span><span class="sxs-lookup"><span data-stu-id="600ae-204">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="600ae-205">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-205">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="600ae-206">(13)</span><span class="sxs-lookup"><span data-stu-id="600ae-206">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="600ae-207">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-207">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="600ae-208">(14)</span><span class="sxs-lookup"><span data-stu-id="600ae-208">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="600ae-209">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="600ae-209">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="600ae-210">(15)</span><span class="sxs-lookup"><span data-stu-id="600ae-210">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="600ae-211">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-211">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="600ae-212">(16)</span><span class="sxs-lookup"><span data-stu-id="600ae-212">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="600ae-213">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="600ae-213">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="600ae-214">(17)</span><span class="sxs-lookup"><span data-stu-id="600ae-214">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="600ae-215">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-215">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="600ae-216">(18)</span><span class="sxs-lookup"><span data-stu-id="600ae-216">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="600ae-217">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="600ae-217">**Failure using the VxD loader.**</span></span> <span data-ttu-id="600ae-218">(19)</span><span class="sxs-lookup"><span data-stu-id="600ae-218">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="600ae-219">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="600ae-219">**Your registry might be corrupted.**</span></span> <span data-ttu-id="600ae-220">(20)</span><span class="sxs-lookup"><span data-stu-id="600ae-220">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="600ae-221">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-221">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="600ae-222">(21)</span><span class="sxs-lookup"><span data-stu-id="600ae-222">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="600ae-223">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="600ae-223">**This device is disabled.**</span></span> <span data-ttu-id="600ae-224">(22)</span><span class="sxs-lookup"><span data-stu-id="600ae-224">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="600ae-225">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="600ae-225">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="600ae-226">(23)</span><span class="sxs-lookup"><span data-stu-id="600ae-226">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="600ae-227">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="600ae-227">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="600ae-228">(24)</span><span class="sxs-lookup"><span data-stu-id="600ae-228">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="600ae-229">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="600ae-230">(25)</span><span class="sxs-lookup"><span data-stu-id="600ae-230">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="600ae-231">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-231">**Windows is still setting up this device.**</span></span> <span data-ttu-id="600ae-232">(26)</span><span class="sxs-lookup"><span data-stu-id="600ae-232">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="600ae-233">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="600ae-233">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="600ae-234">(27)</span><span class="sxs-lookup"><span data-stu-id="600ae-234">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="600ae-235">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="600ae-235">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="600ae-236">(28)</span><span class="sxs-lookup"><span data-stu-id="600ae-236">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="600ae-237">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="600ae-237">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="600ae-238">(29)</span><span class="sxs-lookup"><span data-stu-id="600ae-238">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="600ae-239">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="600ae-239">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="600ae-240">(30)</span><span class="sxs-lookup"><span data-stu-id="600ae-240">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="600ae-241">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="600ae-241">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="600ae-242">31</span><span class="sxs-lookup"><span data-stu-id="600ae-242">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="600ae-243">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="600ae-243">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-244">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="600ae-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-246">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="600ae-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-247">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="600ae-247">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="600ae-248">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-248">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-249">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="600ae-249">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-252">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="600ae-252">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="600ae-253">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="600ae-253">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="600ae-254">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="600ae-254">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="600ae-255">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-255">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-256">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="600ae-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-259">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="600ae-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-260">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="600ae-260">A textual description of the object.</span></span>

<span data-ttu-id="600ae-261">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-262">**ID**</span><span class="sxs-lookup"><span data-stu-id="600ae-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-265">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="600ae-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="600ae-266">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="600ae-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="600ae-267">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-268">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="600ae-268">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-269">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="600ae-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-271">Tipo de monitor de escritorio o CRT.</span><span class="sxs-lookup"><span data-stu-id="600ae-271">Type of desktop monitor or CRT.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="600ae-272">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="600ae-272">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="600ae-273">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="600ae-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="600ae-274">**Color de Multiscan** (2)</span><span class="sxs-lookup"><span data-stu-id="600ae-274">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="600ae-275">**Monocromo Multiscan** (3)</span><span class="sxs-lookup"><span data-stu-id="600ae-275">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="600ae-276">**Color de frecuencia fijo** (4)</span><span class="sxs-lookup"><span data-stu-id="600ae-276">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="600ae-277">**Monocromática de frecuencia fija** (5)</span><span class="sxs-lookup"><span data-stu-id="600ae-277">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="600ae-278">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="600ae-278">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-279">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="600ae-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-281">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="600ae-281">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="600ae-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-283">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="600ae-283">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-286">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="600ae-286">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="600ae-287">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-288">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="600ae-288">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-289">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="600ae-289">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-291">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="600ae-291">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-292">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="600ae-292">Indicates when the object was installed.</span></span> <span data-ttu-id="600ae-293">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="600ae-293">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="600ae-294">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-295">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="600ae-295">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-296">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="600ae-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-298">Si es **true**, el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="600ae-298">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="600ae-299">Esta propiedad se hereda de [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-299">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-300">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="600ae-300">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-301">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="600ae-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-303">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="600ae-303">Last error code reported by the logical device.</span></span>

<span data-ttu-id="600ae-304">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-305">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="600ae-305">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-308">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="600ae-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-309">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="600ae-309">Label by which the object is known.</span></span> <span data-ttu-id="600ae-310">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="600ae-310">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="600ae-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-312">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="600ae-312">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-315">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="600ae-315">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-316">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="600ae-316">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="600ae-317">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="600ae-317">Example: "\*PNP030b"</span></span>

<span data-ttu-id="600ae-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-319">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="600ae-319">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-320">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="600ae-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="600ae-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-322">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="600ae-322">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="600ae-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="600ae-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="600ae-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-325">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="600ae-325">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="600ae-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="600ae-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-327">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="600ae-327">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="600ae-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="600ae-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-329">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="600ae-329">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="600ae-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="600ae-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-331">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="600ae-331">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="600ae-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="600ae-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-333">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="600ae-333">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="600ae-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="600ae-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-335">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="600ae-335">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="600ae-336">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="600ae-336">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="600ae-337">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="600ae-337">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="600ae-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="600ae-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-339">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="600ae-339">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="600ae-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="600ae-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="600ae-341">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="600ae-341">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="600ae-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="600ae-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-343">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="600ae-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-345">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="600ae-345">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="600ae-346">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="600ae-346">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="600ae-347">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="600ae-347">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="600ae-348">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="600ae-348">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="600ae-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-350">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="600ae-350">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-351">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="600ae-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-353">Alto lógico de la pantalla, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="600ae-353">Logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="600ae-354">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="600ae-354">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-355">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="600ae-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="600ae-357">Ancho lógico de la pantalla, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="600ae-357">Logical width of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="600ae-358">**Estado**</span><span class="sxs-lookup"><span data-stu-id="600ae-358">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-359">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-361">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="600ae-361">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-362">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="600ae-362">String that indicates the current status of the object.</span></span> <span data-ttu-id="600ae-363">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="600ae-363">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="600ae-364">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="600ae-364">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="600ae-365">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="600ae-365">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="600ae-366">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="600ae-366">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="600ae-367">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="600ae-367">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="600ae-368">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="600ae-368">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="600ae-369">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="600ae-370">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="600ae-370">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="600ae-371">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="600ae-371">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="600ae-372">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="600ae-372">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="600ae-373">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="600ae-373">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="600ae-374">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="600ae-374">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="600ae-375">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="600ae-375">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="600ae-376">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="600ae-376">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="600ae-377">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="600ae-377">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="600ae-378">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="600ae-378">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="600ae-379">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="600ae-379">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="600ae-380">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="600ae-380">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="600ae-381">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="600ae-381">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="600ae-382">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="600ae-382">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="600ae-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="600ae-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-384">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="600ae-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-386">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="600ae-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="600ae-387">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="600ae-387">State of the logical device.</span></span> <span data-ttu-id="600ae-388">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="600ae-388">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="600ae-389">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="600ae-390">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="600ae-390">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="600ae-391">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="600ae-391">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="600ae-392">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="600ae-392">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="600ae-393">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="600ae-393">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="600ae-394">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="600ae-394">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="600ae-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="600ae-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-396">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-398">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="600ae-398">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="600ae-399">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="600ae-399">The scoping system's creation class name.</span></span>

<span data-ttu-id="600ae-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="600ae-401">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="600ae-401">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="600ae-402">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="600ae-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="600ae-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="600ae-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="600ae-404">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="600ae-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="600ae-405">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="600ae-405">The scoping system's name.</span></span>

<span data-ttu-id="600ae-406">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="600ae-407">Observaciones</span><span class="sxs-lookup"><span data-stu-id="600ae-407">Remarks</span></span>

<span data-ttu-id="600ae-408">La clase **CIM \_ DesktopMonitor** se deriva de la [**\_ presentación de CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-408">The **CIM\_DesktopMonitor** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="600ae-409">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="600ae-409">WMI does not implement this class.</span></span> <span data-ttu-id="600ae-410">Para obtener más información sobre las clases derivadas de **CIM \_ DesktopMonitor**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="600ae-410">For more information about classes derived from **CIM\_DesktopMonitor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="600ae-411">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="600ae-411">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="600ae-412">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="600ae-412">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="600ae-413">Requisitos</span><span class="sxs-lookup"><span data-stu-id="600ae-413">Requirements</span></span>



| <span data-ttu-id="600ae-414">Requisito</span><span class="sxs-lookup"><span data-stu-id="600ae-414">Requirement</span></span> | <span data-ttu-id="600ae-415">Value</span><span class="sxs-lookup"><span data-stu-id="600ae-415">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="600ae-416">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="600ae-416">Minimum supported client</span></span><br/> | <span data-ttu-id="600ae-417">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="600ae-417">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="600ae-418">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="600ae-418">Minimum supported server</span></span><br/> | <span data-ttu-id="600ae-419">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="600ae-419">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="600ae-420">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="600ae-420">Namespace</span></span><br/>                | <span data-ttu-id="600ae-421">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="600ae-421">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="600ae-422">MOF</span><span class="sxs-lookup"><span data-stu-id="600ae-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="600ae-423"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="600ae-423"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="600ae-424">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="600ae-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="600ae-425"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="600ae-425"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600ae-426">Vea también</span><span class="sxs-lookup"><span data-stu-id="600ae-426">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600ae-427">**Presentación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="600ae-427">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

