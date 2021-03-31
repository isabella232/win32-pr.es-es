---
description: El \_ PCVIDEOCONTROLLER CIM representa las capacidades y la administración de un controlador de vídeo de equipo personal, un subtipo de controlador de vídeo.
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: CIM_PCVideoController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423383"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="48602-103">\_Clase PCVideoController de CIM</span><span class="sxs-lookup"><span data-stu-id="48602-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="48602-104">El **\_ PCVideoController CIM** representa las capacidades y la administración de un controlador de vídeo de equipo personal, un subtipo de controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48602-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48602-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="48602-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48602-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="48602-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48602-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="48602-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="48602-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="48602-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48602-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48602-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="48602-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="48602-110">Members</span></span>

<span data-ttu-id="48602-111">La clase **CIM \_ PCVideoController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48602-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="48602-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="48602-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="48602-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48602-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48602-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="48602-114">Methods</span></span>

<span data-ttu-id="48602-115">La clase **CIM \_ PCVideoController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="48602-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="48602-116">Método</span><span class="sxs-lookup"><span data-stu-id="48602-116">Method</span></span>                                                                       | <span data-ttu-id="48602-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="48602-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48602-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="48602-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="48602-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="48602-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="48602-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="48602-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="48602-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="48602-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="48602-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="48602-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="48602-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="48602-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48602-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48602-124">Properties</span></span>

<span data-ttu-id="48602-125">La clase **CIM \_ PCVideoController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="48602-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48602-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="48602-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-127">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48602-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-129">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="48602-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="48602-130">Gráficos y capacidades 3D del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48602-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="48602-131">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="48602-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="48602-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="48602-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48602-136">acelerador 3D</span><span class="sxs-lookup"><span data-stu-id="48602-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-137">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="48602-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-138">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="48602-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="48602-141">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-141">Availability and status of the device.</span></span>

<span data-ttu-id="48602-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="48602-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48602-146">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="48602-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="48602-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="48602-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="48602-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="48602-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="48602-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="48602-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="48602-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="48602-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="48602-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="48602-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="48602-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="48602-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="48602-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="48602-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="48602-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="48602-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="48602-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="48602-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="48602-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="48602-157">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="48602-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="48602-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="48602-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="48602-159">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="48602-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="48602-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="48602-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="48602-161">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="48602-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="48602-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="48602-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="48602-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="48602-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="48602-164">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="48602-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="48602-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="48602-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="48602-166">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="48602-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="48602-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="48602-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="48602-168">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="48602-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="48602-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="48602-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="48602-170">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="48602-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="48602-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="48602-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="48602-172">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="48602-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-173">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="48602-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-174">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="48602-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48602-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-176">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**controlador de \_ videojuego CIM**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="48602-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="48602-177">Cadenas de forma libre que proporcionan explicaciones detalladas para las características de acelerador de vídeo indicadas en la matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="48602-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="48602-178">Cada entrada de la matriz está relacionada con la entrada de la matriz **AcceleratorCapabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="48602-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="48602-179">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-180">**Caption**</span><span class="sxs-lookup"><span data-stu-id="48602-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-183">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="48602-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="48602-184">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="48602-184">Short textual description of the object.</span></span>

<span data-ttu-id="48602-185">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48602-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="48602-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-189">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="48602-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="48602-190">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="48602-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="48602-191">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="48602-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="48602-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="48602-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="48602-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="48602-194">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="48602-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="48602-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="48602-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="48602-196">(1)</span><span class="sxs-lookup"><span data-stu-id="48602-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="48602-197">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="48602-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="48602-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="48602-199">(2)</span><span class="sxs-lookup"><span data-stu-id="48602-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="48602-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="48602-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="48602-201">(3)</span><span class="sxs-lookup"><span data-stu-id="48602-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="48602-202">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="48602-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="48602-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="48602-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="48602-204">(4)</span><span class="sxs-lookup"><span data-stu-id="48602-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="48602-205">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="48602-205">Device is not working properly.</span></span> <span data-ttu-id="48602-206">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="48602-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="48602-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="48602-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="48602-208">(5)</span><span class="sxs-lookup"><span data-stu-id="48602-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="48602-209">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="48602-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="48602-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="48602-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="48602-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="48602-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="48602-212">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="48602-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="48602-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="48602-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="48602-214">(7)</span><span class="sxs-lookup"><span data-stu-id="48602-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="48602-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="48602-216">(8)</span><span class="sxs-lookup"><span data-stu-id="48602-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="48602-217">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="48602-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="48602-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="48602-219">(9)</span><span class="sxs-lookup"><span data-stu-id="48602-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="48602-220">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="48602-220">Device is not working properly.</span></span> <span data-ttu-id="48602-221">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="48602-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="48602-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="48602-223">(10)</span><span class="sxs-lookup"><span data-stu-id="48602-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="48602-224">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="48602-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="48602-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="48602-226">(11)</span><span class="sxs-lookup"><span data-stu-id="48602-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="48602-227">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="48602-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="48602-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="48602-229">(12)</span><span class="sxs-lookup"><span data-stu-id="48602-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="48602-230">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="48602-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="48602-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="48602-232">(13)</span><span class="sxs-lookup"><span data-stu-id="48602-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="48602-233">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="48602-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="48602-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="48602-235">(14)</span><span class="sxs-lookup"><span data-stu-id="48602-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="48602-236">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="48602-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="48602-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="48602-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="48602-238">(15)</span><span class="sxs-lookup"><span data-stu-id="48602-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="48602-239">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="48602-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="48602-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="48602-241">(16)</span><span class="sxs-lookup"><span data-stu-id="48602-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="48602-242">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="48602-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="48602-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="48602-244">(17)</span><span class="sxs-lookup"><span data-stu-id="48602-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="48602-245">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="48602-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="48602-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="48602-247">(18)</span><span class="sxs-lookup"><span data-stu-id="48602-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="48602-248">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="48602-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="48602-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="48602-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="48602-250">(19)</span><span class="sxs-lookup"><span data-stu-id="48602-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="48602-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="48602-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="48602-252">(20)</span><span class="sxs-lookup"><span data-stu-id="48602-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="48602-253">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="48602-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="48602-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="48602-255">(21)</span><span class="sxs-lookup"><span data-stu-id="48602-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="48602-256">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="48602-256">System failure.</span></span> <span data-ttu-id="48602-257">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="48602-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="48602-258">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="48602-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="48602-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="48602-260">(22)</span><span class="sxs-lookup"><span data-stu-id="48602-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="48602-261">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="48602-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="48602-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="48602-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="48602-263">(23)</span><span class="sxs-lookup"><span data-stu-id="48602-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="48602-264">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="48602-264">System failure.</span></span> <span data-ttu-id="48602-265">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="48602-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="48602-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="48602-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="48602-267">(24)</span><span class="sxs-lookup"><span data-stu-id="48602-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="48602-268">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="48602-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="48602-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="48602-270">(25)</span><span class="sxs-lookup"><span data-stu-id="48602-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="48602-271">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="48602-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="48602-273">(26)</span><span class="sxs-lookup"><span data-stu-id="48602-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="48602-274">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48602-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="48602-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="48602-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="48602-276">(27)</span><span class="sxs-lookup"><span data-stu-id="48602-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="48602-277">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="48602-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="48602-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="48602-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="48602-279">(28)</span><span class="sxs-lookup"><span data-stu-id="48602-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="48602-280">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="48602-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="48602-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="48602-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="48602-282">(29)</span><span class="sxs-lookup"><span data-stu-id="48602-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="48602-283">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="48602-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="48602-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="48602-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="48602-285">(30)</span><span class="sxs-lookup"><span data-stu-id="48602-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="48602-286">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="48602-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="48602-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="48602-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="48602-288">31</span><span class="sxs-lookup"><span data-stu-id="48602-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="48602-289">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="48602-289">Device is not working properly.</span></span> <span data-ttu-id="48602-290">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="48602-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="48602-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-292">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48602-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48602-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-294">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="48602-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="48602-295">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="48602-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="48602-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="48602-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-300">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48602-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48602-301">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="48602-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="48602-302">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="48602-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="48602-303">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-304">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="48602-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-305">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-307">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="48602-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="48602-308">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="48602-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="48602-309">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-310">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="48602-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-311">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-313">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="48602-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="48602-314">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="48602-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="48602-315">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-316">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="48602-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-317">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48602-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48602-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-319">Número de colores admitidos en las resoluciones actuales.</span><span class="sxs-lookup"><span data-stu-id="48602-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="48602-320">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="48602-321">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="48602-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="48602-322">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="48602-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-323">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-325">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="48602-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="48602-326">Si está en modo de carácter, número de columnas para el controlador de vídeo; en caso contrario, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="48602-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="48602-327">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-328">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="48602-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-329">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-331">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="48602-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="48602-332">Si está en modo de carácter, número de filas para este controlador de vídeo; en caso contrario, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="48602-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="48602-333">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-334">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="48602-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="48602-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="48602-338">Frecuencia de actualización actual en hercios.</span><span class="sxs-lookup"><span data-stu-id="48602-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="48602-339">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-340">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="48602-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-341">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-343">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="48602-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="48602-344">Modo de exploración actual.</span><span class="sxs-lookup"><span data-stu-id="48602-344">Current scan mode.</span></span> <span data-ttu-id="48602-345">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="48602-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelazado** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="48602-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**No entrelazado** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="48602-350">No entrelazado</span><span class="sxs-lookup"><span data-stu-id="48602-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-351">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="48602-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-352">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-354">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="48602-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="48602-355">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="48602-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="48602-356">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-357">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48602-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-360">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="48602-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="48602-361">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="48602-361">Textual description of the object.</span></span>

<span data-ttu-id="48602-362">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48602-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-363">**ID**</span><span class="sxs-lookup"><span data-stu-id="48602-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-366">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48602-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48602-367">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="48602-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="48602-368">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-369">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="48602-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-370">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48602-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48602-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-372">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="48602-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="48602-373">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="48602-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-375">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-377">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="48602-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="48602-378">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="48602-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-380">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48602-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48602-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-382">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="48602-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="48602-383">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="48602-383">Date and time the object was installed.</span></span> <span data-ttu-id="48602-384">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="48602-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="48602-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48602-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-386">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="48602-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-387">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-389">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="48602-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="48602-390">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-391">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="48602-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-392">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-394">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="48602-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="48602-395">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="48602-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="48602-396">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-397">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="48602-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-398">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-400">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="48602-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="48602-401">Número máximo de entidades directamente direccionables admitidas por el controlador.</span><span class="sxs-lookup"><span data-stu-id="48602-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="48602-402">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="48602-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="48602-403">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-404">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="48602-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-405">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-407">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="48602-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="48602-408">Frecuencia de actualización máxima del controlador de vídeo en hercios.</span><span class="sxs-lookup"><span data-stu-id="48602-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="48602-409">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-410">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="48602-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-411">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-413">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="48602-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="48602-414">Frecuencia de actualización mínima del controlador de vídeo en hercios.</span><span class="sxs-lookup"><span data-stu-id="48602-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="48602-415">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-416">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="48602-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-417">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-419">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="48602-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="48602-420">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="48602-420">Label by which the object is known.</span></span> <span data-ttu-id="48602-421">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="48602-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="48602-422">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48602-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-423">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="48602-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-424">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-426">Número actual de planos de color.</span><span class="sxs-lookup"><span data-stu-id="48602-426">Current number of color planes.</span></span> <span data-ttu-id="48602-427">Si este valor no es aplicable a la configuración de vídeo actual, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="48602-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="48602-428">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="48602-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-429">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48602-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48602-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-431">Número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="48602-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="48602-432">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="48602-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-436">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="48602-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="48602-437">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="48602-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="48602-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="48602-439">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="48602-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="48602-440">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="48602-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-441">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="48602-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-443">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="48602-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="48602-444">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="48602-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="48602-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="48602-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="48602-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="48602-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48602-449">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="48602-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="48602-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="48602-451">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="48602-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="48602-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="48602-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="48602-453">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="48602-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="48602-454">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="48602-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="48602-455">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="48602-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="48602-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="48602-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="48602-457">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="48602-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="48602-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="48602-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="48602-459">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="48602-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-460">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="48602-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-461">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="48602-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="48602-462">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-463">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="48602-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="48602-464">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="48602-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="48602-465">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="48602-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="48602-466">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="48602-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="48602-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-468">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="48602-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-469">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-471">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="48602-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="48602-472">Protocolo usado por el controlador para tener acceso a los dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="48602-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="48602-473">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="48602-474">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="48602-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-475">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-476">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="48602-477">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="48602-478">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="48602-479">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="48602-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="48602-480">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="48602-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="48602-481">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="48602-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="48602-482">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="48602-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="48602-483">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="48602-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="48602-484">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="48602-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="48602-485">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="48602-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="48602-486">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="48602-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="48602-487">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="48602-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="48602-488">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="48602-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="48602-489">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="48602-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="48602-490">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="48602-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="48602-491">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="48602-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="48602-492">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="48602-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="48602-493">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="48602-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="48602-494">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="48602-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="48602-495">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="48602-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="48602-496">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="48602-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="48602-497">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="48602-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="48602-498">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="48602-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="48602-499">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="48602-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="48602-500">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="48602-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="48602-501">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="48602-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="48602-502">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="48602-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="48602-503">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="48602-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="48602-504">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="48602-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="48602-505">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="48602-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="48602-506">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="48602-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="48602-507">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="48602-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="48602-508">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="48602-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="48602-509">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="48602-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="48602-510">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="48602-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="48602-511">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="48602-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="48602-512">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="48602-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="48602-513">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="48602-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="48602-514">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="48602-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="48602-515">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="48602-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="48602-516">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="48602-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="48602-517">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="48602-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="48602-518">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="48602-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="48602-519">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="48602-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="48602-520">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="48602-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="48602-521">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="48602-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-522">**Estado**</span><span class="sxs-lookup"><span data-stu-id="48602-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-525">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="48602-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="48602-526">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="48602-526">Current status of the object.</span></span> <span data-ttu-id="48602-527">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48602-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="48602-528">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="48602-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="48602-529">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="48602-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="48602-530">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="48602-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="48602-531">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="48602-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-532">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="48602-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="48602-533">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="48602-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="48602-534">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="48602-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="48602-535">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="48602-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="48602-536">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="48602-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="48602-537">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="48602-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="48602-538">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="48602-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="48602-539">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="48602-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="48602-540">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="48602-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="48602-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-542">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-543">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-544">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="48602-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="48602-545">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="48602-545">State of the logical device.</span></span> <span data-ttu-id="48602-546">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="48602-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="48602-547">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-548">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-549">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="48602-550">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="48602-551">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="48602-552">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="48602-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-553">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="48602-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-554">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-555">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-556">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48602-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48602-557">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="48602-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="48602-558">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-559">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="48602-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-560">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-561">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-562">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48602-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48602-563">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="48602-563">Scoping system's name.</span></span>

<span data-ttu-id="48602-564">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="48602-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-565">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="48602-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-566">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48602-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48602-567">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-568">Fecha y hora en que se restableció por última vez este controlador, lo que significa que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="48602-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="48602-569">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="48602-570">**Videoarquitectura**</span><span class="sxs-lookup"><span data-stu-id="48602-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-571">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-572">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-573">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="48602-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="48602-574">Arquitectura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48602-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-575">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-576">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="48602-577">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="48602-578">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="48602-579">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="48602-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="48602-580">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="48602-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="48602-581">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="48602-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="48602-582">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="48602-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="48602-583">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="48602-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="48602-584">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="48602-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="48602-585">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="48602-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="48602-586">**Búfer de trama lineal** (12)</span><span class="sxs-lookup"><span data-stu-id="48602-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="48602-587">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="48602-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-588">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="48602-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-589">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-590">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-591">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="48602-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="48602-592">Tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48602-592">Type of video memory.</span></span>

<span data-ttu-id="48602-593">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48602-594">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="48602-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48602-595">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="48602-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="48602-596">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="48602-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="48602-597">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="48602-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="48602-598">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="48602-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="48602-599">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="48602-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="48602-600">**Edo RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="48602-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="48602-601">**DRAM sincrónica de ráfaga** (8)</span><span class="sxs-lookup"><span data-stu-id="48602-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="48602-602">**SRAM de ráfaga canalizada** (9)</span><span class="sxs-lookup"><span data-stu-id="48602-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="48602-603">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="48602-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="48602-604">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="48602-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="48602-605">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="48602-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="48602-606">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="48602-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48602-607">**Modo**</span><span class="sxs-lookup"><span data-stu-id="48602-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-608">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48602-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48602-609">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48602-610">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="48602-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="48602-611">Modo de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="48602-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="48602-612">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="48602-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48602-613">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48602-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48602-614">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48602-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48602-615">Cadena de forma libre que describe el procesador o controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="48602-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="48602-616">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48602-617">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48602-617">Remarks</span></span>

<span data-ttu-id="48602-618">La **clase \_ PCVideoController de CIM** se deriva [**del \_ videocontrolador CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="48602-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="48602-619">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="48602-619">WMI does not implement this class.</span></span> <span data-ttu-id="48602-620">Para las clases WMI derivadas de [**CIM \_ PCVideoController**](cim-videocontroller.md), vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="48602-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="48602-621">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="48602-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48602-622">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="48602-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48602-623">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48602-623">Requirements</span></span>



| <span data-ttu-id="48602-624">Requisito</span><span class="sxs-lookup"><span data-stu-id="48602-624">Requirement</span></span> | <span data-ttu-id="48602-625">Value</span><span class="sxs-lookup"><span data-stu-id="48602-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48602-626">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48602-626">Minimum supported client</span></span><br/> | <span data-ttu-id="48602-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48602-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48602-628">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48602-628">Minimum supported server</span></span><br/> | <span data-ttu-id="48602-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48602-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48602-630">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48602-630">Namespace</span></span><br/>                | <span data-ttu-id="48602-631">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="48602-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48602-632">MOF</span><span class="sxs-lookup"><span data-stu-id="48602-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48602-633"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48602-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48602-634">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48602-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48602-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48602-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48602-636">Vea también</span><span class="sxs-lookup"><span data-stu-id="48602-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48602-637">**\_Videocontroladora CIM**</span><span class="sxs-lookup"><span data-stu-id="48602-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

