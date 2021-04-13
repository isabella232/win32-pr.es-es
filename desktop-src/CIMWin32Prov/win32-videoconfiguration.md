---
description: La clase de configuración videowin32 \_ no está activa. No devolverá ninguna instancia, ya que no hay ningún proveedor que la respalde.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538548"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="049b3-104">Clase de configuración de videowin32 \_</span><span class="sxs-lookup"><span data-stu-id="049b3-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="049b3-105">La clase de **\_ configuración videowin32** no está activa.</span><span class="sxs-lookup"><span data-stu-id="049b3-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="049b3-106">No devolverá ninguna instancia, ya que no hay ningún proveedor que la respalde.</span><span class="sxs-lookup"><span data-stu-id="049b3-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="049b3-107">La clase de **\_ configuración videowin32** representa una configuración de un subsistema de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="049b3-108">Esta clase ha quedado en desuso en favor de las propiedades contenidas en las clases [**\_ videocontroller de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)y [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)</span><span class="sxs-lookup"><span data-stu-id="049b3-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="049b3-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="049b3-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="049b3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="049b3-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="049b3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="049b3-111">Members</span></span>

<span data-ttu-id="049b3-112">La clase de **\_ configuración videowin32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="049b3-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="049b3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="049b3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="049b3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="049b3-114">Properties</span></span>

<span data-ttu-id="049b3-115">La clase de **\_ configuración videowin32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="049b3-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="049b3-116">**ActualColorResolution**</span><span class="sxs-lookup"><span data-stu-id="049b3-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-119">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por píxel")</span><span class="sxs-lookup"><span data-stu-id="049b3-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-120">Indica la profundidad de color actual de la pantalla de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="049b3-121">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-122">**AdapterChipType**</span><span class="sxs-lookup"><span data-stu-id="049b3-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-125">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| ChipType")</span><span class="sxs-lookup"><span data-stu-id="049b3-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-126">Contiene el nombre del chip del adaptador.</span><span class="sxs-lookup"><span data-stu-id="049b3-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="049b3-127">Ejemplo: S3</span><span class="sxs-lookup"><span data-stu-id="049b3-127">Example: s3</span></span>

<span data-ttu-id="049b3-128">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-129">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="049b3-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-132">Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="049b3-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-133">Especifica el nombre del fabricante del adaptador.</span><span class="sxs-lookup"><span data-stu-id="049b3-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="049b3-134">Este nombre se puede usar para comparar la compatibilidad de este dispositivo con las necesidades del sistema.</span><span class="sxs-lookup"><span data-stu-id="049b3-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="049b3-135">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-136">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="049b3-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-139">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| DACType")</span><span class="sxs-lookup"><span data-stu-id="049b3-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-140">Indica el nombre del chip digital a analógico (DAC) utilizado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="049b3-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="049b3-141">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-142">**AdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="049b3-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-145">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="049b3-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-146">Contiene una descripción o el nombre descriptivo del adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="049b3-147">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-148">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="049b3-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-151">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| Memory"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="049b3-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-152">Indica el tamaño de la memoria del adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="049b3-153">Ejemplo: 16777216</span><span class="sxs-lookup"><span data-stu-id="049b3-153">Example: 16777216</span></span>

<span data-ttu-id="049b3-154">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="049b3-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-158">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| Descripción de hardware \\ \\ \\ \\ del sistema \\ \\ DisplayController \\ \\ 0 \\ \\ identificador")</span><span class="sxs-lookup"><span data-stu-id="049b3-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-159">Indica el tipo de adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="049b3-160">Juego de caracteres: alfanumérico</span><span class="sxs-lookup"><span data-stu-id="049b3-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="049b3-161">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-162">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="049b3-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-165">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="049b3-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-166">Indica el número real de bits por píxel que representa la presentación.</span><span class="sxs-lookup"><span data-stu-id="049b3-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="049b3-167">Se puede escalar a la configuración de vídeo actual (representada por la propiedad ActualColorResolution) del usuario.</span><span class="sxs-lookup"><span data-stu-id="049b3-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="049b3-168">Ejemplo: 8</span><span class="sxs-lookup"><span data-stu-id="049b3-168">Example: 8</span></span>

<span data-ttu-id="049b3-169">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-170">**Caption**</span><span class="sxs-lookup"><span data-stu-id="049b3-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-173">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="049b3-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="049b3-174">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="049b3-174">Short textual description of the current object.</span></span>

<span data-ttu-id="049b3-175">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-176">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="049b3-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-179">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| funciones de contexto de dispositivo \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| planos")</span><span class="sxs-lookup"><span data-stu-id="049b3-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-180">Indica el número actual de planos de color usados en la pantalla de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="049b3-181">Un plano de color es otra manera de representar colores de píxeles; en lugar de asignar un único valor RGB a cada píxel, los planos de color separan el gráfico en cada uno de los componentes de color primario (rojo verde azul) y los almacenan en sus propios planos.</span><span class="sxs-lookup"><span data-stu-id="049b3-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="049b3-182">Esto permite mayores profundidades de color en sistemas de vídeo de 8 y 16 bits.</span><span class="sxs-lookup"><span data-stu-id="049b3-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="049b3-183">Los sistemas de gráficos actuales tienen el bitwidth lo suficientemente grande como para almacenar información de profundidad de color, lo que hace que solo sea necesario un plano de color.</span><span class="sxs-lookup"><span data-stu-id="049b3-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="049b3-184">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="049b3-184">Example: 1</span></span>

<span data-ttu-id="049b3-185">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-186">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="049b3-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-189">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="049b3-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-190">Indica el número de índices de color de una tabla de colores para una pantalla de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="049b3-191">Esta propiedad se usa si el dispositivo tiene una profundidad de color de no más de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="049b3-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="049b3-192">En el caso de los dispositivos con mayor profundidad de color, se devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="049b3-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="049b3-193">Ejemplo: 256</span><span class="sxs-lookup"><span data-stu-id="049b3-193">Example: 256</span></span>

<span data-ttu-id="049b3-194">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-195">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="049b3-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="049b3-198">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="049b3-198">Textual description of the current object.</span></span>

<span data-ttu-id="049b3-199">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-200">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="049b3-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-203">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="049b3-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-204">Indica el número actual de lápices específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="049b3-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="049b3-205">Un valor de 0xFFFFFFFF significa que el dispositivo no admite lápices.</span><span class="sxs-lookup"><span data-stu-id="049b3-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="049b3-206">Los lápices se usan para dibujar líneas y los bordes de los objetos poligonales.</span><span class="sxs-lookup"><span data-stu-id="049b3-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="049b3-207">Ejemplo: 3</span><span class="sxs-lookup"><span data-stu-id="049b3-207">Example: 3</span></span>

<span data-ttu-id="049b3-208">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-209">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="049b3-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-210">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="049b3-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-212">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="049b3-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-213">Indica la fecha y la hora en que se instaló el controlador de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="049b3-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="049b3-214">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="049b3-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-216">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-218">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")</span><span class="sxs-lookup"><span data-stu-id="049b3-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-219">Indica el número actual de píxeles en la dirección horizontal (eje X) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="049b3-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="049b3-220">Ejemplo: 1024</span><span class="sxs-lookup"><span data-stu-id="049b3-220">Example: 1024</span></span>

<span data-ttu-id="049b3-221">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-222">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="049b3-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-225">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="049b3-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-226">Especifica la ruta de acceso al archivo. inf del controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="049b3-227">Ejemplo: C: \\ Windows \\ system32 \\ drivers</span><span class="sxs-lookup"><span data-stu-id="049b3-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="049b3-228">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-229">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="049b3-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-232">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="049b3-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-233">Indica la sección del archivo. inf en la que reside la información de vídeo de Win32.</span><span class="sxs-lookup"><span data-stu-id="049b3-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="049b3-234">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-235">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="049b3-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-238">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| DRV")</span><span class="sxs-lookup"><span data-stu-id="049b3-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-239">Indica el nombre del controlador de vídeo instalado.</span><span class="sxs-lookup"><span data-stu-id="049b3-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="049b3-240">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-241">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="049b3-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-244">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="049b3-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-245">Indica el nombre del fabricante del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="049b3-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="049b3-246">Ejemplo: NEC</span><span class="sxs-lookup"><span data-stu-id="049b3-246">Example: NEC</span></span>

<span data-ttu-id="049b3-247">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-248">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="049b3-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-251">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| Descripción de hardware \\ \\ \\ \\ del sistema \\ \\ MonitorPeripheral \\ \\ 0 \| identificador")</span><span class="sxs-lookup"><span data-stu-id="049b3-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-252">Indica el nombre del modelo del dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="049b3-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="049b3-253">Ejemplo: NEC 5FGp</span><span class="sxs-lookup"><span data-stu-id="049b3-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="049b3-254">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-255">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="049b3-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-258">Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="049b3-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-259">Contiene un nombre de identificación para la clase de configuración de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="049b3-260">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-261">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="049b3-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-262">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-264">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")</span><span class="sxs-lookup"><span data-stu-id="049b3-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-265">Indica el número de píxeles por pulgada lógica a lo largo del eje X (dirección horizontal) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="049b3-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="049b3-266">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-267">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="049b3-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-268">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-270">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")</span><span class="sxs-lookup"><span data-stu-id="049b3-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-271">Indica el número de píxeles por pulgada lógica a lo largo del eje Y (dirección vertical) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="049b3-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="049b3-272">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-273">**Frecuencia**</span><span class="sxs-lookup"><span data-stu-id="049b3-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-274">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-276">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")</span><span class="sxs-lookup"><span data-stu-id="049b3-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-277">Indica la frecuencia de actualización de la configuración de vídeo.</span><span class="sxs-lookup"><span data-stu-id="049b3-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="049b3-278">Un valor de 0 o 1 indica que se está usando una tasa predeterminada.</span><span class="sxs-lookup"><span data-stu-id="049b3-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="049b3-279">Ejemplo: 72</span><span class="sxs-lookup"><span data-stu-id="049b3-279">Example: 72</span></span>

<span data-ttu-id="049b3-280">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-281">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="049b3-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-284">Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. entrelazado")</span><span class="sxs-lookup"><span data-stu-id="049b3-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-285">Indica si el dispositivo de pantalla está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="049b3-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="049b3-286">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="049b3-287">**No entrelazado** ("no entrelazado")</span><span class="sxs-lookup"><span data-stu-id="049b3-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="049b3-288">**Entrelazado** ("entrelazado")</span><span class="sxs-lookup"><span data-stu-id="049b3-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="049b3-289">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="049b3-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-290">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-292">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")</span><span class="sxs-lookup"><span data-stu-id="049b3-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-293">Especifica el alto de la pantalla física.</span><span class="sxs-lookup"><span data-stu-id="049b3-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="049b3-294">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-295">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="049b3-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-296">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-298">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")</span><span class="sxs-lookup"><span data-stu-id="049b3-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-299">Especifica el ancho de la pantalla física.</span><span class="sxs-lookup"><span data-stu-id="049b3-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="049b3-300">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="049b3-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="049b3-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-304">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="049b3-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="049b3-305">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="049b3-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="049b3-306">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-307">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="049b3-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-308">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-310">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")</span><span class="sxs-lookup"><span data-stu-id="049b3-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-311">Hace referencia a el número actual de entradas de índice de color reservadas para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="049b3-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="049b3-312">Este valor solo es válido para la configuración de pantalla que usa una paleta indizada.</span><span class="sxs-lookup"><span data-stu-id="049b3-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="049b3-313">Las paletas indizadas no se utilizan para profundidades de color de más de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="049b3-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="049b3-314">Si la profundidad de color tiene más de 8 bits por píxel, este valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="049b3-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="049b3-315">Ejemplo: 20</span><span class="sxs-lookup"><span data-stu-id="049b3-315">Example: 20</span></span>

<span data-ttu-id="049b3-316">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="049b3-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="049b3-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="049b3-318">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="049b3-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="049b3-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="049b3-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="049b3-320">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")</span><span class="sxs-lookup"><span data-stu-id="049b3-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="049b3-321">Indica el número actual de píxeles en la dirección vertical (eje Y) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="049b3-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="049b3-322">Ejemplo: 768</span><span class="sxs-lookup"><span data-stu-id="049b3-322">Example: 768</span></span>

<span data-ttu-id="049b3-323">Esta propiedad ha quedado en desuso en favor de las propiedades correspondientes contenidas en el [**\_ videocontrolador de Win32**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) y//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="049b3-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="049b3-324">Requisitos</span><span class="sxs-lookup"><span data-stu-id="049b3-324">Requirements</span></span>



| <span data-ttu-id="049b3-325">Requisito</span><span class="sxs-lookup"><span data-stu-id="049b3-325">Requirement</span></span> | <span data-ttu-id="049b3-326">Value</span><span class="sxs-lookup"><span data-stu-id="049b3-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="049b3-327">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="049b3-327">Minimum supported client</span></span><br/> | <span data-ttu-id="049b3-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="049b3-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="049b3-329">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="049b3-329">Minimum supported server</span></span><br/> | <span data-ttu-id="049b3-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="049b3-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="049b3-331">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="049b3-331">Namespace</span></span><br/>                | <span data-ttu-id="049b3-332">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="049b3-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="049b3-333">MOF</span><span class="sxs-lookup"><span data-stu-id="049b3-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="049b3-334"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="049b3-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="049b3-335">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="049b3-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="049b3-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="049b3-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="049b3-337">Vea también</span><span class="sxs-lookup"><span data-stu-id="049b3-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="049b3-338">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="049b3-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
