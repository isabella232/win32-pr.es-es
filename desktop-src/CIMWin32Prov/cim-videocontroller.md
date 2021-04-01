---
description: La \_ clase de Videocontroladora CIM representa las capacidades y la administración del controlador de vídeo.
ms.assetid: 7cf6bf2a-62a5-46fa-8c8f-976604360461
ms.tgt_platform: multiple
title: CIM_VideoController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController
- CIM_VideoController.AcceleratorCapabilities
- CIM_VideoController.Availability
- CIM_VideoController.CapabilityDescriptions
- CIM_VideoController.Caption
- CIM_VideoController.ConfigManagerErrorCode
- CIM_VideoController.ConfigManagerUserConfig
- CIM_VideoController.CreationClassName
- CIM_VideoController.CurrentBitsPerPixel
- CIM_VideoController.CurrentHorizontalResolution
- CIM_VideoController.CurrentNumberOfColors
- CIM_VideoController.CurrentNumberOfColumns
- CIM_VideoController.CurrentNumberOfRows
- CIM_VideoController.CurrentRefreshRate
- CIM_VideoController.CurrentScanMode
- CIM_VideoController.CurrentVerticalResolution
- CIM_VideoController.Description
- CIM_VideoController.DeviceID
- CIM_VideoController.ErrorCleared
- CIM_VideoController.ErrorDescription
- CIM_VideoController.InstallDate
- CIM_VideoController.LastErrorCode
- CIM_VideoController.MaxMemorySupported
- CIM_VideoController.MaxNumberControlled
- CIM_VideoController.MaxRefreshRate
- CIM_VideoController.MinRefreshRate
- CIM_VideoController.Name
- CIM_VideoController.NumberOfVideoPages
- CIM_VideoController.PNPDeviceID
- CIM_VideoController.PowerManagementCapabilities
- CIM_VideoController.PowerManagementSupported
- CIM_VideoController.ProtocolSupported
- CIM_VideoController.Status
- CIM_VideoController.StatusInfo
- CIM_VideoController.SystemCreationClassName
- CIM_VideoController.SystemName
- CIM_VideoController.TimeOfLastReset
- CIM_VideoController.VideoMemoryType
- CIM_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6475c99e7a6f2ee1bef56bf2c266c788efc0b805
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907430"
---
# <a name="cim_videocontroller-class"></a><span data-ttu-id="36a29-103">\_Clase de Videocontroladora CIM</span><span class="sxs-lookup"><span data-stu-id="36a29-103">CIM\_VideoController class</span></span>

<span data-ttu-id="36a29-104">La clase de **\_ videocontroladora CIM** representa las capacidades y la administración del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="36a29-104">The **CIM\_VideoController** class represents the capabilities and management of the video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36a29-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="36a29-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36a29-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36a29-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36a29-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="36a29-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="36a29-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="36a29-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a29-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36a29-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE5-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoController : CIM_Controller
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
  uint16   VideoMemoryType;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="36a29-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="36a29-110">Members</span></span>

<span data-ttu-id="36a29-111">La clase de **\_ videocontroller CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36a29-111">The **CIM\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="36a29-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="36a29-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="36a29-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36a29-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="36a29-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="36a29-114">Methods</span></span>

<span data-ttu-id="36a29-115">La clase de **\_ videocontroller CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="36a29-115">The **CIM\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="36a29-116">Método</span><span class="sxs-lookup"><span data-stu-id="36a29-116">Method</span></span>                                                                     | <span data-ttu-id="36a29-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="36a29-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36a29-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="36a29-118">**Reset**</span></span>](reset-method-in-class-cim-videocontroller.md)                 | <span data-ttu-id="36a29-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a29-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="36a29-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="36a29-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="36a29-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="36a29-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-videocontroller.md) | <span data-ttu-id="36a29-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="36a29-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="36a29-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="36a29-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="36a29-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36a29-124">Properties</span></span>

<span data-ttu-id="36a29-125">La clase de **\_ videocontroller CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="36a29-125">The **CIM\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36a29-126">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="36a29-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-127">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36a29-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-129">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ controlador de videojuego CIM**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="36a29-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-130">Gráficos y capacidades 3D del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="36a29-130">Graphics and 3-D capabilities of the video controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-131">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="36a29-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="36a29-132">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="36a29-133">**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-133">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="36a29-134">**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-134">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-135">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="36a29-135">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-136">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="36a29-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-139">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-139">Availability and status of the device.</span></span>

<span data-ttu-id="36a29-140">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-140">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="36a29-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-141"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="36a29-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-143"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="36a29-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="36a29-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="36a29-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="36a29-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="36a29-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="36a29-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="36a29-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="36a29-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="36a29-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="36a29-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="36a29-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="36a29-149"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="36a29-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="36a29-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="36a29-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="36a29-151"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="36a29-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="36a29-152"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="36a29-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="36a29-153"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-154">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="36a29-154">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="36a29-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="36a29-155"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-156">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="36a29-156">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="36a29-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="36a29-157"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-158">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="36a29-158">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="36a29-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="36a29-159"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="36a29-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="36a29-160"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-161">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="36a29-161">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="36a29-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="36a29-162"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-163">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="36a29-163">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="36a29-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="36a29-164"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-165">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="36a29-165">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="36a29-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="36a29-166"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-167">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="36a29-167">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="36a29-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="36a29-168"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-169">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="36a29-169">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-170">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="36a29-170">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-171">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="36a29-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="36a29-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-173">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**controlador de \_ videojuego CIM**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="36a29-173">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-174">Cadenas de forma libre que proporcionan descripciones detalladas de las características del acelerador de vídeo indicadas en la matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="36a29-174">Free-form strings that provide detailed descriptions for the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="36a29-175">Cada entrada de esta matriz está relacionada con la entrada de la matriz **AcceleratorCapabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="36a29-175">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="36a29-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="36a29-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-179">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="36a29-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-180">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="36a29-180">Short textual description of the object.</span></span>

<span data-ttu-id="36a29-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-182">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="36a29-182">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-183">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-185">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="36a29-185">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-186">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="36a29-186">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="36a29-187">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-187">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="36a29-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="36a29-188"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="36a29-189"> (0)</span><span class="sxs-lookup"><span data-stu-id="36a29-189">(0)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-190">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="36a29-190">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="36a29-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="36a29-191"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="36a29-192">(1)</span><span class="sxs-lookup"><span data-stu-id="36a29-192">(1)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-193">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="36a29-193">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="36a29-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-194"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="36a29-195">(2)</span><span class="sxs-lookup"><span data-stu-id="36a29-195">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="36a29-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="36a29-196"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="36a29-197">(3)</span><span class="sxs-lookup"><span data-stu-id="36a29-197">(3)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-198">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="36a29-198">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="36a29-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="36a29-199"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="36a29-200">(4)</span><span class="sxs-lookup"><span data-stu-id="36a29-200">(4)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-201">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="36a29-201">Device is not working properly.</span></span> <span data-ttu-id="36a29-202">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="36a29-202">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="36a29-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="36a29-203"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="36a29-204">(5)</span><span class="sxs-lookup"><span data-stu-id="36a29-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-205">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="36a29-205">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="36a29-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="36a29-206"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="36a29-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="36a29-207">(6)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-208">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="36a29-208">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="36a29-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="36a29-209"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="36a29-210">(7)</span><span class="sxs-lookup"><span data-stu-id="36a29-210">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="36a29-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-211"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="36a29-212">(8)</span><span class="sxs-lookup"><span data-stu-id="36a29-212">(8)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-213">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-213">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="36a29-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="36a29-214"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="36a29-215">(9)</span><span class="sxs-lookup"><span data-stu-id="36a29-215">(9)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-216">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="36a29-216">Device is not working properly.</span></span> <span data-ttu-id="36a29-217">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-217">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="36a29-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="36a29-218"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="36a29-219">(10)</span><span class="sxs-lookup"><span data-stu-id="36a29-219">(10)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-220">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="36a29-220">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="36a29-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-221"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="36a29-222">(11)</span><span class="sxs-lookup"><span data-stu-id="36a29-222">(11)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-223">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-223">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="36a29-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="36a29-224"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="36a29-225">(12)</span><span class="sxs-lookup"><span data-stu-id="36a29-225">(12)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-226">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="36a29-226">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="36a29-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-227"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="36a29-228">(13)</span><span class="sxs-lookup"><span data-stu-id="36a29-228">(13)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-229">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-229">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="36a29-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-230"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="36a29-231">(14)</span><span class="sxs-lookup"><span data-stu-id="36a29-231">(14)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-232">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="36a29-232">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="36a29-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="36a29-233"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="36a29-234">(15)</span><span class="sxs-lookup"><span data-stu-id="36a29-234">(15)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-235">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="36a29-235">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="36a29-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-236"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="36a29-237">(16)</span><span class="sxs-lookup"><span data-stu-id="36a29-237">(16)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-238">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-238">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="36a29-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="36a29-239"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="36a29-240">(17)</span><span class="sxs-lookup"><span data-stu-id="36a29-240">(17)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-241">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="36a29-241">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="36a29-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-242"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="36a29-243">(18)</span><span class="sxs-lookup"><span data-stu-id="36a29-243">(18)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-244">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="36a29-244">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="36a29-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="36a29-245"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="36a29-246">(19)</span><span class="sxs-lookup"><span data-stu-id="36a29-246">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="36a29-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="36a29-247"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="36a29-248">(20)</span><span class="sxs-lookup"><span data-stu-id="36a29-248">(20)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-249">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="36a29-249">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="36a29-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="36a29-251">(21)</span><span class="sxs-lookup"><span data-stu-id="36a29-251">(21)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-252">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="36a29-252">System failure.</span></span> <span data-ttu-id="36a29-253">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="36a29-253">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="36a29-254">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-254">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="36a29-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="36a29-255"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="36a29-256">(22)</span><span class="sxs-lookup"><span data-stu-id="36a29-256">(22)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-257">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="36a29-257">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="36a29-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="36a29-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="36a29-259">(23)</span><span class="sxs-lookup"><span data-stu-id="36a29-259">(23)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-260">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="36a29-260">System failure.</span></span> <span data-ttu-id="36a29-261">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="36a29-261">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="36a29-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="36a29-262"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="36a29-263">(24)</span><span class="sxs-lookup"><span data-stu-id="36a29-263">(24)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-264">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="36a29-264">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="36a29-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="36a29-266">(25)</span><span class="sxs-lookup"><span data-stu-id="36a29-266">(25)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-267">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="36a29-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-268"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="36a29-269">(26)</span><span class="sxs-lookup"><span data-stu-id="36a29-269">(26)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-270">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36a29-270">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="36a29-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="36a29-271"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="36a29-272">(27)</span><span class="sxs-lookup"><span data-stu-id="36a29-272">(27)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-273">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="36a29-273">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="36a29-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="36a29-274"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="36a29-275">(28)</span><span class="sxs-lookup"><span data-stu-id="36a29-275">(28)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-276">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="36a29-276">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="36a29-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="36a29-277"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="36a29-278">(29)</span><span class="sxs-lookup"><span data-stu-id="36a29-278">(29)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-279">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="36a29-279">Device is disabled.</span></span> <span data-ttu-id="36a29-280">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="36a29-280">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="36a29-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="36a29-281"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="36a29-282">(30)</span><span class="sxs-lookup"><span data-stu-id="36a29-282">(30)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-283">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="36a29-283">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="36a29-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="36a29-284"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="36a29-285">31</span><span class="sxs-lookup"><span data-stu-id="36a29-285">(31)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-286">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="36a29-286">Device is not working properly.</span></span> <span data-ttu-id="36a29-287">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="36a29-287">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="36a29-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-289">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="36a29-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-291">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="36a29-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-292">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="36a29-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="36a29-293">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="36a29-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-297">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="36a29-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="36a29-298">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="36a29-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="36a29-299">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="36a29-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="36a29-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-301">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="36a29-301">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-302">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-304">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="36a29-304">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-305">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="36a29-305">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-306">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="36a29-306">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-307">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-309">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="36a29-309">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-310">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="36a29-310">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-311">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="36a29-311">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-312">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="36a29-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-314">Número de colores admitidos en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="36a29-314">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="36a29-315">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="36a29-315">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-316">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="36a29-316">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-317">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-319">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-320">Si está en modo de carácter, número de columnas para el controlador de vídeo; en caso contrario, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="36a29-320">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-321">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="36a29-321">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-322">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-324">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-325">Si está en modo de carácter, número de filas para el controlador de vídeo; en caso contrario, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="36a29-325">If in character mode, number of rows for the video controller; otherwise, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-326">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="36a29-326">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-327">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-329">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="36a29-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-330">Frecuencia de actualización actual, en hercios.</span><span class="sxs-lookup"><span data-stu-id="36a29-330">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-331">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="36a29-331">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-332">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-334">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-335">Modo de exploración actual.</span><span class="sxs-lookup"><span data-stu-id="36a29-335">Current scan mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="36a29-336">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-336">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-337">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-337">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="36a29-338">**Entrelazado** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-338">**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="36a29-339">**No entrelazado** (4)</span><span class="sxs-lookup"><span data-stu-id="36a29-339">**Non Interlaced** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-340">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="36a29-340">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-341">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-343">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="36a29-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-344">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="36a29-344">Current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-345">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="36a29-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-348">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="36a29-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-349">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="36a29-349">Textual description of the object.</span></span>

<span data-ttu-id="36a29-350">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-351">**ID**</span><span class="sxs-lookup"><span data-stu-id="36a29-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-354">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="36a29-354">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="36a29-355">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a29-355">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="36a29-356">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-357">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="36a29-357">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-358">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="36a29-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-360">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="36a29-360">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="36a29-361">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-362">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="36a29-362">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-363">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-365">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="36a29-365">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="36a29-366">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-367">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="36a29-367">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-368">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="36a29-368">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-370">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="36a29-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-371">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="36a29-371">Date and time the object was installed.</span></span> <span data-ttu-id="36a29-372">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="36a29-372">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="36a29-373">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-374">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="36a29-374">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-375">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-377">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a29-377">Last error code reported by the logical device.</span></span>

<span data-ttu-id="36a29-378">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-379">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="36a29-379">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-380">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-382">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="36a29-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-383">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="36a29-383">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-384">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="36a29-384">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-385">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-387">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-388">Número máximo de entidades directamente direccionables admitidas por el controlador.</span><span class="sxs-lookup"><span data-stu-id="36a29-388">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="36a29-389">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="36a29-389">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="36a29-390">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-390">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-391">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="36a29-391">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-392">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="36a29-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-395">Frecuencia de actualización máxima del controlador de vídeo, en hercios.</span><span class="sxs-lookup"><span data-stu-id="36a29-395">Maximum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-396">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="36a29-396">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-397">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-397">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-399">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="36a29-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-400">Frecuencia de actualización mínima del controlador de vídeo, en hercios.</span><span class="sxs-lookup"><span data-stu-id="36a29-400">Minimum refresh rate of the video controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-401">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="36a29-401">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-402">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-404">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="36a29-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-405">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="36a29-405">Label by which the object is known.</span></span> <span data-ttu-id="36a29-406">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="36a29-406">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="36a29-407">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-408">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="36a29-408">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-409">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36a29-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-411">Número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="36a29-411">Number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="36a29-412">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="36a29-412">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-413">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-415">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="36a29-415">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-416">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a29-416">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="36a29-417">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="36a29-418">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="36a29-418">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="36a29-419">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="36a29-419">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-420">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="36a29-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-422">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a29-422">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="36a29-423">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="36a29-423">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="36a29-424"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="36a29-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-425"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="36a29-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-426"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="36a29-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-427"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-428">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="36a29-428">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="36a29-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="36a29-429"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-430">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="36a29-430">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="36a29-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="36a29-431"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-432">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="36a29-432">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="36a29-433">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="36a29-433">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="36a29-434">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="36a29-434">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="36a29-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="36a29-435"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-436">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="36a29-436">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="36a29-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="36a29-437"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="36a29-438">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="36a29-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-439">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="36a29-439">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-440">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="36a29-440">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-442">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="36a29-442">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="36a29-443">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="36a29-443">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="36a29-444">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="36a29-444">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="36a29-445">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="36a29-445">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="36a29-446">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-447">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="36a29-447">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-448">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-450">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-451">Protocolo usado por el controlador para tener acceso a los dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="36a29-451">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="36a29-452">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-452">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="36a29-453">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="36a29-453">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="36a29-454">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-454">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-455">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-455">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="36a29-456">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-456">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="36a29-457">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="36a29-457">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="36a29-458">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="36a29-458">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="36a29-459">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="36a29-459">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="36a29-460">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="36a29-460">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="36a29-461">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="36a29-461">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="36a29-462">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="36a29-462">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="36a29-463">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="36a29-463">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="36a29-464">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="36a29-464">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="36a29-465">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="36a29-465">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="36a29-466">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="36a29-466">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="36a29-467">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="36a29-467">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="36a29-468">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="36a29-468">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="36a29-469">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="36a29-469">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="36a29-470">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="36a29-470">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="36a29-471">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="36a29-471">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="36a29-472">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="36a29-472">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="36a29-473">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="36a29-473">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="36a29-474">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="36a29-474">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="36a29-475">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="36a29-475">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="36a29-476">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="36a29-476">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="36a29-477">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="36a29-477">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="36a29-478">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="36a29-478">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="36a29-479">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="36a29-479">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="36a29-480">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="36a29-480">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="36a29-481">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="36a29-481">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="36a29-482">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="36a29-482">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="36a29-483">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="36a29-483">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="36a29-484">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="36a29-484">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="36a29-485">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="36a29-485">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="36a29-486">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="36a29-486">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="36a29-487">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="36a29-487">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="36a29-488">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="36a29-488">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="36a29-489">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="36a29-489">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="36a29-490">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="36a29-490">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="36a29-491">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="36a29-491">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="36a29-492">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="36a29-492">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="36a29-493">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="36a29-493">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="36a29-494">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="36a29-494">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="36a29-495">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="36a29-495">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="36a29-496">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="36a29-496">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="36a29-497">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="36a29-497">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="36a29-498">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="36a29-498">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="36a29-499">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="36a29-499">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="36a29-500">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="36a29-500">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-501">**Estado**</span><span class="sxs-lookup"><span data-stu-id="36a29-501">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-502">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-504">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="36a29-504">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-505">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="36a29-505">Current status of the object.</span></span> <span data-ttu-id="36a29-506">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-506">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="36a29-507">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="36a29-507">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="36a29-508">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="36a29-508">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="36a29-509">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="36a29-509">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="36a29-510">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="36a29-510">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-511">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="36a29-511">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="36a29-512">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="36a29-512">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="36a29-513">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="36a29-513">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="36a29-514">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="36a29-514">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="36a29-515">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="36a29-515">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="36a29-516">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="36a29-516">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="36a29-517">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="36a29-517">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="36a29-518">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="36a29-518">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="36a29-519">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="36a29-519">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-520">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="36a29-520">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-521">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-522">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-523">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-524">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="36a29-524">State of the logical device.</span></span> <span data-ttu-id="36a29-525">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="36a29-525">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="36a29-526">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-526">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="36a29-527">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-527">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-528">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-528">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="36a29-529">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-529">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="36a29-530">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="36a29-530">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="36a29-531">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="36a29-531">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="36a29-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-533">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-534">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-535">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="36a29-535">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="36a29-536">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="36a29-536">Scoping system's creation class name.</span></span>

<span data-ttu-id="36a29-537">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-537">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-538">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="36a29-538">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-539">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-540">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-541">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="36a29-541">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="36a29-542">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="36a29-542">Scoping system's name.</span></span>

<span data-ttu-id="36a29-543">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-543">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-544">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="36a29-544">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-545">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="36a29-545">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-546">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-546">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-547">Fecha y hora de la última vez que se restableció el controlador, lo que significa que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="36a29-547">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="36a29-548">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-548">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="36a29-549">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="36a29-549">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-550">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="36a29-550">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-551">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-551">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36a29-552">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="36a29-552">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="36a29-553">Tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="36a29-553">Type of video memory.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="36a29-554">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="36a29-554">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36a29-555">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="36a29-555">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="36a29-556">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="36a29-556">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="36a29-557">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="36a29-557">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="36a29-558">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="36a29-558">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="36a29-559">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="36a29-559">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="36a29-560">**Edo RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="36a29-560">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="36a29-561">**DRAM sincrónica de ráfaga** (8)</span><span class="sxs-lookup"><span data-stu-id="36a29-561">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="36a29-562">**SRAM de ráfaga canalizada** (9)</span><span class="sxs-lookup"><span data-stu-id="36a29-562">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="36a29-563">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="36a29-563">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="36a29-564">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="36a29-564">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="36a29-565">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="36a29-565">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="36a29-566">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="36a29-566">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="36a29-567">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="36a29-567">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36a29-568">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="36a29-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36a29-569">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="36a29-569">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="36a29-570">Cadena de forma libre que describe el procesador de vídeo o el controlador.</span><span class="sxs-lookup"><span data-stu-id="36a29-570">Free-form string that describes the video processor or controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36a29-571">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36a29-571">Remarks</span></span>

<span data-ttu-id="36a29-572">La clase de **\_ videocontroladora CIM** se deriva del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-572">The **CIM\_VideoController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="36a29-573">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="36a29-573">WMI does not implement this class.</span></span> <span data-ttu-id="36a29-574">En el caso de las clases WMI derivadas de un **\_ videocontrolador CIM**, consulte [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36a29-574">For WMI classes derived from **CIM\_VideoController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="36a29-575">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="36a29-575">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36a29-576">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="36a29-576">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36a29-577">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36a29-577">Requirements</span></span>



| <span data-ttu-id="36a29-578">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a29-578">Requirement</span></span> | <span data-ttu-id="36a29-579">Value</span><span class="sxs-lookup"><span data-stu-id="36a29-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36a29-580">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a29-580">Minimum supported client</span></span><br/> | <span data-ttu-id="36a29-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36a29-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36a29-582">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36a29-582">Minimum supported server</span></span><br/> | <span data-ttu-id="36a29-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36a29-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36a29-584">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="36a29-584">Namespace</span></span><br/>                | <span data-ttu-id="36a29-585">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="36a29-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36a29-586">MOF</span><span class="sxs-lookup"><span data-stu-id="36a29-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36a29-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36a29-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36a29-588">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36a29-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36a29-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36a29-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a29-590">Vea también</span><span class="sxs-lookup"><span data-stu-id="36a29-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a29-591">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="36a29-591">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

