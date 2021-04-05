---
description: La \_ clase WMI PrinterConfiguration de Win32 representa la configuración de un dispositivo de impresora. Esto incluye capacidades como resolución, color, fuentes y orientación.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Win32_PrinterConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000723"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="db24c-104">\_Clase Win32 PrinterConfiguration</span><span class="sxs-lookup"><span data-stu-id="db24c-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="db24c-105">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterConfiguration de Win32** representa la configuración de un dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="db24c-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="db24c-106">Esto incluye capacidades como resolución, color, fuentes y orientación.</span><span class="sxs-lookup"><span data-stu-id="db24c-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="db24c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="db24c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="db24c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="db24c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="db24c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db24c-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="db24c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="db24c-110">Members</span></span>

<span data-ttu-id="db24c-111">La **clase \_ PrinterConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="db24c-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="db24c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db24c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db24c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db24c-113">Properties</span></span>

<span data-ttu-id="db24c-114">La **clase \_ PrinterConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="db24c-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db24c-115">**BitsPerPel**</span><span class="sxs-lookup"><span data-stu-id="db24c-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-118">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-119">Número de bits utilizados para representar el color de esta configuración (los bits por píxel).</span><span class="sxs-lookup"><span data-stu-id="db24c-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="db24c-120">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="db24c-120">This property is obsolete.</span></span> <span data-ttu-id="db24c-121">En su lugar, use las propiedades de las clases [**\_ videocontroller**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) de Win32 para determinar cómo se representa el color.</span><span class="sxs-lookup"><span data-stu-id="db24c-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="db24c-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-125">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="db24c-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-126">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="db24c-126">Short textual description of the current object.</span></span>

<span data-ttu-id="db24c-127">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="db24c-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="db24c-128">**Intercalar**</span><span class="sxs-lookup"><span data-stu-id="db24c-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="db24c-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-131">Si **es true**, se deben intercalar las páginas que se imprimen.</span><span class="sxs-lookup"><span data-stu-id="db24c-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="db24c-132">La intercalación es imprimir todo el documento antes de imprimir la siguiente copia, en lugar de imprimir cada página del documento el número de veces que se requiera.</span><span class="sxs-lookup"><span data-stu-id="db24c-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="db24c-133">Esta propiedad se omite a menos que el controlador de impresora indique la compatibilidad con la intercalación.</span><span class="sxs-lookup"><span data-stu-id="db24c-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-134">**Color**</span><span class="sxs-lookup"><span data-stu-id="db24c-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-137">Color del documento.</span><span class="sxs-lookup"><span data-stu-id="db24c-137">Color of the document.</span></span> <span data-ttu-id="db24c-138">Algunas impresoras de color tienen la capacidad de imprimir con True Black en lugar de una combinación de cian, magenta y amarillo (CMY).</span><span class="sxs-lookup"><span data-stu-id="db24c-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="db24c-139">Esto normalmente crea texto más oscuro y más nítido para los documentos.</span><span class="sxs-lookup"><span data-stu-id="db24c-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="db24c-140">Esta opción solo es útil para las impresoras de color que admiten la impresión en negro real.</span><span class="sxs-lookup"><span data-stu-id="db24c-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="db24c-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="db24c-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-142">Monocromo (verdadero negro)</span><span class="sxs-lookup"><span data-stu-id="db24c-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="db24c-143"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="db24c-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-144">Color</span><span class="sxs-lookup"><span data-stu-id="db24c-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-145">**Copias**</span><span class="sxs-lookup"><span data-stu-id="db24c-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-148">Número de copias que se van a imprimir.</span><span class="sxs-lookup"><span data-stu-id="db24c-148">Number of copies to be printed.</span></span> <span data-ttu-id="db24c-149">El controlador de impresora debe admitir la impresión de copias de varias páginas.</span><span class="sxs-lookup"><span data-stu-id="db24c-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="db24c-150">Ejemplo: 2</span><span class="sxs-lookup"><span data-stu-id="db24c-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="db24c-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db24c-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-154">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="db24c-154">Textual description of the current object.</span></span>

<span data-ttu-id="db24c-155">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="db24c-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="db24c-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="db24c-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-159">Nombre descriptivo de la impresora.</span><span class="sxs-lookup"><span data-stu-id="db24c-159">Friendly name of the printer.</span></span> <span data-ttu-id="db24c-160">Este nombre es único para el tipo de impresora y se puede truncar debido a las limitaciones de la cadena de la que se deriva.</span><span class="sxs-lookup"><span data-stu-id="db24c-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="db24c-161">Ejemplo: "PCL/HP LaserJet"</span><span class="sxs-lookup"><span data-stu-id="db24c-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="db24c-162">**DisplayFlags**</span><span class="sxs-lookup"><span data-stu-id="db24c-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-163">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-165">Indica si el dispositivo de pantalla es de color o monocromo y si el tipo de digitalización no es entrelazado o entrelazado.</span><span class="sxs-lookup"><span data-stu-id="db24c-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="db24c-166">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="db24c-166">This property is obsolete.</span></span> <span data-ttu-id="db24c-167">En su lugar, use las propiedades de presentación, como la propiedad **DisplayType** de la clase **\_ DesktopMonitor de Win32** .</span><span class="sxs-lookup"><span data-stu-id="db24c-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-168">**DisplayFrequency**</span><span class="sxs-lookup"><span data-stu-id="db24c-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-169">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-171">Muestra la frecuencia de actualización vertical.</span><span class="sxs-lookup"><span data-stu-id="db24c-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="db24c-172">La frecuencia de actualización de un monitor es el número de veces que se vuelve a dibujar la pantalla por segundo (frecuencia).</span><span class="sxs-lookup"><span data-stu-id="db24c-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="db24c-173">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="db24c-173">This property is obsolete.</span></span> <span data-ttu-id="db24c-174">En su lugar, use las propiedades de la clase [**Win32 \_ videocontroller**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="db24c-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-175">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="db24c-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-176">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-178">Tipo de interpolación de la impresora.</span><span class="sxs-lookup"><span data-stu-id="db24c-178">Dither type of the printer.</span></span> <span data-ttu-id="db24c-179">Esta propiedad puede asumir valores predefinidos de 1 a 5 o valores definidos por el controlador de 6 a 256.</span><span class="sxs-lookup"><span data-stu-id="db24c-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="db24c-180">La interpolación de líneas de arte es un método de interpolación especial que genera bordes bien definidos entre las escalas de color negro, blanco y gris.</span><span class="sxs-lookup"><span data-stu-id="db24c-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="db24c-181">No es adecuado para las imágenes que incluyen graduaciones continuas de intensidad y matiz, como fotografías digitalizadas.</span><span class="sxs-lookup"><span data-stu-id="db24c-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="db24c-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="db24c-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-183">Sin interpolación</span><span class="sxs-lookup"><span data-stu-id="db24c-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="db24c-184"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="db24c-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-185">Pincel grueso</span><span class="sxs-lookup"><span data-stu-id="db24c-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="db24c-186"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="db24c-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-187">Pincel fino</span><span class="sxs-lookup"><span data-stu-id="db24c-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="db24c-188"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="db24c-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-189">Arte de líneas</span><span class="sxs-lookup"><span data-stu-id="db24c-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="db24c-190"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="db24c-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-191">Escala de grises</span><span class="sxs-lookup"><span data-stu-id="db24c-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-192">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="db24c-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-195">Número de versión del controlador de impresora basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="db24c-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="db24c-196">El fabricante del controlador crea y mantiene los números de versión.</span><span class="sxs-lookup"><span data-stu-id="db24c-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-197">**Dúplex**</span><span class="sxs-lookup"><span data-stu-id="db24c-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-198">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="db24c-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-200">Si es **true**, la impresión se realiza en ambos lados.</span><span class="sxs-lookup"><span data-stu-id="db24c-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="db24c-201">Si es **false**, la impresión se realiza solo en un lado del medio.</span><span class="sxs-lookup"><span data-stu-id="db24c-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-202">**FormName**</span><span class="sxs-lookup"><span data-stu-id="db24c-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-205">No se admite.</span><span class="sxs-lookup"><span data-stu-id="db24c-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="db24c-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-207">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-209">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (puntos por pulgada)</span><span class="sxs-lookup"><span data-stu-id="db24c-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-210">Resolución de impresión en puntos por pulgada a lo largo del eje x (ancho) del trabajo de impresión (similar a la propiedad **XResolution** obsoleta).</span><span class="sxs-lookup"><span data-stu-id="db24c-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="db24c-211">Este valor solo se establece cuando la propiedad **PrintQuality** de esta clase es positiva.</span><span class="sxs-lookup"><span data-stu-id="db24c-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-212">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="db24c-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-213">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-215">Valor específico de uno de los tres métodos de coincidencia de color posibles (denominados intenciones) que se debe usar de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="db24c-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="db24c-216">Las aplicaciones ICM establecen intenciones mediante el uso de las funciones de ICM.</span><span class="sxs-lookup"><span data-stu-id="db24c-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="db24c-217">Esta propiedad puede asumir valores predefinidos de 1 a 3 o valores definidos por el controlador de 4 a 256.</span><span class="sxs-lookup"><span data-stu-id="db24c-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="db24c-218">Las aplicaciones no ICM pueden utilizar este valor para determinar cómo trata la impresora los trabajos de impresión en color.</span><span class="sxs-lookup"><span data-stu-id="db24c-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="db24c-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="db24c-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-220">Saturación</span><span class="sxs-lookup"><span data-stu-id="db24c-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="db24c-221"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="db24c-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-222">Compare</span><span class="sxs-lookup"><span data-stu-id="db24c-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="db24c-223"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="db24c-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-224">Color exacto</span><span class="sxs-lookup"><span data-stu-id="db24c-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-225">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="db24c-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-226">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-228">Cómo se controla ICM.</span><span class="sxs-lookup"><span data-stu-id="db24c-228">How ICM is handled.</span></span> <span data-ttu-id="db24c-229">En el caso de una aplicación no ICM, esta propiedad determina si ICM está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="db24c-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="db24c-230">En el caso de las aplicaciones ICM, el sistema examina esta propiedad para determinar qué parte del sistema del equipo controla la compatibilidad con ICM.</span><span class="sxs-lookup"><span data-stu-id="db24c-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="db24c-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="db24c-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="db24c-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="db24c-233"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="db24c-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-234">Windows</span><span class="sxs-lookup"><span data-stu-id="db24c-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="db24c-235"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="db24c-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-236">Controlador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="db24c-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="db24c-237"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="db24c-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-238">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="db24c-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-239">**LogPixels**</span><span class="sxs-lookup"><span data-stu-id="db24c-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-240">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-242">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-243">Número de píxeles por pulgada lógica.</span><span class="sxs-lookup"><span data-stu-id="db24c-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="db24c-244">Esta propiedad obsoleta solo es válida con dispositivos que funcionan con píxeles, lo que excluye dispositivos como las impresoras.</span><span class="sxs-lookup"><span data-stu-id="db24c-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="db24c-245">No hay ningún valor de reemplazo que se aplique a las impresoras.</span><span class="sxs-lookup"><span data-stu-id="db24c-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-246">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="db24c-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-247">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-249">Tipo de medio en el que se imprime la impresora.</span><span class="sxs-lookup"><span data-stu-id="db24c-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="db24c-250">La propiedad se puede establecer en un valor predefinido o un valor definido por el controlador mayor o igual que 256.</span><span class="sxs-lookup"><span data-stu-id="db24c-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="db24c-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="db24c-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-252">Estándar</span><span class="sxs-lookup"><span data-stu-id="db24c-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="db24c-253"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="db24c-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-254">Transparencia</span><span class="sxs-lookup"><span data-stu-id="db24c-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="db24c-255"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="db24c-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-256">Fotográfico</span><span class="sxs-lookup"><span data-stu-id="db24c-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-257">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="db24c-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-260">Calificadores: [**clave**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="db24c-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-261">Nombre de la impresora a la que está asociada esta configuración.</span><span class="sxs-lookup"><span data-stu-id="db24c-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="db24c-262">Este valor coincide con la propiedad **Name** de la instancia de [**\_ impresora Win32**](win32-printer.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="db24c-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-263">**Orientación**</span><span class="sxs-lookup"><span data-stu-id="db24c-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-264">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-266">Orientación de impresión del papel.</span><span class="sxs-lookup"><span data-stu-id="db24c-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="db24c-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="db24c-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-268">Vertical</span><span class="sxs-lookup"><span data-stu-id="db24c-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="db24c-269"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="db24c-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-270">Horizontal</span><span class="sxs-lookup"><span data-stu-id="db24c-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-271">**PaperLength**</span><span class="sxs-lookup"><span data-stu-id="db24c-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-272">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-274">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimas de milímetro)</span><span class="sxs-lookup"><span data-stu-id="db24c-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-275">Longitud del papel.</span><span class="sxs-lookup"><span data-stu-id="db24c-275">Length of the paper.</span></span> <span data-ttu-id="db24c-276">Para determinar el tamaño del papel en pulgadas, divida este valor por 254.</span><span class="sxs-lookup"><span data-stu-id="db24c-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="db24c-277">Ejemplo: 2794</span><span class="sxs-lookup"><span data-stu-id="db24c-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="db24c-278">**PaperSize**</span><span class="sxs-lookup"><span data-stu-id="db24c-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-281">Tamaño del papel.</span><span class="sxs-lookup"><span data-stu-id="db24c-281">Size of the paper.</span></span> <span data-ttu-id="db24c-282">Los tamaños posibles se encuentran en la propiedad **PaperSizesSupported** de la clase [**de \_ impresora Win32**](win32-printer.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="db24c-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="db24c-283">Ejemplo: "A4 o letra".</span><span class="sxs-lookup"><span data-stu-id="db24c-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="db24c-284">**PaperWidth**</span><span class="sxs-lookup"><span data-stu-id="db24c-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-287">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimas de milímetro)</span><span class="sxs-lookup"><span data-stu-id="db24c-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-288">Ancho del papel.</span><span class="sxs-lookup"><span data-stu-id="db24c-288">Width of the paper.</span></span> <span data-ttu-id="db24c-289">Para determinar el tamaño del papel en pulgadas, divida este valor por 254.</span><span class="sxs-lookup"><span data-stu-id="db24c-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="db24c-290">Ejemplo: 2159</span><span class="sxs-lookup"><span data-stu-id="db24c-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="db24c-291">**PelsHeight**</span><span class="sxs-lookup"><span data-stu-id="db24c-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-292">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-294">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-295">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="db24c-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-296">**PelsWidth**</span><span class="sxs-lookup"><span data-stu-id="db24c-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-297">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-299">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-300">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="db24c-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="db24c-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-302">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-304">Uno de los cuatro niveles de calidad del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="db24c-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="db24c-305">Si se especifica un valor positivo, la calidad se mide en puntos por pulgada.</span><span class="sxs-lookup"><span data-stu-id="db24c-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="db24c-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="db24c-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-307">Borrador</span><span class="sxs-lookup"><span data-stu-id="db24c-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="db24c-308"><span id="-2"></span>**-2**</span><span class="sxs-lookup"><span data-stu-id="db24c-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-309">Bajo</span><span class="sxs-lookup"><span data-stu-id="db24c-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="db24c-310"><span id="-3"></span>**-3**</span><span class="sxs-lookup"><span data-stu-id="db24c-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-311">Media</span><span class="sxs-lookup"><span data-stu-id="db24c-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="db24c-312"><span id="-4"></span>**-4**</span><span class="sxs-lookup"><span data-stu-id="db24c-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="db24c-313">Alto</span><span class="sxs-lookup"><span data-stu-id="db24c-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-314">**Escala**</span><span class="sxs-lookup"><span data-stu-id="db24c-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-317">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (porcentaje)</span><span class="sxs-lookup"><span data-stu-id="db24c-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-318">Factor por el que se va a escalar la salida impresa.</span><span class="sxs-lookup"><span data-stu-id="db24c-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="db24c-319">Por ejemplo, una escala de 75 reduce la salida de impresión a 3/4 su alto y ancho originales.</span><span class="sxs-lookup"><span data-stu-id="db24c-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="db24c-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db24c-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-323">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="db24c-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-324">Identificador por el que se conoce el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="db24c-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="db24c-325">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="db24c-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="db24c-326">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="db24c-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-327">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-329">Número de versión de los datos de inicialización del dispositivo asociado a la impresora basada en Windows.</span><span class="sxs-lookup"><span data-stu-id="db24c-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-330">**TTOption**</span><span class="sxs-lookup"><span data-stu-id="db24c-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-331">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db24c-333">Indica cómo se deben imprimir las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="db24c-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="db24c-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Mapa de bits** (1)</span><span class="sxs-lookup"><span data-stu-id="db24c-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db24c-335">Imprime las fuentes TrueType como gráficos.</span><span class="sxs-lookup"><span data-stu-id="db24c-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="db24c-336">Esta es la acción predeterminada para las impresoras matriciales.</span><span class="sxs-lookup"><span data-stu-id="db24c-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="db24c-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Descargar** (2)</span><span class="sxs-lookup"><span data-stu-id="db24c-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db24c-338">Descarga fuentes TrueType como fuentes flexibles.</span><span class="sxs-lookup"><span data-stu-id="db24c-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="db24c-339">Esta es la acción predeterminada para las impresoras que usan el lenguaje de control de impresoras (PCL).</span><span class="sxs-lookup"><span data-stu-id="db24c-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="db24c-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span><span class="sxs-lookup"><span data-stu-id="db24c-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db24c-341">Sustituye las fuentes del dispositivo por fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="db24c-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="db24c-342">Esta es la acción predeterminada para las impresoras PostScript.</span><span class="sxs-lookup"><span data-stu-id="db24c-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db24c-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="db24c-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-344">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-346">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (puntos por pulgada)</span><span class="sxs-lookup"><span data-stu-id="db24c-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-347">Resolución de impresión a lo largo del eje y (alto) del trabajo de impresión (similar a la propiedad **YResolution** obsoleta).</span><span class="sxs-lookup"><span data-stu-id="db24c-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="db24c-348">Este valor solo se establece cuando la propiedad **PrintQuality** de esta clase es positiva.</span><span class="sxs-lookup"><span data-stu-id="db24c-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-349">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="db24c-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-350">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-352">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-353">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="db24c-353">This property is obsolete.</span></span> <span data-ttu-id="db24c-354">En su lugar, use la propiedad **HorizontalResolution** .</span><span class="sxs-lookup"><span data-stu-id="db24c-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="db24c-355">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="db24c-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db24c-356">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db24c-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db24c-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db24c-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db24c-358">Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="db24c-359">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="db24c-359">This property is obsolete.</span></span> <span data-ttu-id="db24c-360">En su lugar, use la propiedad **VerticalResolution** .</span><span class="sxs-lookup"><span data-stu-id="db24c-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db24c-361">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db24c-361">Remarks</span></span>

<span data-ttu-id="db24c-362">La **clase \_ PrinterConfiguration de Win32** se deriva de la [**\_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="db24c-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="db24c-363">**Información general**</span><span class="sxs-lookup"><span data-stu-id="db24c-363">**Overview**</span></span>

<span data-ttu-id="db24c-364">Para poder determinar cómo distribuir y usar mejor los recursos de impresión, debe tener un conocimiento detallado de esos recursos.</span><span class="sxs-lookup"><span data-stu-id="db24c-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="db24c-365">Por ejemplo, el Departamento A solo puede tener tres impresoras comparadas con cinco impresoras del Departamento B. Sin embargo, si las impresoras del Departamento A pueden imprimir 20 páginas por minuto y las impresoras del Departamento B pueden imprimir solo 5 páginas por minuto, los usuarios del Departamento A realmente tienen más capacidad de impresión.</span><span class="sxs-lookup"><span data-stu-id="db24c-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="db24c-366">Sin conocer las capacidades detalladas de estas impresoras, podría concluir erróneamente que el Departamento A es corto en la capacidad de impresión y, por tanto, adquirir impresoras adicionales que acaben sin usarse.</span><span class="sxs-lookup"><span data-stu-id="db24c-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="db24c-367">WMI incluye dos clases, [**\_ impresora Win32**](win32-printer.md) y **\_ PrinterConfiguration Win32**, que se pueden usar para devolver información detallada sobre todas las impresoras instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="db24c-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="db24c-368">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="db24c-368">Examples</span></span>

<span data-ttu-id="db24c-369">En el ejemplo de código siguiente se recupera la información de la impresora.</span><span class="sxs-lookup"><span data-stu-id="db24c-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="db24c-370">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db24c-370">Requirements</span></span>



| <span data-ttu-id="db24c-371">Requisito</span><span class="sxs-lookup"><span data-stu-id="db24c-371">Requirement</span></span> | <span data-ttu-id="db24c-372">Value</span><span class="sxs-lookup"><span data-stu-id="db24c-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db24c-373">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db24c-373">Minimum supported client</span></span><br/> | <span data-ttu-id="db24c-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db24c-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="db24c-375">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db24c-375">Minimum supported server</span></span><br/> | <span data-ttu-id="db24c-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db24c-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="db24c-377">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="db24c-377">Namespace</span></span><br/>                | <span data-ttu-id="db24c-378">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="db24c-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="db24c-379">MOF</span><span class="sxs-lookup"><span data-stu-id="db24c-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db24c-380"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db24c-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="db24c-381">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db24c-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db24c-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db24c-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="db24c-383">Vea también</span><span class="sxs-lookup"><span data-stu-id="db24c-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db24c-384">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="db24c-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="db24c-385">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="db24c-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
