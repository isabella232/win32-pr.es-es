---
description: La \_ clase WMI DisplayControllerConfiguration de Win32 representa la información de configuración del adaptador de vídeo de un equipo que ejecuta Windows.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Win32_DisplayControllerConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153355"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="60b04-103">\_Clase Win32 DisplayControllerConfiguration</span><span class="sxs-lookup"><span data-stu-id="60b04-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="60b04-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DisplayControllerConfiguration de Win32** representa la información de configuración del adaptador de vídeo de un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="60b04-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="60b04-105">Esta clase está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="60b04-105">This class is obsolete.</span></span> <span data-ttu-id="60b04-106">En lugar de esta clase, debe utilizar las propiedades de las clases [**\_ videocontroller**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)y [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) de Win32.</span><span class="sxs-lookup"><span data-stu-id="60b04-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="60b04-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="60b04-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="60b04-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="60b04-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b04-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60b04-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="60b04-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="60b04-110">Members</span></span>

<span data-ttu-id="60b04-111">La **clase \_ DisplayControllerConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60b04-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="60b04-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60b04-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60b04-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60b04-113">Properties</span></span>

<span data-ttu-id="60b04-114">La **clase \_ DisplayControllerConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60b04-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60b04-115">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="60b04-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-118">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="60b04-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-119">El número de bits que se usa para representar el color de esta configuración o los bits de cada píxel.</span><span class="sxs-lookup"><span data-stu-id="60b04-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="60b04-120">Ejemplo: 8</span><span class="sxs-lookup"><span data-stu-id="60b04-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="60b04-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60b04-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b04-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-124">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="60b04-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="60b04-125">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="60b04-125">Short textual description of the current object.</span></span>

<span data-ttu-id="60b04-126">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="60b04-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b04-127">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="60b04-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-130">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api de \| funciones de contexto de dispositivo \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| planos")</span><span class="sxs-lookup"><span data-stu-id="60b04-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-131">Número actual de planos de color usados en la configuración de pantalla.</span><span class="sxs-lookup"><span data-stu-id="60b04-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="60b04-132">Un plano de color es otra manera de representar colores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="60b04-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="60b04-133">En lugar de asignar un único valor RGB a cada píxel, los planos de color separan el gráfico en cada uno de los componentes de color primario (rojo, verde, azul) y los almacena en sus propios planos.</span><span class="sxs-lookup"><span data-stu-id="60b04-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="60b04-134">Esto permite mayores profundidades de color en sistemas de vídeo de 8 y 16 bits.</span><span class="sxs-lookup"><span data-stu-id="60b04-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="60b04-135">Los sistemas de gráficos actuales tienen el bitwidth lo suficientemente grande como para almacenar información de profundidad de color, lo que significa que solo se necesita un plano de color.</span><span class="sxs-lookup"><span data-stu-id="60b04-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="60b04-136">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="60b04-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="60b04-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60b04-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b04-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60b04-140">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="60b04-140">Textual description of the current object.</span></span>

<span data-ttu-id="60b04-141">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="60b04-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b04-142">**DeviceEntriesInAColorTable**</span><span class="sxs-lookup"><span data-stu-id="60b04-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-145">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="60b04-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-146">Número de índices de color en una tabla de colores de un dispositivo de pantalla (si el dispositivo tiene una profundidad de color de no más de 8 bits por píxel).</span><span class="sxs-lookup"><span data-stu-id="60b04-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="60b04-147">En el caso de los dispositivos con mayor profundidad de color, se devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="60b04-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="60b04-148">Ejemplo: 256</span><span class="sxs-lookup"><span data-stu-id="60b04-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="60b04-149">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="60b04-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-152">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="60b04-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-153">Número actual de lápices específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60b04-153">Current number of device-specific pens.</span></span> <span data-ttu-id="60b04-154">Un valor de 0xFFFFFFFF significa que el dispositivo no admite lápices.</span><span class="sxs-lookup"><span data-stu-id="60b04-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="60b04-155">Los lápices son propiedades lógicas que puede asignar el controlador de pantalla para mostrar los dispositivos y que se usan para dibujar líneas, bordes de polígonos y texto.</span><span class="sxs-lookup"><span data-stu-id="60b04-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="60b04-156">Ejemplo: 3</span><span class="sxs-lookup"><span data-stu-id="60b04-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="60b04-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="60b04-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-158">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-160">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de contexto de dispositivo \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles")</span><span class="sxs-lookup"><span data-stu-id="60b04-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-161">Número actual de píxeles en la dirección horizontal (eje x) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="60b04-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="60b04-162">Ejemplo: 1024</span><span class="sxs-lookup"><span data-stu-id="60b04-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="60b04-163">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="60b04-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b04-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-166">Calificadores: [**desusado**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="60b04-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-167">Nombre del adaptador usado en esta configuración.</span><span class="sxs-lookup"><span data-stu-id="60b04-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="60b04-168">**Frecuencia**</span><span class="sxs-lookup"><span data-stu-id="60b04-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-169">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="60b04-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-171">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios")</span><span class="sxs-lookup"><span data-stu-id="60b04-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-172">Frecuencia de actualización del adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="60b04-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="60b04-173">Un valor de 0 (cero) o 1 (uno) indica que se está usando una tasa predeterminada.</span><span class="sxs-lookup"><span data-stu-id="60b04-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="60b04-174">Un valor de-1 indica que se está usando una tasa óptima.</span><span class="sxs-lookup"><span data-stu-id="60b04-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="60b04-175">Ejemplo: 72</span><span class="sxs-lookup"><span data-stu-id="60b04-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="60b04-176">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="60b04-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-179">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="60b04-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-180">Número actual de entradas de índice de color reservadas para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="60b04-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="60b04-181">Este valor solo es válido para la configuración de pantalla que usa una paleta indizada.</span><span class="sxs-lookup"><span data-stu-id="60b04-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="60b04-182">Las paletas indizadas no se utilizan para profundidades de color de más de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="60b04-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="60b04-183">Si la profundidad de color tiene más de 8 bits por píxel, este valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="60b04-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="60b04-184">Ejemplo: 20</span><span class="sxs-lookup"><span data-stu-id="60b04-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="60b04-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="60b04-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b04-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-188">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="60b04-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="60b04-189">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="60b04-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="60b04-190">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="60b04-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="60b04-191">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="60b04-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-192">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-194">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones de contexto de dispositivo inesperados win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="60b04-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-195">Número actual de entradas de índice de color reservadas para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="60b04-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="60b04-196">Este valor solo es válido para la configuración de pantalla que usa una paleta indizada.</span><span class="sxs-lookup"><span data-stu-id="60b04-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="60b04-197">Las paletas indizadas no se utilizan para profundidades de color de más de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="60b04-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="60b04-198">Si la profundidad de color tiene más de 8 bits por píxel, este valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="60b04-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="60b04-199">Ejemplo: 20</span><span class="sxs-lookup"><span data-stu-id="60b04-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="60b04-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="60b04-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-201">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60b04-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-203">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de contexto de dispositivo \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles")</span><span class="sxs-lookup"><span data-stu-id="60b04-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-204">Número actual de píxeles en la dirección vertical (eje y) de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="60b04-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="60b04-205">Ejemplo: 768</span><span class="sxs-lookup"><span data-stu-id="60b04-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="60b04-206">**Modo**</span><span class="sxs-lookup"><span data-stu-id="60b04-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60b04-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60b04-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60b04-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60b04-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60b04-209">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="60b04-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="60b04-210">Descripción legible por el usuario de la configuración de color y resolución de pantalla actual de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="60b04-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="60b04-211">Ejemplo: "1024 768 con colores 256"</span><span class="sxs-lookup"><span data-stu-id="60b04-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b04-212">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60b04-212">Remarks</span></span>

<span data-ttu-id="60b04-213">La **clase \_ DisplayControllerConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="60b04-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60b04-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b04-214">Requirements</span></span>



| <span data-ttu-id="60b04-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b04-215">Requirement</span></span> | <span data-ttu-id="60b04-216">Value</span><span class="sxs-lookup"><span data-stu-id="60b04-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b04-217">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b04-217">Minimum supported client</span></span><br/> | <span data-ttu-id="60b04-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60b04-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60b04-219">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60b04-219">Minimum supported server</span></span><br/> | <span data-ttu-id="60b04-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60b04-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60b04-221">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60b04-221">Namespace</span></span><br/>                | <span data-ttu-id="60b04-222">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="60b04-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60b04-223">MOF</span><span class="sxs-lookup"><span data-stu-id="60b04-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b04-224"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60b04-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b04-225">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60b04-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b04-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b04-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b04-227">Vea también</span><span class="sxs-lookup"><span data-stu-id="60b04-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b04-228">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="60b04-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="60b04-229">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="60b04-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

