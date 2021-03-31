---
description: Representa las capacidades y la capacidad de administración del controlador de vídeo en un equipo que ejecuta Windows.
ms.assetid: 5c81994b-4a84-46ff-8689-09998dc66f91
ms.tgt_platform: multiple
title: Clase Win32_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoController
- Win32_VideoController.Reset
- Win32_VideoController.SetPowerState
- Win32_VideoController.AcceleratorCapabilities
- Win32_VideoController.AdapterCompatibility
- Win32_VideoController.AdapterDACType
- Win32_VideoController.AdapterRAM
- Win32_VideoController.Availability
- Win32_VideoController.CapabilityDescriptions
- Win32_VideoController.Caption
- Win32_VideoController.ColorTableEntries
- Win32_VideoController.ConfigManagerErrorCode
- Win32_VideoController.ConfigManagerUserConfig
- Win32_VideoController.CreationClassName
- Win32_VideoController.CurrentBitsPerPixel
- Win32_VideoController.CurrentHorizontalResolution
- Win32_VideoController.CurrentNumberOfColors
- Win32_VideoController.CurrentNumberOfColumns
- Win32_VideoController.CurrentNumberOfRows
- Win32_VideoController.CurrentRefreshRate
- Win32_VideoController.CurrentScanMode
- Win32_VideoController.CurrentVerticalResolution
- Win32_VideoController.Description
- Win32_VideoController.DeviceID
- Win32_VideoController.DeviceSpecificPens
- Win32_VideoController.DitherType
- Win32_VideoController.DriverDate
- Win32_VideoController.DriverVersion
- Win32_VideoController.ErrorCleared
- Win32_VideoController.ErrorDescription
- Win32_VideoController.ICMIntent
- Win32_VideoController.ICMMethod
- Win32_VideoController.InfFilename
- Win32_VideoController.InfSection
- Win32_VideoController.InstallDate
- Win32_VideoController.InstalledDisplayDrivers
- Win32_VideoController.LastErrorCode
- Win32_VideoController.MaxMemorySupported
- Win32_VideoController.MaxNumberControlled
- Win32_VideoController.MaxRefreshRate
- Win32_VideoController.MinRefreshRate
- Win32_VideoController.Monochrome
- Win32_VideoController.Name
- Win32_VideoController.NumberOfColorPlanes
- Win32_VideoController.NumberOfVideoPages
- Win32_VideoController.PNPDeviceID
- Win32_VideoController.PowerManagementCapabilities
- Win32_VideoController.PowerManagementSupported
- Win32_VideoController.ProtocolSupported
- Win32_VideoController.ReservedSystemPaletteEntries
- Win32_VideoController.SpecificationVersion
- Win32_VideoController.Status
- Win32_VideoController.StatusInfo
- Win32_VideoController.SystemCreationClassName
- Win32_VideoController.SystemName
- Win32_VideoController.SystemPaletteEntries
- Win32_VideoController.TimeOfLastReset
- Win32_VideoController.VideoArchitecture
- Win32_VideoController.VideoMemoryType
- Win32_VideoController.VideoMode
- Win32_VideoController.VideoModeDescription
- Win32_VideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deb6903ba6cf27170539281da90569a14471999c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495832"
---
# <a name="win32_videocontroller-class"></a><span data-ttu-id="8e202-103">\_Clase de Videocontroller Win32</span><span class="sxs-lookup"><span data-stu-id="8e202-103">Win32\_VideoController class</span></span>

<span data-ttu-id="8e202-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ videocontroller de Win32** representa las capacidades y la capacidad de administración del controlador de vídeo en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="8e202-104">The **Win32\_VideoController** [WMI class](../wmisdk/retrieving-a-class.md) represents the capabilities and management capacity of the video controller on a computer system running Windows.</span></span>

<span data-ttu-id="8e202-105">El hardware que no es compatible con Windows Display Driver Model (WDDM) devuelve valores de propiedad inexactos para las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8e202-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="8e202-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8e202-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e202-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8e202-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e202-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e202-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF1-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoController : CIM_PCVideoController
{
  uint16   AcceleratorCapabilities[];
  string   AdapterCompatibility;
  string   AdapterDACType;
  uint32   AdapterRAM;
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ColorTableEntries;
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
  uint32   DeviceSpecificPens;
  uint32   DitherType;
  datetime DriverDate;
  string   DriverVersion;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   ICMIntent;
  uint32   ICMMethod;
  string   InfFilename;
  string   InfSection;
  datetime InstallDate;
  string   InstalledDisplayDrivers;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  boolean  Monochrome;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  uint32   ReservedSystemPaletteEntries;
  uint32   SpecificationVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   SystemPaletteEntries;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoModeDescription;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="8e202-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e202-109">Members</span></span>

<span data-ttu-id="8e202-110">La clase de **\_ videocontroller de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8e202-110">The **Win32\_VideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="8e202-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8e202-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="8e202-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e202-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8e202-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8e202-113">Methods</span></span>

<span data-ttu-id="8e202-114">La clase de **\_ Videocontroller de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8e202-114">The **Win32\_VideoController** class has these methods.</span></span>



| <span data-ttu-id="8e202-115">Método</span><span class="sxs-lookup"><span data-stu-id="8e202-115">Method</span></span>            | <span data-ttu-id="8e202-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e202-116">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e202-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8e202-117">**Reset**</span></span>         | <span data-ttu-id="8e202-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8e202-118">Not implemented.</span></span> <span data-ttu-id="8e202-119">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/>                 |
| <span data-ttu-id="8e202-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8e202-120">**SetPowerState**</span></span> | <span data-ttu-id="8e202-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8e202-121">Not implemented.</span></span> <span data-ttu-id="8e202-122">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8e202-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e202-123">Properties</span></span>

<span data-ttu-id="8e202-124">La clase de **\_ Videocontroller de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8e202-124">The **Win32\_VideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e202-125">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8e202-125">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-126">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e202-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-128">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8e202-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-129">Matriz de gráficos y capacidades 3D del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-129">Array of graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="8e202-130">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-130">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8e202-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="8e202-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-133"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="8e202-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-134"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-135">Acelerador 3D</span><span class="sxs-lookup"><span data-stu-id="8e202-135">3-D Accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-136">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="8e202-136">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-139">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="8e202-139">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-140">Conjunto de chips general usado para que este controlador Compare las compatibilidades con el sistema.</span><span class="sxs-lookup"><span data-stu-id="8e202-140">General chipset used for this controller to compare compatibilities with the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-141">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="8e202-141">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-144">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. DACType")</span><span class="sxs-lookup"><span data-stu-id="8e202-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.DACType")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-145">Nombre o identificador del chip del convertidor digital a analógico (DAC).</span><span class="sxs-lookup"><span data-stu-id="8e202-145">Name or identifier of the digital-to-analog converter (DAC) chip.</span></span> <span data-ttu-id="8e202-146">El juego de caracteres de esta propiedad es alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="8e202-146">The character set of this property is alphanumeric.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-147">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="8e202-147">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-150">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation. MemorySize"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8e202-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation.MemorySize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-151">Tamaño de memoria del adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-151">Memory size of the video adapter.</span></span>

<span data-ttu-id="8e202-152">Ejemplo: 64000</span><span class="sxs-lookup"><span data-stu-id="8e202-152">Example: 64000</span></span>

</dd> <dt>

<span data-ttu-id="8e202-153">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="8e202-153">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-156">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="8e202-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-157">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-157">Availability and status of the device.</span></span>

<span data-ttu-id="8e202-158">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-158">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-160"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8e202-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-161"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-162">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="8e202-162">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8e202-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-163"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8e202-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-164"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8e202-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="8e202-165"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8e202-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="8e202-166"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8e202-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="8e202-167"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-168">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="8e202-168">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8e202-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="8e202-169"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e202-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="8e202-170"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8e202-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="8e202-171"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8e202-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="8e202-172"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8e202-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="8e202-173"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-174">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="8e202-174">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8e202-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="8e202-175"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-176">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="8e202-176">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8e202-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="8e202-177"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-178">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="8e202-178">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8e202-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="8e202-179"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8e202-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="8e202-180"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-181">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="8e202-181">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8e202-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="8e202-182"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-183">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="8e202-183">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8e202-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="8e202-184"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-185">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="8e202-185">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8e202-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="8e202-186"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-187">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="8e202-187">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8e202-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="8e202-188"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-189">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="8e202-189">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-190">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8e202-190">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-191">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8e202-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8e202-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-193">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**controlador de \_ videojuego CIM**](cim-videocontroller.md).**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="8e202-193">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-194">Cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características del acelerador de vídeo indicadas en la matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="8e202-194">Free-form strings providing more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="8e202-195">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz **AcceleratorCapabilities** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="8e202-195">Note, each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

<span data-ttu-id="8e202-196">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-196">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-197">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8e202-197">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-200">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8e202-200">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-201">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8e202-201">Short description of the object.</span></span>

<span data-ttu-id="8e202-202">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-202">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-203">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="8e202-203">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-204">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-206">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="8e202-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-207">Tamaño de la tabla de colores del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e202-207">Size of the system's color table.</span></span> <span data-ttu-id="8e202-208">El dispositivo debe tener una profundidad de color de no más de 8 bits por píxel. de lo contrario, no se establece esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8e202-208">The device must have a color depth of no more than 8 bits per pixel; otherwise, this property is not set.</span></span>

<span data-ttu-id="8e202-209">Ejemplo: 256</span><span class="sxs-lookup"><span data-stu-id="8e202-209">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="8e202-210">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8e202-210">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-211">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-213">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8e202-213">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-214">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="8e202-214">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8e202-215">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-215">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8e202-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="8e202-216"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8e202-217"> (0)</span><span class="sxs-lookup"><span data-stu-id="8e202-217">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-218">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e202-218">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8e202-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="8e202-219"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8e202-220">(1)</span><span class="sxs-lookup"><span data-stu-id="8e202-220">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-221">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e202-221">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8e202-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-222"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8e202-223">(2)</span><span class="sxs-lookup"><span data-stu-id="8e202-223">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8e202-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="8e202-224"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8e202-225">(3)</span><span class="sxs-lookup"><span data-stu-id="8e202-225">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-226">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="8e202-226">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8e202-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="8e202-227"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8e202-228">(4)</span><span class="sxs-lookup"><span data-stu-id="8e202-228">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-229">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e202-229">Device is not working properly.</span></span> <span data-ttu-id="8e202-230">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="8e202-230">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8e202-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="8e202-231"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8e202-232">(5)</span><span class="sxs-lookup"><span data-stu-id="8e202-232">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-233">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="8e202-233">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8e202-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="8e202-234"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8e202-235"> (6)</span><span class="sxs-lookup"><span data-stu-id="8e202-235">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-236">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8e202-236">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8e202-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="8e202-237"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8e202-238">(7)</span><span class="sxs-lookup"><span data-stu-id="8e202-238">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8e202-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-239"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8e202-240">(8)</span><span class="sxs-lookup"><span data-stu-id="8e202-240">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-241">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-241">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8e202-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="8e202-242"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8e202-243">(9)</span><span class="sxs-lookup"><span data-stu-id="8e202-243">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-244">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e202-244">Device is not working properly.</span></span> <span data-ttu-id="8e202-245">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-245">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8e202-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="8e202-246"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8e202-247">(10)</span><span class="sxs-lookup"><span data-stu-id="8e202-247">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-248">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="8e202-248">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8e202-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-249"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8e202-250">(11)</span><span class="sxs-lookup"><span data-stu-id="8e202-250">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-251">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-251">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8e202-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="8e202-252"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8e202-253">(12)</span><span class="sxs-lookup"><span data-stu-id="8e202-253">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-254">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="8e202-254">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8e202-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-255"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8e202-256">(13)</span><span class="sxs-lookup"><span data-stu-id="8e202-256">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-257">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-257">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8e202-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-258"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8e202-259">(14)</span><span class="sxs-lookup"><span data-stu-id="8e202-259">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-260">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="8e202-260">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8e202-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="8e202-261"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8e202-262">(15)</span><span class="sxs-lookup"><span data-stu-id="8e202-262">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-263">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="8e202-263">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8e202-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8e202-265">(16)</span><span class="sxs-lookup"><span data-stu-id="8e202-265">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-266">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-266">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8e202-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="8e202-267"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8e202-268">(17)</span><span class="sxs-lookup"><span data-stu-id="8e202-268">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-269">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="8e202-269">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8e202-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-270"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8e202-271">(18)</span><span class="sxs-lookup"><span data-stu-id="8e202-271">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-272">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8e202-272">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8e202-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="8e202-273"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8e202-274">(19)</span><span class="sxs-lookup"><span data-stu-id="8e202-274">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8e202-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="8e202-275"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8e202-276">(20)</span><span class="sxs-lookup"><span data-stu-id="8e202-276">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-277">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="8e202-277">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8e202-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8e202-279">(21)</span><span class="sxs-lookup"><span data-stu-id="8e202-279">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-280">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e202-280">System failure.</span></span> <span data-ttu-id="8e202-281">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="8e202-281">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8e202-282">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-282">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8e202-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="8e202-283"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8e202-284">(22)</span><span class="sxs-lookup"><span data-stu-id="8e202-284">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-285">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8e202-285">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8e202-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="8e202-286"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8e202-287">(23)</span><span class="sxs-lookup"><span data-stu-id="8e202-287">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-288">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e202-288">System failure.</span></span> <span data-ttu-id="8e202-289">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="8e202-289">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8e202-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="8e202-290"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8e202-291">(24)</span><span class="sxs-lookup"><span data-stu-id="8e202-291">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-292">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="8e202-292">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8e202-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-293"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8e202-294">(25)</span><span class="sxs-lookup"><span data-stu-id="8e202-294">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-295">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-295">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8e202-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8e202-297">(26)</span><span class="sxs-lookup"><span data-stu-id="8e202-297">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-298">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8e202-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="8e202-299"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8e202-300">(27)</span><span class="sxs-lookup"><span data-stu-id="8e202-300">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-301">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="8e202-301">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8e202-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="8e202-302"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8e202-303">(28)</span><span class="sxs-lookup"><span data-stu-id="8e202-303">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-304">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="8e202-304">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8e202-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="8e202-305"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8e202-306">(29)</span><span class="sxs-lookup"><span data-stu-id="8e202-306">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-307">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8e202-307">Device is disabled.</span></span> <span data-ttu-id="8e202-308">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8e202-308">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8e202-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="8e202-309"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8e202-310">(30)</span><span class="sxs-lookup"><span data-stu-id="8e202-310">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-311">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="8e202-311">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8e202-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8e202-312"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8e202-313">31</span><span class="sxs-lookup"><span data-stu-id="8e202-313">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-314">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8e202-314">Device is not working properly.</span></span> <span data-ttu-id="8e202-315">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8e202-315">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-316">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8e202-316">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-317">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e202-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-319">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8e202-319">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-320">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8e202-320">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8e202-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-322">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e202-322">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-325">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e202-325">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e202-326">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="8e202-326">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8e202-327">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="8e202-327">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8e202-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-329">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="8e202-329">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-330">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-332">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,12 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="8e202-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-333">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="8e202-333">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="8e202-334">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-334">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-335">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="8e202-335">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-336">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-338">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="8e202-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-339">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="8e202-339">Current number of horizontal pixels.</span></span>

<span data-ttu-id="8e202-340">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-340">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-341">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="8e202-341">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8e202-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-344">Número de colores admitidos en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="8e202-344">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="8e202-345">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-345">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="8e202-346">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-346">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-347">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="8e202-347">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-348">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-350">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-351">Número de columnas de este controlador de vídeo (si está en modo de carácter).</span><span class="sxs-lookup"><span data-stu-id="8e202-351">Number of columns for this video controller (if in character mode).</span></span> <span data-ttu-id="8e202-352">En caso contrario, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="8e202-352">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="8e202-353">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-353">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-354">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="8e202-354">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-355">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-357">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-358">Número de filas para este controlador de vídeo (si está en modo de carácter).</span><span class="sxs-lookup"><span data-stu-id="8e202-358">Number of rows for this video controller (if in character mode).</span></span> <span data-ttu-id="8e202-359">En caso contrario, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="8e202-359">Otherwise, enter 0 (zero).</span></span>

<span data-ttu-id="8e202-360">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-360">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-361">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="8e202-361">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-362">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-362">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-364">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hercios")</span><span class="sxs-lookup"><span data-stu-id="8e202-364">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("CurrentRefreshRate"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HardwareInformation."), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-365">Frecuencia con la que el controlador de vídeo actualiza la imagen para el monitor.</span><span class="sxs-lookup"><span data-stu-id="8e202-365">Frequency at which the video controller refreshes the image for the monitor.</span></span> <span data-ttu-id="8e202-366">Un valor de 0 (cero) indica que se está usando la tasa predeterminada, mientras que 0xFFFFFFFF indica que se está usando la velocidad óptima.</span><span class="sxs-lookup"><span data-stu-id="8e202-366">A value of 0 (zero) indicates the default rate is being used, while 0xFFFFFFFF indicates the optimal rate is being used.</span></span>

<span data-ttu-id="8e202-367">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-367">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-368">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="8e202-368">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-369">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-371">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-372">Modo de exploración actual.</span><span class="sxs-lookup"><span data-stu-id="8e202-372">Current scan mode.</span></span>

<span data-ttu-id="8e202-373">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-373">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-374"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="8e202-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Entrelazado** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-376"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="8e202-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**No entrelazado** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-377"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-378">No entrelazado</span><span class="sxs-lookup"><span data-stu-id="8e202-378">Noninterlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-379">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="8e202-379">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-380">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-382">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,10 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="8e202-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-383">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="8e202-383">Current number of vertical pixels.</span></span>

<span data-ttu-id="8e202-384">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-384">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-385">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e202-385">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-386">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-388">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="8e202-388">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-389">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8e202-389">Description of the object.</span></span>

<span data-ttu-id="8e202-390">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-390">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-391">**ID**</span><span class="sxs-lookup"><span data-stu-id="8e202-391">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-392">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-394">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8e202-394">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-395">Identificador (único en el sistema del equipo) para este controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-395">Identifier (unique to the computer system) for this video controller.</span></span>

<span data-ttu-id="8e202-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-397">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="8e202-397">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-398">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-400">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="8e202-400">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-401">Número actual de lápices específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e202-401">Current number of device-specific pens.</span></span> <span data-ttu-id="8e202-402">Un valor de 0xFFFF significa que el dispositivo no admite lápices.</span><span class="sxs-lookup"><span data-stu-id="8e202-402">A value of 0xffff means that the device does not support pens.</span></span>

<span data-ttu-id="8e202-403">Ejemplo: 3</span><span class="sxs-lookup"><span data-stu-id="8e202-403">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="8e202-404">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="8e202-404">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-405">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-407">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device context Functions \| EnumDisplaySettings")</span><span class="sxs-lookup"><span data-stu-id="8e202-407">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|EnumDisplaySettings")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-408">Tipo de interpolación del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-408">Dither type of the video controller.</span></span> <span data-ttu-id="8e202-409">La propiedad puede ser uno de los valores predefinidos o un valor definido por el controlador mayor o igual que 256.</span><span class="sxs-lookup"><span data-stu-id="8e202-409">The property can be one of the predefined values, or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="8e202-410">Si se elige la interpolación de líneas, el controlador usa un método de interpolación que genera bordes bien definidos entre las escalas de color negro, blanco y gris.</span><span class="sxs-lookup"><span data-stu-id="8e202-410">If line art dithering is chosen, the controller uses a dithering method that produces well-defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="8e202-411">La interpolación de líneas de arte no es adecuada para las imágenes que incluyen graduaciones continuas de intensidad y matiz como fotografías digitalizadas.</span><span class="sxs-lookup"><span data-stu-id="8e202-411">Line art dithering is not suitable for images that include continuous graduations in intensity and hue such as scanned photographs.</span></span>

<dt>

<span id="No_dithering"></span><span id="no_dithering"></span><span id="NO_DITHERING"></span>

<span data-ttu-id="8e202-412">**Sin interpolación** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-412">**No dithering** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_coarse_brush"></span><span id="dithering_with_a_coarse_brush"></span><span id="DITHERING_WITH_A_COARSE_BRUSH"></span>

<span data-ttu-id="8e202-413">**Interpolación con un pincel grueso** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-413">**Dithering with a coarse brush** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dithering_with_a_fine_brush"></span><span id="dithering_with_a_fine_brush"></span><span id="DITHERING_WITH_A_FINE_BRUSH"></span>

<span data-ttu-id="8e202-414">**Interpolación con un pincel fino** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-414">**Dithering with a fine brush** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_art_dithering"></span><span id="line_art_dithering"></span><span id="LINE_ART_DITHERING"></span>

<span data-ttu-id="8e202-415">**Interpolación de líneas lineales** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-415">**Line art dithering** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_does_gray_scaling"></span><span id="device_does_gray_scaling"></span><span id="DEVICE_DOES_GRAY_SCALING"></span>

<span data-ttu-id="8e202-416">El **dispositivo realiza el ajuste de escala gris** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-416">**Device does gray scaling** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-417">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="8e202-417">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-418">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e202-418">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-420">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="8e202-420">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-421">Fecha y hora de la última modificación del controlador de vídeo instalado actualmente.</span><span class="sxs-lookup"><span data-stu-id="8e202-421">Last modification date and time of the currently installed video driver.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-422">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="8e202-422">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-423">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-425">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| File Installation Library Functions \| GetFileVersionInfo")</span><span class="sxs-lookup"><span data-stu-id="8e202-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Installation Library Functions\|GetFileVersionInfo")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-426">Número de versión del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-426">Version number of the video driver.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8e202-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-428">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e202-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-430">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="8e202-430">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="8e202-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-432">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8e202-432">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-435">Cadena de forma libre que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="8e202-435">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="8e202-436">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-437">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="8e202-437">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-438">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-440">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Printing and Print spooler Structures \| DEVMODE \| dmICMIntent")</span><span class="sxs-lookup"><span data-stu-id="8e202-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMIntent")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-441">Valor específico de uno de los tres métodos de coincidencia de color posibles o intenciones que se deben usar de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8e202-441">Specific value of one of the three possible color-matching methods or intents that should be used by default.</span></span> <span data-ttu-id="8e202-442">Esta propiedad se usa principalmente para aplicaciones no ICM.</span><span class="sxs-lookup"><span data-stu-id="8e202-442">This property is used primarily for non-ICM applications.</span></span> <span data-ttu-id="8e202-443">Las aplicaciones ICM establecen intenciones mediante el uso de las funciones de ICM.</span><span class="sxs-lookup"><span data-stu-id="8e202-443">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="8e202-444">Esta propiedad puede ser un valor predefinido o un valor definido por el controlador mayor o igual que 256.</span><span class="sxs-lookup"><span data-stu-id="8e202-444">This property can be a predefined value or a driver defined value greater than or equal to 256.</span></span> <span data-ttu-id="8e202-445">La coincidencia de color basada en la saturación es la opción más adecuada para los gráficos de empresa cuando no se desea el tramado.</span><span class="sxs-lookup"><span data-stu-id="8e202-445">Color matching based on saturation is the most appropriate choice for business graphs when dithering is not desired.</span></span> <span data-ttu-id="8e202-446">La coincidencia de color basada en el contraste es la opción más adecuada para imágenes digitalizadas o fotográficas cuando se desea el tramado.</span><span class="sxs-lookup"><span data-stu-id="8e202-446">Color matching based on contrast is the most appropriate choice for scanned or photographic images when dithering is desired.</span></span> <span data-ttu-id="8e202-447">La coincidencia de color optimizada para coincidir con el color exacto solicitado es la más adecuada para su uso con logotipos comerciales u otras imágenes cuando se desea una coincidencia de color exacta.</span><span class="sxs-lookup"><span data-stu-id="8e202-447">Color matching optimized to match the exact color requested is most appropriate for use with business logos or other images when an exact color match is desired.</span></span>

<dt>

<span id="Saturation"></span><span id="saturation"></span><span id="SATURATION"></span>

<span data-ttu-id="8e202-448">**Saturación** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-448">**Saturation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Contrast"></span><span id="contrast"></span><span id="CONTRAST"></span>

<span data-ttu-id="8e202-449">**Contraste** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-449">**Contrast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Exact_Color"></span><span id="exact_color"></span><span id="EXACT_COLOR"></span>

<span data-ttu-id="8e202-450">**Color exacto** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-450">**Exact Color** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-451">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="8e202-451">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-452">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-454">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Printing and Print spooler Structures \| DEVMODE \| dmICMMethod")</span><span class="sxs-lookup"><span data-stu-id="8e202-454">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmICMMethod")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-455">Método para controlar ICM.</span><span class="sxs-lookup"><span data-stu-id="8e202-455">Method of handling ICM.</span></span> <span data-ttu-id="8e202-456">En el caso de las aplicaciones no ICM, esta propiedad determina si está habilitado ICM.</span><span class="sxs-lookup"><span data-stu-id="8e202-456">For non-ICM applications, this property determines if ICM is enabled.</span></span> <span data-ttu-id="8e202-457">En el caso de las aplicaciones ICM, el sistema examina esta propiedad para determinar cómo controlar la compatibilidad con ICM.</span><span class="sxs-lookup"><span data-stu-id="8e202-457">For ICM applications, the system examines this property to determine how to handle ICM support.</span></span> <span data-ttu-id="8e202-458">Esta propiedad puede ser un valor predefinido o un valor definido por el controlador mayor o igual que 256.</span><span class="sxs-lookup"><span data-stu-id="8e202-458">This property can be a predefined value or a driver-defined value greater than or equal to 256.</span></span> <span data-ttu-id="8e202-459">El valor determina qué sistema controla la coincidencia de color de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8e202-459">The value determines which system handles image color matching.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e202-460">**Deshabilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-460">**Disabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows"></span><span id="windows"></span><span id="WINDOWS"></span>

<span data-ttu-id="8e202-461">**Windows** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-461">**Windows** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Driver"></span><span id="device_driver"></span><span id="DEVICE_DRIVER"></span>

<span data-ttu-id="8e202-462">**Controlador de dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-462">**Device Driver** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination_Device"></span><span id="destination_device"></span><span id="DESTINATION_DEVICE"></span>

<span data-ttu-id="8e202-463">**Dispositivo de destino** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-463">**Destination Device** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-464">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="8e202-464">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-465">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-467">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="8e202-467">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-468">Ruta de acceso al archivo. inf del adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-468">Path to the video adapter's .inf file.</span></span>

<span data-ttu-id="8e202-469">Ejemplo: "C: \\ Windows \\ system32 \\ drivers"</span><span class="sxs-lookup"><span data-stu-id="8e202-469">Example: "C:\\Windows\\SYSTEM32\\DRIVERS"</span></span>

</dd> <dt>

<span data-ttu-id="8e202-470">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="8e202-470">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-471">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-473">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \\ \\ {4D36E968-E325-11CE-BFC1-08002BE10318} \\ \\ 0000")</span><span class="sxs-lookup"><span data-stu-id="8e202-473">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E968-E325-11CE-BFC1-08002BE10318}\\\\0000")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-474">Del archivo. inf en el que reside la información de vídeo de Windows.</span><span class="sxs-lookup"><span data-stu-id="8e202-474">Section of the .inf file where the Windows video information resides.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-475">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e202-475">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-476">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e202-476">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-478">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="8e202-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-479">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="8e202-479">Date and time the object was installed.</span></span> <span data-ttu-id="8e202-480">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8e202-480">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8e202-481">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-482">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="8e202-482">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-483">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-484">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-485">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="8e202-485">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-486">Nombre del controlador de dispositivo de pantalla instalado.</span><span class="sxs-lookup"><span data-stu-id="8e202-486">Name of the installed display device driver.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-487">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8e202-487">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-488">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-490">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8e202-490">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8e202-491">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-492">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="8e202-492">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-493">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-494">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-495">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8e202-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-496">Cantidad máxima de memoria admitida en bytes.</span><span class="sxs-lookup"><span data-stu-id="8e202-496">Maximum amount of memory supported in bytes.</span></span>

<span data-ttu-id="8e202-497">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-497">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-498">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="8e202-498">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-499">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-499">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-501">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-501">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-502">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="8e202-502">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="8e202-503">Se debe utilizar un valor de 0 (cero) si se desconoce el número.</span><span class="sxs-lookup"><span data-stu-id="8e202-503">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="8e202-504">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-504">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-505">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="8e202-505">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-506">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-508">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="8e202-508">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-509">Frecuencia de actualización máxima del controlador de vídeo en hercios.</span><span class="sxs-lookup"><span data-stu-id="8e202-509">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="8e202-510">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-510">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-511">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="8e202-511">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-512">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-512">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-514">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,4 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="8e202-514">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-515">Frecuencia de actualización mínima del controlador de vídeo en hercios.</span><span class="sxs-lookup"><span data-stu-id="8e202-515">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="8e202-516">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-516">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-517">**Monocromático**</span><span class="sxs-lookup"><span data-stu-id="8e202-517">**Monochrome**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-518">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e202-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-520">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8e202-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-521">Si es **true**, se usa la escala de grises para mostrar imágenes.</span><span class="sxs-lookup"><span data-stu-id="8e202-521">If **TRUE**, gray scale is used to display images.</span></span>

</dd> <dt>

<span data-ttu-id="8e202-522">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8e202-522">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-525">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8e202-525">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-526">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8e202-526">Label by which the object is known.</span></span> <span data-ttu-id="8e202-527">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="8e202-527">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="8e202-528">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-528">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-529">**NumberOfColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="8e202-529">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-530">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-531">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-532">Número actual de planos de color.</span><span class="sxs-lookup"><span data-stu-id="8e202-532">Current number of color planes.</span></span> <span data-ttu-id="8e202-533">Si este valor no es aplicable a la configuración de vídeo actual, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="8e202-533">If this value is not applicable for the current video configuration, enter 0 (zero).</span></span>

<span data-ttu-id="8e202-534">Esta propiedad se hereda de [**\_ PCVideoController CIM**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-534">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-535">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="8e202-535">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-536">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-536">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-538">Número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="8e202-538">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="8e202-539">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-539">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-540">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8e202-540">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-541">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-543">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8e202-543">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-544">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8e202-544">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="8e202-545">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8e202-545">Example: "\*PNP030b"</span></span>

<span data-ttu-id="8e202-546">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-546">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-547">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8e202-547">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-548">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-548">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e202-549">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-550">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8e202-550">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8e202-551">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-551">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8e202-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8e202-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-553"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e202-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-554"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8e202-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-555"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-556">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8e202-556">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8e202-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-557"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-558">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="8e202-558">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8e202-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-559"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-560">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="8e202-560">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8e202-561">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="8e202-561">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="8e202-562">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-562">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8e202-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="8e202-563"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-564">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="8e202-564">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8e202-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="8e202-565"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-566">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="8e202-566">Timed Power-On Supported</span></span>

<span data-ttu-id="8e202-567">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="8e202-567">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-568">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8e202-568">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-569">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e202-569">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-570">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-570">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-571">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="8e202-571">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="8e202-572">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="8e202-572">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="8e202-573">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-574">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="8e202-574">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-575">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-576">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-577">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-577">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-578">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="8e202-578">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="8e202-579">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-579">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-580"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-581"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="8e202-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-582"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="8e202-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-583"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="8e202-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-584"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="8e202-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="8e202-585"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8e202-586">ATA o ATAPI</span><span class="sxs-lookup"><span data-stu-id="8e202-586">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="8e202-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="8e202-587"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="8e202-588"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="8e202-588"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="8e202-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="8e202-589"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="8e202-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="8e202-590"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="8e202-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="8e202-591"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="8e202-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="8e202-592"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="8e202-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="8e202-593"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="8e202-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="8e202-594"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="8e202-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="8e202-595"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="8e202-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="8e202-596"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="8e202-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="8e202-597"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="8e202-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="8e202-598"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="8e202-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="8e202-599"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="8e202-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="8e202-600"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="8e202-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="8e202-601"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="8e202-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="8e202-602"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="8e202-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="8e202-603"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="8e202-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="8e202-604"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="8e202-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="8e202-605"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="8e202-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="8e202-606"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="8e202-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="8e202-607"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="8e202-608"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="8e202-608"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="8e202-609"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="8e202-609"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="8e202-610"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="8e202-610"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="8e202-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="8e202-611"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="8e202-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="8e202-612"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="8e202-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="8e202-613"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="8e202-614"><span id="ansi_x3t9.5_fddi"></span>**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="8e202-614"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="8e202-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="8e202-615"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="8e202-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="8e202-616"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="8e202-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="8e202-617"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="8e202-618"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="8e202-618"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="8e202-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="8e202-619"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="8e202-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="8e202-620"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="8e202-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="8e202-621"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="8e202-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="8e202-622"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="8e202-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="8e202-623"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="8e202-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="8e202-624"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="8e202-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="8e202-625"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="8e202-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="8e202-626"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="8e202-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="8e202-627"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-628">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="8e202-628">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-629">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-629">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-630">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-631">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="8e202-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-632">Número de entradas reservadas en la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e202-632">Number of reserved entries in the system palette.</span></span> <span data-ttu-id="8e202-633">El sistema operativo puede reservar entradas para admitir los colores estándar de las barras de tareas y otros elementos de visualización del escritorio.</span><span class="sxs-lookup"><span data-stu-id="8e202-633">The operating system may reserve entries to support standard colors for task bars and other desktop display items.</span></span> <span data-ttu-id="8e202-634">Este índice solo es válido si el controlador de dispositivo establece el bit de la **\_ paleta RC** en el índice RASTERCAPS y solo está disponible si el controlador es compatible con Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e202-634">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="8e202-635">Si el sistema no está utilizando una paleta, **ReservedSystemPaletteEntries** no se establece.</span><span class="sxs-lookup"><span data-stu-id="8e202-635">If the system is not using a palette, **ReservedSystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="8e202-636">Ejemplo: 20</span><span class="sxs-lookup"><span data-stu-id="8e202-636">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="8e202-637">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="8e202-637">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-638">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-638">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-639">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-639">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-640">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Printing and Print spooler Structures \| DEVMODE \| dmSpecVersion")</span><span class="sxs-lookup"><span data-stu-id="8e202-640">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Printing and Print Spooler Structures\|DevMode\|dmSpecVersion")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-641">Número de versión de la especificación de datos de inicialización (en la que se basa la estructura).</span><span class="sxs-lookup"><span data-stu-id="8e202-641">Version number of the initialization data specification (upon which the structure is based).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-642">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8e202-642">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-643">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-644">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-644">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-645">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="8e202-645">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-646">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8e202-646">Current status of the object.</span></span> <span data-ttu-id="8e202-647">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="8e202-647">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8e202-648">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8e202-648">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8e202-649">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="8e202-649">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e202-650">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8e202-650">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e202-651">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="8e202-651">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e202-652">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-652">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e202-653">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e202-653">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e202-654">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="8e202-654">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e202-655">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="8e202-655">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e202-656">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8e202-656">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-657">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="8e202-657">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e202-658">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="8e202-658">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e202-659">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="8e202-659">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e202-660">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="8e202-660">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e202-661">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="8e202-661">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e202-662">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="8e202-662">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e202-663">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8e202-663">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e202-664">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="8e202-664">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e202-665">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="8e202-665">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-666">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8e202-666">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-667">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-667">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-668">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-668">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-669">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-669">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-670">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8e202-670">State of the logical device.</span></span> <span data-ttu-id="8e202-671">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="8e202-671">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8e202-672">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-672">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-673">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-673">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-674">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-674">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8e202-675">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-675">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8e202-676">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-676">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8e202-677">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-677">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-678">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e202-678">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-679">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-679">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-680">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-681">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e202-681">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e202-682">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8e202-682">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="8e202-683">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-683">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-684">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8e202-684">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-685">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-685">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-686">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-687">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e202-687">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e202-688">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8e202-688">Name of the scoping system.</span></span>

<span data-ttu-id="8e202-689">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-689">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-690">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="8e202-690">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-691">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e202-691">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-692">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-692">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-693">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="8e202-693">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-694">Número actual de entradas de índice de color en la paleta del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e202-694">Current number of color index entries in the system palette.</span></span> <span data-ttu-id="8e202-695">Este índice solo es válido si el controlador de dispositivo establece el bit de la **\_ paleta RC** en el índice RASTERCAPS y solo está disponible si el controlador es compatible con Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e202-695">This index is valid only if the device driver sets the **RC\_PALETTE** bit in the RASTERCAPS index, and is available only if the driver is compatible with 16-bit Windows.</span></span> <span data-ttu-id="8e202-696">Si el sistema no está utilizando una paleta, **SystemPaletteEntries** no se establece.</span><span class="sxs-lookup"><span data-stu-id="8e202-696">If the system is not using a palette, **SystemPaletteEntries** is not set.</span></span>

<span data-ttu-id="8e202-697">Ejemplo: 20</span><span class="sxs-lookup"><span data-stu-id="8e202-697">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="8e202-698">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="8e202-698">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-699">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e202-699">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-700">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-700">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-701">Fecha y hora en que se restableció por última vez este controlador.</span><span class="sxs-lookup"><span data-stu-id="8e202-701">Date and time this controller was last reset.</span></span> <span data-ttu-id="8e202-702">Esto podría significar que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="8e202-702">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="8e202-703">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-703">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-704">**Videoarquitectura**</span><span class="sxs-lookup"><span data-stu-id="8e202-704">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-705">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-705">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-706">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-706">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-707">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-707">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-708">Tipo de arquitectura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-708">Type of video architecture.</span></span>

<span data-ttu-id="8e202-709">Esta propiedad se hereda de [**\_ PCVideoController CIM**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-709">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-710">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-710">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-711">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-711">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="8e202-712">**CGA** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-712">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="8e202-713">**EGA** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-713">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="8e202-714">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-714">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="8e202-715">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="8e202-715">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="8e202-716">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="8e202-716">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="8e202-717">**HGC** (8)</span><span class="sxs-lookup"><span data-stu-id="8e202-717">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="8e202-718">**MCGA** (9)</span><span class="sxs-lookup"><span data-stu-id="8e202-718">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="8e202-719">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="8e202-719">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="8e202-720">**XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="8e202-720">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="8e202-721">**Búfer de trama lineal** (12)</span><span class="sxs-lookup"><span data-stu-id="8e202-721">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="8e202-722">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="8e202-722">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-723">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="8e202-723">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-724">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-724">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-725">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-726">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-726">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-727">Tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-727">Type of video memory.</span></span>

<span data-ttu-id="8e202-728">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-728">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e202-729">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e202-729">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e202-730">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e202-730">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="8e202-731">**VRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="8e202-731">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="8e202-732">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="8e202-732">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="8e202-733">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="8e202-733">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="8e202-734">**WRAM** (6)</span><span class="sxs-lookup"><span data-stu-id="8e202-734">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="8e202-735">**Edo RAM** (7)</span><span class="sxs-lookup"><span data-stu-id="8e202-735">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="8e202-736">**DRAM sincrónica de ráfaga** (8)</span><span class="sxs-lookup"><span data-stu-id="8e202-736">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="8e202-737">**SRAM de ráfaga canalizada** (9)</span><span class="sxs-lookup"><span data-stu-id="8e202-737">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="8e202-738">**CDRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="8e202-738">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="8e202-739">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="8e202-739">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="8e202-740">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="8e202-740">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="8e202-741">**SGRAM** (13)</span><span class="sxs-lookup"><span data-stu-id="8e202-741">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e202-742">**Modo**</span><span class="sxs-lookup"><span data-stu-id="8e202-742">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-743">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e202-743">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-744">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-744">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-745">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Vídeo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8e202-745">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-746">Modo de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="8e202-746">Current video mode.</span></span>

<span data-ttu-id="8e202-747">Esta propiedad se hereda de [**\_ PCVideoController CIM**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-747">This property is inherited from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e202-748">**VideoModeDescription**</span><span class="sxs-lookup"><span data-stu-id="8e202-748">**VideoModeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-749">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-750">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-750">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e202-751">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span><span class="sxs-lookup"><span data-stu-id="8e202-751">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)")</span></span>
</dt> </dl>

<span data-ttu-id="8e202-752">Configuración actual de la resolución, el color y el modo de exploración del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-752">Current resolution, color, and scan mode settings of the video controller.</span></span>

<span data-ttu-id="8e202-753">Ejemplo: "1024 x 768 x 256 colores"</span><span class="sxs-lookup"><span data-stu-id="8e202-753">Example: "1024 x 768 x 256 colors"</span></span>

</dd> <dt>

<span data-ttu-id="8e202-754">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="8e202-754">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e202-755">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e202-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e202-756">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e202-756">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e202-757">Cadena de forma libre que describe el procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-757">Free-form string describing the video processor.</span></span>

<span data-ttu-id="8e202-758">Esta propiedad se hereda del [**\_ controlador de videodispositivo CIM**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-758">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e202-759">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e202-759">Remarks</span></span>

<span data-ttu-id="8e202-760">La clase de **\_ videocontroladora Win32** se deriva de [**CIM \_ PCVideoController**](cim-pcvideocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8e202-760">The **Win32\_VideoController** class is derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md).</span></span>

<span data-ttu-id="8e202-761">Para obtener más información sobre el uso de esta clase, como la recuperación de información de varios monitores, consulte [uso de PowerShell para detectar información de varios](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx)monitores.</span><span class="sxs-lookup"><span data-stu-id="8e202-761">For more information about using this class, such as retrieving information from multiple monitors, see [Use PowerShell to Discover Multi-Monitor Information](https://blogs.technet.com/b/heyscriptingguy/archive/2013/10/03/use-powershell-to-discover-multi-monitor-information.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="8e202-762">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8e202-762">Examples</span></span>

<span data-ttu-id="8e202-763">En el ejemplo de la [lista de propiedades del controlador de vídeo](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) de VBScript se enumeran las propiedades del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-763">The [List Video Controller Properties](https://Gallery.TechNet.Microsoft.Com/6c1a585c-742f-4f51-bb57-23838e8f011f) VBScript sample lists the video controller properties.</span></span>

<span data-ttu-id="8e202-764">En el siguiente ejemplo de PowerShell se enumeran las propiedades del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e202-764">The following PowerShell example lists the video controller properties.</span></span>


```VB
$strComputer = "." 
 
$colItems = get-wmiobject -class "Win32_VideoController" -namespace "root\CIMV2" ` 
-computername $strComputer 
 
foreach ($objItem in $colItems) { 
      write-host "Accelerator Capabilities: " $objItem.AcceleratorCapabilities 
      write-host "Adapter Compatibility: " $objItem.AdapterCompatibility 
      write-host "Adapter DAC Type: " $objItem.AdapterDACType 
      write-host "Adapter RAM: " $objItem.AdapterRAM 
      write-host "Availability: " $objItem.Availability 
      write-host "Capability Descriptions: " $objItem.CapabilityDescriptions 
      write-host "Caption: " $objItem.Caption 
      write-host "Color Table Entries: " $objItem.ColorTableEntries 
      write-host "Configuration Manager Error Code: " $objItem.ConfigManagerErrorCode 
      write-host "Configuration Manager User Configuration: " $objItem.ConfigManagerUserConfig 
      write-host "Creation Class Name: " $objItem.CreationClassName 
      write-host "Current Bits Per Pixel: " $objItem.CurrentBitsPerPixel 
      write-host "Current Horizontal Resolution: " $objItem.CurrentHorizontalResolution 
      write-host "Current Number Of Colors: " $objItem.CurrentNumberOfColors 
      write-host "Current Number Of Columns: " $objItem.CurrentNumberOfColumns 
      write-host "Current Number Of Rows: " $objItem.CurrentNumberOfRows 
      write-host "Current Refresh Rate: " $objItem.CurrentRefreshRate 
      write-host "Current Scan Mode: " $objItem.CurrentScanMode 
      write-host "Current Vertical Resolution: " $objItem.CurrentVerticalResolution 
      write-host "Description: " $objItem.Description 
      write-host "Device ID: " $objItem.DeviceID 
      write-host "Device Specific Pens: " $objItem.DeviceSpecificPens 
      write-host "Dither Type: " $objItem.DitherType 
      write-host "Driver Date: " $objItem.DriverDate 
      write-host "Driver Version: " $objItem.DriverVersion 
      write-host "Error Cleared: " $objItem.ErrorCleared 
      write-host "Error Description: " $objItem.ErrorDescription 
      write-host "ICM Intent: " $objItem.ICMIntent 
      write-host "ICM Method: " $objItem.ICMMethod 
      write-host "Inf File Name: " $objItem.InfFilename 
      write-host "Inf Section: " $objItem.InfSection 
      write-host "Installation Date: " $objItem.InstallDate 
      write-host "Installed Display Drivers: " $objItem.InstalledDisplayDrivers 
      write-host "Last Error Code: " $objItem.LastErrorCode 
      write-host "Maximum Memory Supported: " $objItem.MaxMemorySupported 
      write-host "Maximum Number Controlled: " $objItem.MaxNumberControlled 
      write-host "Maximum Refresh Rate: " $objItem.MaxRefreshRate 
      write-host "Minimum Refresh Rate: " $objItem.MinRefreshRate 
      write-host "Monochrome: " $objItem.Monochrome 
      write-host "Name: " $objItem.Name 
      write-host "Number Of Color Planes: " $objItem.NumberOfColorPlanes 
      write-host "Number Of Video Pages: " $objItem.NumberOfVideoPages 
      write-host "PNP Device ID: " $objItem.PNPDeviceID 
      write-host "Power Management Capabilities: " $objItem.PowerManagementCapabilities 
      write-host "Power Management Supported: " $objItem.PowerManagementSupported 
      write-host "Protocol Supported: " $objItem.ProtocolSupported 
      write-host "Reserved System Palette Entries: " $objItem.ReservedSystemPaletteEntries 
      write-host "Specification Version: " $objItem.SpecificationVersion 
      write-host "Status: " $objItem.Status 
      write-host "Status Information: " $objItem.StatusInfo 
      write-host "System Creation Class Name: " $objItem.SystemCreationClassName 
      write-host "System Name: " $objItem.SystemName 
      write-host "System Palette Entries: " $objItem.SystemPaletteEntries 
      write-host "Time Of Last Reset: " $objItem.TimeOfLastReset 
      write-host "Video Architecture: " $objItem.VideoArchitecture 
      write-host "Video Memory Type: " $objItem.VideoMemoryType 
      write-host "Video Mode: " $objItem.VideoMode 
      write-host "Video Mode Description: " $objItem.VideoModeDescription 
      write-host "Video Processor: " $objItem.VideoProcessor 
      write-host 
} 
```



## <a name="requirements"></a><span data-ttu-id="8e202-765">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e202-765">Requirements</span></span>



| <span data-ttu-id="8e202-766">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e202-766">Requirement</span></span> | <span data-ttu-id="8e202-767">Value</span><span class="sxs-lookup"><span data-stu-id="8e202-767">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e202-768">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e202-768">Minimum supported client</span></span><br/> | <span data-ttu-id="8e202-769">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e202-769">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e202-770">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e202-770">Minimum supported server</span></span><br/> | <span data-ttu-id="8e202-771">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e202-771">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e202-772">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e202-772">Namespace</span></span><br/>                | <span data-ttu-id="8e202-773">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e202-773">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e202-774">MOF</span><span class="sxs-lookup"><span data-stu-id="8e202-774">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e202-775"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e202-775"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e202-776">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e202-776">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e202-777"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e202-777"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e202-778">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e202-778">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e202-779">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="8e202-779">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="8e202-780">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8e202-780">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
