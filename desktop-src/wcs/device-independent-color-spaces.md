---
title: Espacios de color independientes del dispositivo
description: Al reconocer la necesidad de medidas de color estándar, independientes del dispositivo, la Comisión International de l'Eclairage (Comisión Internacional en iluminación) o CIE, creó un espacio de colores basado en \ 0034; imaginario \ 0034; colores primarios.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Sistema de color de Windows (WCS), espacios de colores independientes del dispositivo
- WCS (sistema de colores de Windows), espacios de colores independientes del dispositivo
- Administración del color de imagen, espacios de colores independientes del dispositivo
- Administración del color, espacios de colores independientes del dispositivo
- colores, espacios de colores independientes del dispositivo
- espacios de colores, independiente del dispositivo
- espacios de colores independientes del dispositivo
- Comisión International de l'Eclairage (CIE)
- Comisión Internacional de iluminación (CIE)
- CIE (Comisión International de l'Eclairage)
- CIE (Comisión Internacional sobre iluminación)
- Espacio de colores de CIEXYZ
- Espacio de colores XYZ
- espacio de color sRGB
- espacios de colores, CIEXYZ
- espacios de colores, sRGB
- espacios de colores, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721128"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="1e4c6-120">Espacios de color independientes del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1e4c6-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="1e4c6-121">Al reconocer la necesidad de las medidas de color estándar, independientes del dispositivo, la Comisión International de l'Eclairage (Comisión Internacional sobre iluminación) o CIE, creó un [espacio de colores](c.md) basado en los [colores primarios](p.md)"imaginarios".</span><span class="sxs-lookup"><span data-stu-id="1e4c6-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="1e4c6-122">No se espera que ningún dispositivo real genere colores en este espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="1e4c6-123">Se utiliza como medio para convertir colores de un espacio de colores a otro.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="1e4c6-124">Los colores primarios de este espacio de colores son los colores abstractos X, Y y Z.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="1e4c6-125">El espacio de colores 1931 CIEXYZ se utiliza ampliamente como base para la conversión del espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="1e4c6-126">Con el aumento de Internet, sin embargo, las consideraciones de ancho de banda han hecho que el espacio de colores XYZ no sea manejable.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="1e4c6-127">El intercambio de imágenes sobre el ancho de banda limitado de Internet requiere un modelo de [color](c.md)más compacto.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="1e4c6-128">Como resultado, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de colores RGB predefinido estándar conocido como sRGB, para permitir una administración de color precisa con muy poca sobrecarga de datos.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="1e4c6-129">Este estándar se ha aprobado como estándar internacional formal por el Comisión electrotécnica internacional (CEI) (IEC) como IEC 61966-2-1: sistemas multimedia y medida EquipmentColour y ManagementPart 2-1: el color ManagementDefault RGB de color.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="1e4c6-130">Está disponible directamente desde el IEC en <https://www.iec.ch/> .</span><span class="sxs-lookup"><span data-stu-id="1e4c6-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="1e4c6-131">La información que describe los problemas técnicos implicados en sRGB está disponible en Internet en:</span><span class="sxs-lookup"><span data-stu-id="1e4c6-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="1e4c6-132">Un espacio de colores predeterminado estándar para Internet-sRGB</span><span class="sxs-lookup"><span data-stu-id="1e4c6-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="1e4c6-133">En la \\ carpeta ayuda de la referencia del programador de WCS 1,0 del SDK de la plataforma se encuentra disponible una versión de archivo de ayuda de una nota del producto en la que se describen los problemas técnicos relacionados con sRGB, sRGB. hlp.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="1e4c6-134">Los distintos formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en el espacio de color sRGB.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="1e4c6-135">En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) en LCS \_ sRGB, se especifica que los colores DIB están en el espacio de color sRGB.</span><span class="sxs-lookup"><span data-stu-id="1e4c6-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




