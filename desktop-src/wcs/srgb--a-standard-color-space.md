---
title: 'sRGB: espacio de color estándar'
description: Como resultado de las consideraciones sobre el ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de colores predefinido estándar conocido como sRGB (IEC 61966-2-1), para permitir una asignación de colores precisa con muy poca sobrecarga de datos.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Sistema de colores de Windows (WCS), espacio de colores sRGB
- WCS (Windows Color System), espacio de colores sRGB
- administración de colores de imagen, espacio de colores sRGB
- administración de colores, espacio de colores sRGB
- colors,sRGB color space
- Espacio de colores sRGB
- espacios de colores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443646"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="30c12-110">sRGB: un espacio de colores estándar</span><span class="sxs-lookup"><span data-stu-id="30c12-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="30c12-111">Como resultado de las consideraciones sobre el ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de [colores](c.md) predefinido estándar conocido como *sRGB* (IEC 61966-2-1), para permitir una asignación de [colores](c.md) precisa con muy poca sobrecarga de datos.</span><span class="sxs-lookup"><span data-stu-id="30c12-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="30c12-112">Hay disponible una versión del archivo de ayuda de un documento técnico que describe los detalles técnicos de sRGB, sRGB.hlp, en la carpeta Ayuda de la referencia del programador de \\ WCS 1.0.</span><span class="sxs-lookup"><span data-stu-id="30c12-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="30c12-113">Diferentes formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en un espacio de colores sRGB.</span><span class="sxs-lookup"><span data-stu-id="30c12-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="30c12-114">En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) en **LCS \_ sRGB** se especifica que los colores DIB están en el espacio de colores sRGB.</span><span class="sxs-lookup"><span data-stu-id="30c12-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="30c12-115">WCS 1.0 proporciona compatibilidad nativa con sRGB.</span><span class="sxs-lookup"><span data-stu-id="30c12-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="30c12-116">Hay dos maneras de usar WCS 1.0 para representar una imagen definida en el espacio de colores sRGB:</span><span class="sxs-lookup"><span data-stu-id="30c12-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="30c12-117">**Para representar una imagen dentro del contexto del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="30c12-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="30c12-118">Cree un contexto de dispositivo (DC) en el dispositivo para mostrar.</span><span class="sxs-lookup"><span data-stu-id="30c12-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="30c12-119">Establezca la administración de colores mediante [**la función SetICMMode.**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)</span><span class="sxs-lookup"><span data-stu-id="30c12-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="30c12-120">Use la [**función SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir la DIB al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="30c12-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="30c12-121">Siempre que el miembro **bV5CSMType** de la estructura DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) esté establecido en **LCS \_ sRGB,** el sistema realizará la administración de colores adecuada.</span><span class="sxs-lookup"><span data-stu-id="30c12-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="30c12-122">**Para representar una imagen fuera del contexto del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="30c12-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="30c12-123">Cree una transformación mediante [**CreateColorTransformW.**](/windows/win32/api/icm/nf-icm-createcolortransformw)</span><span class="sxs-lookup"><span data-stu-id="30c12-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="30c12-124">El **miembro lcsCSType de** la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) a la que apunta el parámetro *pLogColorSpace* debe establecerse en **LCS \_ sRGB.**</span><span class="sxs-lookup"><span data-stu-id="30c12-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="30c12-125">El *parámetro hDestProfile* indica el espacio de color del dispositivo para mostrar.</span><span class="sxs-lookup"><span data-stu-id="30c12-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="30c12-126">Use la transformación de color creada para que el color coincida con la imagen antes de mostrarla en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30c12-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="30c12-127">Valores predeterminados de WCS 1.0 para el espacio de color de entrada y el perfil de salida</span><span class="sxs-lookup"><span data-stu-id="30c12-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="30c12-128">Cuando no se especifica ningún espacio de color de entrada, de forma predeterminada WCS 1.0 usa el espacio de colores sRGB como espacio de color de entrada para la asignación [de colores.](c.md)</span><span class="sxs-lookup"><span data-stu-id="30c12-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="30c12-129">Cuando no se especifica ningún perfil de salida, pero se especifica un dispositivo predeterminado, WCS 1.0 selecciona un perfil de salida predeterminado.</span><span class="sxs-lookup"><span data-stu-id="30c12-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="30c12-130">Si el dispositivo predeterminado no tiene un perfil asociado, WCS 1.0 usa el espacio de color sRGB como perfil de salida.</span><span class="sxs-lookup"><span data-stu-id="30c12-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="30c12-131">En la tabla siguiente se muestran las transformaciones de color resultantes cuando un dispositivo predeterminado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="30c12-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|  &nbsp;                               | <span data-ttu-id="30c12-132">Perfil de salida especificado</span><span class="sxs-lookup"><span data-stu-id="30c12-132">Output Profile Specified</span></span>                              | <span data-ttu-id="30c12-133">Perfil de salida no especificado</span><span class="sxs-lookup"><span data-stu-id="30c12-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="30c12-134">Espacio de color de entrada especificado</span><span class="sxs-lookup"><span data-stu-id="30c12-134">Input Color Space Specified</span></span>     | <span data-ttu-id="30c12-135">La transformación usa los perfiles especificados.</span><span class="sxs-lookup"><span data-stu-id="30c12-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="30c12-136">La transformación convierte el espacio de color de entrada conocido en sRGB.</span><span class="sxs-lookup"><span data-stu-id="30c12-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="30c12-137">Espacio de color de entrada no especificado</span><span class="sxs-lookup"><span data-stu-id="30c12-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="30c12-138">La transformación convierte de sRGB a un perfil de salida conocido.</span><span class="sxs-lookup"><span data-stu-id="30c12-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="30c12-139">Se supone que la transformación de sRGB a sRGB; no se hace nada.</span><span class="sxs-lookup"><span data-stu-id="30c12-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="30c12-140">sRGB y perfiles incrustados</span><span class="sxs-lookup"><span data-stu-id="30c12-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="30c12-141">A partir de la versión 2.0 de ICM, las aplicaciones que usan WCS pueden insertar perfiles en imágenes.</span><span class="sxs-lookup"><span data-stu-id="30c12-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="30c12-142">Los perfiles insertados ayudan a las aplicaciones de los usuarios a mantener una apariencia de color coherente, incluso si las imágenes se transmiten a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="30c12-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="30c12-143">Las imágenes que usan el espacio de colores sRGB no necesitan un perfil de color incrustado.</span><span class="sxs-lookup"><span data-stu-id="30c12-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="30c12-144">Dado que no tienen ningún perfil incrustado, las imágenes basadas en sRGB son más pequeñas y fáciles de transferir a través de canales de datos con ancho de banda limitado.</span><span class="sxs-lookup"><span data-stu-id="30c12-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="30c12-145">Las aplicaciones deben establecer la **marca \_ lcs sRGB** en el encabezado de mapa de bits de la imagen para indicar que la imagen usa el espacio de color sRGB.</span><span class="sxs-lookup"><span data-stu-id="30c12-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="30c12-146">Para obtener más información, vea [Estructuras de encabezado de mapa de bits de Windows](using-structures-in-wcs-1-0.md) y [**LOGCOLORSPACE.**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)</span><span class="sxs-lookup"><span data-stu-id="30c12-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 