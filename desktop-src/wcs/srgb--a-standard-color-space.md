---
title: 'sRGB: espacio de color estándar'
description: Como resultado de las consideraciones de ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de colores predefinido estándar conocido como sRGB (IEC 61966-2-1), para permitir una asignación de color precisa con muy poca sobrecarga de datos.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Sistema de color de Windows (WCS), espacio de color sRGB
- WCS (sistema de colores de Windows), espacio de color sRGB
- Administración del color de imagen, espacio de color sRGB
- Administración del color, espacio de color sRGB
- colores, espacio de color sRGB
- espacio de color sRGB
- espacios de colores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2021
ms.locfileid: "105721155"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="f9776-110">sRGB: un espacio de colores estándar</span><span class="sxs-lookup"><span data-stu-id="f9776-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="f9776-111">Como resultado de las consideraciones de ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un [espacio de colores](c.md) predefinido estándar conocido como *sRGB* (IEC 61966-2-1), para permitir una asignación de [color](c.md) precisa con muy poca sobrecarga de datos.</span><span class="sxs-lookup"><span data-stu-id="f9776-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="f9776-112">Hay disponible una versión de archivo de ayuda de una nota del producto en la que se describen los detalles técnicos de sRGB, sRGB. HLP, en la \\ carpeta help de la referencia del programador de WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="f9776-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="f9776-113">Los distintos formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en el espacio de color sRGB.</span><span class="sxs-lookup"><span data-stu-id="f9776-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="f9776-114">En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) en **LCS \_ sRGB** , se especifica que los colores DIB están en el espacio de color sRGB.</span><span class="sxs-lookup"><span data-stu-id="f9776-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="f9776-115">WCS 1,0 proporciona compatibilidad nativa con sRGB.</span><span class="sxs-lookup"><span data-stu-id="f9776-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="f9776-116">Hay dos maneras de usar WCS 1,0 para representar una imagen definida en el espacio de color sRGB:</span><span class="sxs-lookup"><span data-stu-id="f9776-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="f9776-117">**Para representar una imagen dentro del contexto del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="f9776-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="f9776-118">Cree un contexto de dispositivo (DC) en el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f9776-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="f9776-119">Establezca la administración del color mediante la función [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .</span><span class="sxs-lookup"><span data-stu-id="f9776-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="f9776-120">Utilice la función [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir el DIB al controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f9776-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="f9776-121">Siempre que el miembro **bV5CSMType** de la estructura DIB [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) esté establecido en **LCS \_ sRGB**, el sistema llevará a cabo la administración de color adecuada.</span><span class="sxs-lookup"><span data-stu-id="f9776-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="f9776-122">**Para representar una imagen fuera del contexto del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="f9776-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="f9776-123">Cree una transformación mediante [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span><span class="sxs-lookup"><span data-stu-id="f9776-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="f9776-124">El miembro **lcsCSType** de la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) señalada por el parámetro *PLogColorSpace* debe establecerse en **LCS \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="f9776-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="f9776-125">El parámetro *hDestProfile* indica el espacio de colores del dispositivo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f9776-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="f9776-126">Use la transformación color creada para que el color coincida con la imagen antes de mostrarla en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9776-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="f9776-127">Valores predeterminados de WCS 1,0 para el espacio de colores de entrada y el perfil de salida</span><span class="sxs-lookup"><span data-stu-id="f9776-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="f9776-128">Cuando no se especifica ningún espacio de colores de entrada, de forma predeterminada, WCS 1,0 usa el espacio de color sRGB como espacio de colores de entrada para la [asignación de colores](c.md).</span><span class="sxs-lookup"><span data-stu-id="f9776-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="f9776-129">Cuando no se especifica ningún perfil de salida, pero se especifica un dispositivo predeterminado, WCS 1,0 selecciona un perfil de salida predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9776-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="f9776-130">Si el dispositivo predeterminado no tiene un perfil asociado, WCS 1,0 usa el espacio de color sRGB como perfil de salida.</span><span class="sxs-lookup"><span data-stu-id="f9776-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="f9776-131">En la tabla siguiente se muestran las transformaciones de color resultantes cuando un dispositivo predeterminado no está disponible.</span><span class="sxs-lookup"><span data-stu-id="f9776-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|                                 | <span data-ttu-id="f9776-132">Perfil de salida especificado</span><span class="sxs-lookup"><span data-stu-id="f9776-132">Output Profile Specified</span></span>                              | <span data-ttu-id="f9776-133">No se ha especificado el perfil de salida</span><span class="sxs-lookup"><span data-stu-id="f9776-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="f9776-134">Espacio de colores de entrada especificado</span><span class="sxs-lookup"><span data-stu-id="f9776-134">Input Color Space Specified</span></span>     | <span data-ttu-id="f9776-135">La transformación utiliza los perfiles especificados.</span><span class="sxs-lookup"><span data-stu-id="f9776-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="f9776-136">La transformación convierte el espacio de colores de entrada conocido en sRGB.</span><span class="sxs-lookup"><span data-stu-id="f9776-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="f9776-137">No se ha especificado el espacio de colores de entrada</span><span class="sxs-lookup"><span data-stu-id="f9776-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="f9776-138">La transformación convierte de sRGB a Perfil de salida conocido.</span><span class="sxs-lookup"><span data-stu-id="f9776-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="f9776-139">Se presupone la transformación de sRGB a sRGB; no se hace nada.</span><span class="sxs-lookup"><span data-stu-id="f9776-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="f9776-140">Perfiles de sRGB y Embedded</span><span class="sxs-lookup"><span data-stu-id="f9776-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="f9776-141">A partir de la versión 2,0 de ICM, las aplicaciones que usan WCS pueden insertar perfiles en las imágenes.</span><span class="sxs-lookup"><span data-stu-id="f9776-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="f9776-142">Los perfiles incrustados ayudan a las aplicaciones de los usuarios a mantener una apariencia de color coherente incluso si las imágenes se transmiten a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="f9776-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="f9776-143">Las imágenes que usan el espacio de colores sRGB no necesitan un perfil de color incrustado.</span><span class="sxs-lookup"><span data-stu-id="f9776-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="f9776-144">Dado que no tienen ningún perfil incrustado, las imágenes basadas en sRGB son más pequeñas y se pueden transferir más fácilmente entre los canales de datos con ancho de banda limitado.</span><span class="sxs-lookup"><span data-stu-id="f9776-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="f9776-145">Las aplicaciones deben establecer la marca de **LCS \_ sRGB** en el encabezado de mapa de bits de la imagen para indicar que la imagen usa el espacio de color sRGB.</span><span class="sxs-lookup"><span data-stu-id="f9776-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="f9776-146">Para obtener más información, vea [estructuras de encabezado de mapa de bits de Windows](using-structures-in-wcs-1-0.md) y [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="f9776-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 