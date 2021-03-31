---
title: Personalizar los colores de la cinta de opciones
description: El marco de la cinta de opciones de Windows expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario de la cinta en tiempo de ejecución.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Cinta de Windows, personalizar colores
- Cinta, personalizar colores
- personalizar los colores de la cinta de opciones de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103789004"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="f299a-106">Personalizar los colores de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="f299a-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="f299a-107">El marco de la cinta de opciones de Windows expone un conjunto de propiedades de color que permiten a una aplicación personalizar la apariencia de varios elementos de la interfaz de usuario de la cinta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f299a-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="f299a-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="f299a-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f299a-109">Especificar los colores de la cinta</span><span class="sxs-lookup"><span data-stu-id="f299a-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="f299a-110">Convertir RGB en HSB</span><span class="sxs-lookup"><span data-stu-id="f299a-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="f299a-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f299a-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f299a-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="f299a-112">Introduction</span></span>

<span data-ttu-id="f299a-113">Las [claves de propiedad de marco](windowsribbon-reference-properties-framework.md) enumeradas en la tabla siguiente se usan para establecer el color de varios elementos de la interfaz de usuario en una aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="f299a-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="f299a-114">Estas propiedades permiten que el marco de cinta admita la personalización, los requisitos de identidad y las especificaciones de personalización de marca entre las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f299a-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="f299a-115">Color de la cinta</span><span class="sxs-lookup"><span data-stu-id="f299a-115">Ribbon Color</span></span>                     | <span data-ttu-id="f299a-116">Clave de propiedad de marco de trabajo</span><span class="sxs-lookup"><span data-stu-id="f299a-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f299a-117">Color de fondo</span><span class="sxs-lookup"><span data-stu-id="f299a-117">Background color</span></span>                 | [<span data-ttu-id="f299a-118">UI \_ PKEY \_ GlobalBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="f299a-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f299a-119">Color de resaltado (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="f299a-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="f299a-120">[Interfaz de usuario \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\* \* \* \* incluido en Windows 8 \* \*: \* \* [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) no se puede establecer independientemente de la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="f299a-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="f299a-121">Color del texto</span><span class="sxs-lookup"><span data-stu-id="f299a-121">Text color</span></span>                       | <span data-ttu-id="f299a-122">[Interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\* \* \* \* introducido en Windows 8 **:** los cambios en el valor predeterminado de la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) en Windows 8 podrían requerir un ajuste a la [interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) en aplicaciones de cinta diseñadas para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f299a-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="f299a-123">Especificar los colores de la cinta</span><span class="sxs-lookup"><span data-stu-id="f299a-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="f299a-124">El marco de la cinta de opciones usa un modelo de color Hue, saturación, luminosidad (HSB), que difiere de los espacios de colores de matiz, saturación, luminosidad (HSL) o Hue, saturación, valor (HSV) más comunes.</span><span class="sxs-lookup"><span data-stu-id="f299a-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="f299a-125">En concreto, B representa un nivel de brillo o luminosidad general en lugar de la luminosidad de un color determinado.</span><span class="sxs-lookup"><span data-stu-id="f299a-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="f299a-126">Para especificar el color de los elementos de la interfaz de usuario en el marco de cinta, una aplicación asigna valores HSB a cada una de las propiedades de color globales.</span><span class="sxs-lookup"><span data-stu-id="f299a-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="f299a-127">Estos valores se aplican de forma universal a todos los elementos de la cinta de opciones según lo requiera la aplicación de cinta (el marco no admite la asignación de valores HSB a elementos y controles individuales).</span><span class="sxs-lookup"><span data-stu-id="f299a-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="f299a-128">Introducido en Windows 8 \* \*: \* \*[UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) tiene asignado el mismo valor que la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="f299a-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="f299a-129">En la tabla siguiente se describen los parámetros HSB del marco de cinta.</span><span class="sxs-lookup"><span data-stu-id="f299a-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="f299a-130">Componente</span><span class="sxs-lookup"><span data-stu-id="f299a-130">Component</span></span>

<span data-ttu-id="f299a-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f299a-131">Description</span></span>

<span data-ttu-id="f299a-132">Valores ajustados\*</span><span class="sxs-lookup"><span data-stu-id="f299a-132">Adjusted Values\*</span></span>

<span data-ttu-id="f299a-133">Matiz (H)</span><span class="sxs-lookup"><span data-stu-id="f299a-133">Hue (H)</span></span>

<span data-ttu-id="f299a-134">El color de pigmento, o real, se identifica normalmente como un valor de un intervalo de circlular de 0 a 359 grados.</span><span class="sxs-lookup"><span data-stu-id="f299a-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="f299a-135">0 (rojo) a 255 (rojo)</span><span class="sxs-lookup"><span data-stu-id="f299a-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="f299a-136">Saturación (S)</span><span class="sxs-lookup"><span data-stu-id="f299a-136">Saturation (S)</span></span>

<span data-ttu-id="f299a-137">La pureza, o saturación, del color que se mide como un porcentaje del 0 al 100%.</span><span class="sxs-lookup"><span data-stu-id="f299a-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="f299a-138">0 (gris) a 255 (completamente saturado)</span><span class="sxs-lookup"><span data-stu-id="f299a-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="f299a-139">Brillo (B)</span><span class="sxs-lookup"><span data-stu-id="f299a-139">Brightness (B)</span></span>

<span data-ttu-id="f299a-140">Brillo o oscuridad general del color medido como porcentaje del 0 al 100%.</span><span class="sxs-lookup"><span data-stu-id="f299a-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="f299a-141">0 (oscuro) a 255 (claro)</span><span class="sxs-lookup"><span data-stu-id="f299a-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="f299a-142">\* El intervalo original de cada valor de parámetro se convierte en un intervalo de 0 a 255 para el marco.</span><span class="sxs-lookup"><span data-stu-id="f299a-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="f299a-143">Los valores HSB no identifican colores específicos.</span><span class="sxs-lookup"><span data-stu-id="f299a-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="f299a-144">En su lugar, la combinación de valores de propiedad HSB influye en cómo se ajustan entre sí los degradados de color a lo largo de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f299a-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="f299a-145">Al asignar valores HSB personalizados a la [interfaz de usuario \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) y a la interfaz de [usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), se recomienda que estos valores sean de contraste suficiente para garantizar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f299a-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="f299a-146">En concreto, el color del texto debe ser más oscuro que el sombreado más claro de la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f299a-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="f299a-147">Cuando sea necesario, el marco de trabajo ajusta automáticamente el valor HSB de la interfaz de usuario \_ PKEY \_ GlobalTextColor para proporcionar un contraste suficiente con cualquier sombreado de fondo o degradado derivado de la interfaz de usuario \_ PKEY \_ GlobalBackgroundColor.</span><span class="sxs-lookup"><span data-stu-id="f299a-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="f299a-148">En Windows 7, la [interfaz de usuario \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) se puede establecer independientemente de la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="f299a-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="f299a-149">En el ejemplo siguiente se muestra cómo especificar un color personalizado para las propiedades [UI \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)y [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="f299a-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="f299a-150">Convertir RGB en HSB</span><span class="sxs-lookup"><span data-stu-id="f299a-150">Convert RGB to HSB</span></span>

<span data-ttu-id="f299a-151">En esta sección se describe la fórmula necesaria para hacer coincidir dinámicamente un valor HSB del marco de cinta, la [interfaz de usuario \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) en este ejemplo, a un color RGB específico en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f299a-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="f299a-152">El fondo de la fila de pestañas se usa como punto de referencia porque se representa como una superficie de color plano en comparación con el degradado de brillo del fondo de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="f299a-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="f299a-153">Es necesaria una conversión preliminar para obtener un valor HSL intermedio.</span><span class="sxs-lookup"><span data-stu-id="f299a-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="f299a-154">A continuación, este valor HSL se puede convertir a un valor HSB.</span><span class="sxs-lookup"><span data-stu-id="f299a-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="f299a-155">La conversión de RGB a HSL se realiza fácilmente con la mayoría del software de edición de fotos.</span><span class="sxs-lookup"><span data-stu-id="f299a-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="f299a-156">La conversión de HSL (con cada componente en el intervalo de 0,0 a 1,0) a un valor de la cinta de opciones HSB se realiza a través de las siguientes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="f299a-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="f299a-157">H<sub>background</sub> = Round (255.0 H)</span><span class="sxs-lookup"><span data-stu-id="f299a-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="f299a-158">S<sub>background</sub> = Round (255.0 S)</span><span class="sxs-lookup"><span data-stu-id="f299a-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="f299a-159">B<sub>background</sub> = Round (257.7 + 149,9 LN (L)) si 0,1793 <= L <= 0,9821</span><span class="sxs-lookup"><span data-stu-id="f299a-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="f299a-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f299a-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f299a-161">Instrucciones de color</span><span class="sxs-lookup"><span data-stu-id="f299a-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="f299a-162">Propiedades de Framework</span><span class="sxs-lookup"><span data-stu-id="f299a-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





