---
title: Efecto de administración del color
description: Use el efecto administración del color para transformar una imagen de un perfil de color ICC (International color Consortium) en otro. El efecto transforma la imagen según la especificación de ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- efecto de administración del color
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422233"
---
# <a name="color-management-effect"></a><span data-ttu-id="ed22e-105">Efecto de administración del color</span><span class="sxs-lookup"><span data-stu-id="ed22e-105">Color management effect</span></span>

<span data-ttu-id="ed22e-106">Use el efecto administración del color para transformar una imagen de un perfil de color ICC (International color Consortium) en otro.</span><span class="sxs-lookup"><span data-stu-id="ed22e-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="ed22e-107">El efecto transforma la imagen según la [especificación de ICC](https://www.color.org).</span><span class="sxs-lookup"><span data-stu-id="ed22e-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="ed22e-108">El CLSID para este efecto es CLSID \_ D2D1ColorManagement.</span><span class="sxs-lookup"><span data-stu-id="ed22e-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="ed22e-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="ed22e-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="ed22e-110">Modos de intención de representación</span><span class="sxs-lookup"><span data-stu-id="ed22e-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="ed22e-111">Modos alfa de imagen de entrada</span><span class="sxs-lookup"><span data-stu-id="ed22e-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="ed22e-112">Compatibilidad con la especificación de ICC</span><span class="sxs-lookup"><span data-stu-id="ed22e-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="ed22e-113">Comportamiento del canal alfa</span><span class="sxs-lookup"><span data-stu-id="ed22e-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="ed22e-114">Modos de calidad</span><span class="sxs-lookup"><span data-stu-id="ed22e-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="ed22e-115">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed22e-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="ed22e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed22e-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="ed22e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed22e-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="ed22e-118">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="ed22e-118">Effect properties</span></span>

| <span data-ttu-id="ed22e-119">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="ed22e-119">Display name and index enumeration</span></span> | <span data-ttu-id="ed22e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed22e-120">Description</span></span> |
|-|-|
| <span data-ttu-id="ed22e-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="ed22e-121">SourceContext</span></span><br/> <span data-ttu-id="ed22e-122">D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ contexto de color de origen \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="ed22e-123">Información del espacio de colores de origen.</span><span class="sxs-lookup"><span data-stu-id="ed22e-123">The source color space information.</span></span> <span data-ttu-id="ed22e-124">El tipo es [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="ed22e-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="ed22e-125">El valor predeterminado es NULL.</span><span class="sxs-lookup"><span data-stu-id="ed22e-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="ed22e-126">SourceIntent</span><span class="sxs-lookup"><span data-stu-id="ed22e-126">SourceIntent</span></span><br/> <span data-ttu-id="ed22e-127">Intención de representación de origen de D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="ed22e-128">La intención de representación de ICC que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ed22e-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="ed22e-129">El tipo es D2D1 \_ COLORMANAGEMENT \_ Rendering \_ Intent.</span><span class="sxs-lookup"><span data-stu-id="ed22e-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="ed22e-130">El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ed22e-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="ed22e-131">DestinationContext</span><span class="sxs-lookup"><span data-stu-id="ed22e-131">DestinationContext</span></span><br/> <span data-ttu-id="ed22e-132">Contexto de color de destino de D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="ed22e-133">La información del espacio de colores de destino.</span><span class="sxs-lookup"><span data-stu-id="ed22e-133">The destination color space information.</span></span> <span data-ttu-id="ed22e-134">El tipo es [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="ed22e-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="ed22e-135">El valor predeterminado es NULL.</span><span class="sxs-lookup"><span data-stu-id="ed22e-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="ed22e-136">DestinationIntent</span><span class="sxs-lookup"><span data-stu-id="ed22e-136">DestinationIntent</span></span><br/> <span data-ttu-id="ed22e-137">Objetivo de representación de destino de D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="ed22e-138">La intención de representación de ICC que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ed22e-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="ed22e-139">El tipo es D2D1 \_ COLORMANAGEMENT \_ Rendering \_ Intent.</span><span class="sxs-lookup"><span data-stu-id="ed22e-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="ed22e-140">El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ed22e-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="ed22e-141">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="ed22e-141">AlphaMode</span></span><br/> <span data-ttu-id="ed22e-142">D2D1 \_ COLORMANAGEMENT \_ prop \_ \_ modo alfa</span><span class="sxs-lookup"><span data-stu-id="ed22e-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="ed22e-143">Cómo interpretar los datos alfa contenidos en la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed22e-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="ed22e-144">El tipo es D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa.</span><span class="sxs-lookup"><span data-stu-id="ed22e-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="ed22e-145">El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa \_ premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="ed22e-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="ed22e-146">Calidad</span><span class="sxs-lookup"><span data-stu-id="ed22e-146">Quality</span></span><br/> <span data-ttu-id="ed22e-147">Calidad de la D2D1 \_ COLORMANAGEMENT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="ed22e-148">Nivel de calidad de la transformación.</span><span class="sxs-lookup"><span data-stu-id="ed22e-148">The quality level of the transform.</span></span> <span data-ttu-id="ed22e-149">El tipo es D2D1 \_ COLORMANAGEMENT \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="ed22e-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="ed22e-150">El valor predeterminado es D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal.</span><span class="sxs-lookup"><span data-stu-id="ed22e-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="ed22e-151">Modos de intención de representación</span><span class="sxs-lookup"><span data-stu-id="ed22e-151">Rendering intent modes</span></span>

| <span data-ttu-id="ed22e-152">Enumeración</span><span class="sxs-lookup"><span data-stu-id="ed22e-152">Enumeration</span></span> | <span data-ttu-id="ed22e-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed22e-153">Description</span></span> |
|-|-|
| <span data-ttu-id="ed22e-154">D2D1 \_ COLORMANAGEMENT de \_ representación del intento de representación \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="ed22e-155">El efecto comprime o expande la gama de colores completa de la imagen para rellenar la gama de colores del dispositivo, de modo que se conserva el saldo de gris, pero no se puede conservar la precisión de la colorimétrico.</span><span class="sxs-lookup"><span data-stu-id="ed22e-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="ed22e-156">D2D1 \_ COLORMANAGEMENT de \_ representación \_ \_ con referencia \_ colorimétrica relativa</span><span class="sxs-lookup"><span data-stu-id="ed22e-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="ed22e-157">El efecto conserva el croma de los colores de la imagen con el posible gasto de matiz y luminosidad.</span><span class="sxs-lookup"><span data-stu-id="ed22e-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="ed22e-158">\_Saturación del \_ objetivo de \_ representación \_ de D2D1 COLORMANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ed22e-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="ed22e-159">El efecto ajusta los colores que quedan fuera del intervalo de colores que el dispositivo de salida representa en el color más cercano disponible.</span><span class="sxs-lookup"><span data-stu-id="ed22e-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="ed22e-160">No conserva el punto blanco.</span><span class="sxs-lookup"><span data-stu-id="ed22e-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="ed22e-161">D2D1 \_ COLORMANAGEMENT de representación de la \_ \_ intención \_ absoluta \_ colorimétrica</span><span class="sxs-lookup"><span data-stu-id="ed22e-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="ed22e-162">El efecto ajusta los colores que se encuentran fuera del intervalo que el dispositivo de salida puede representar en el color más cercano que se puede representar.</span><span class="sxs-lookup"><span data-stu-id="ed22e-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="ed22e-163">El efecto no cambia los demás colores y conserva el punto blanco.</span><span class="sxs-lookup"><span data-stu-id="ed22e-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="ed22e-164">Modos alfa de imagen de entrada</span><span class="sxs-lookup"><span data-stu-id="ed22e-164">Input image alpha modes</span></span>

| <span data-ttu-id="ed22e-165">Enumeración</span><span class="sxs-lookup"><span data-stu-id="ed22e-165">Enumeration</span></span> | <span data-ttu-id="ed22e-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed22e-166">Description</span></span> |
|-|-|
| <span data-ttu-id="ed22e-167">D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa \_ premultiplicado</span><span class="sxs-lookup"><span data-stu-id="ed22e-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="ed22e-168">El efecto presupone que el modo alfa está premultiplicado.</span><span class="sxs-lookup"><span data-stu-id="ed22e-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="ed22e-169">D2D1 \_ \_ modo alfa \_ COLORMANAGEMENT \_ recto</span><span class="sxs-lookup"><span data-stu-id="ed22e-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="ed22e-170">El efecto presupone que el modo alfa es recto.</span><span class="sxs-lookup"><span data-stu-id="ed22e-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="ed22e-171">Cambios de comportamiento de D2D1_GAMMA1_G2084</span><span class="sxs-lookup"><span data-stu-id="ed22e-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="ed22e-172">Si la aplicación usa el espacio de [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) , o uno de los valores de enumeración de [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) que usan el espacio de colores SMPTE St. 2084 (cuantificador perceptual), la aplicación intenta trabajar con datos HDR.</span><span class="sxs-lookup"><span data-stu-id="ed22e-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="ed22e-173">Las API [**ID2D1DeviceContext5:: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) y [**ID2D1DeviceContext5:: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) no tienen en cuenta esto; en su lugar, el contenido de HDR se escala para ajustarse al intervalo 0-1 durante la operación de desgamma de G2084.</span><span class="sxs-lookup"><span data-stu-id="ed22e-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="ed22e-174">En la práctica, el contenido que se codifica en este espacio de gamma usa una WhiteLevel de referencia de 10.000 Nits, que normalmente se representaría en CCCS como 10.000/80 = 125,0.</span><span class="sxs-lookup"><span data-stu-id="ed22e-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="ed22e-175">Por lo tanto, para facilitar mejor la aplicación, es más sencillo para esta conversión gamma escalar también la luminancia en un factor de 125.</span><span class="sxs-lookup"><span data-stu-id="ed22e-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="ed22e-176">A partir de Windows 10, versión 1809 (10,0; Compilación 17763), el comportamiento del efecto de administración del color es tal que aplica este ajuste de escala.</span><span class="sxs-lookup"><span data-stu-id="ed22e-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="ed22e-177">Esto significa que usted, como desarrollador, no tiene que aplicar un segundo [efecto de ajuste de nivel blanco](white-level-adjustment-effect.md) a la canalización.</span><span class="sxs-lookup"><span data-stu-id="ed22e-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="ed22e-178">Compatibilidad con la especificación de ICC</span><span class="sxs-lookup"><span data-stu-id="ed22e-178">Compliance with ICC specification</span></span>

<span data-ttu-id="ed22e-179">El efecto de administración del color es compatible con la especificación de ICC v 4.3, con estas limitaciones:</span><span class="sxs-lookup"><span data-stu-id="ed22e-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="ed22e-180">El efecto es compatible con los espacios de colores de canal 1, 3 y 4.</span><span class="sxs-lookup"><span data-stu-id="ed22e-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="ed22e-181">El efecto no admite ColorSpace o perfiles de color con nombre.</span><span class="sxs-lookup"><span data-stu-id="ed22e-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="ed22e-182">Comportamiento del canal alfa</span><span class="sxs-lookup"><span data-stu-id="ed22e-182">Alpha channel behavior</span></span>

<span data-ttu-id="ed22e-183">En general, el efecto establece Alpha en 1 (opaco) si no hay ningún dato alfa en la imagen de origen y los datos alfa se descartan si no hay espacio en la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="ed22e-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="ed22e-184">En la tabla siguiente se describe el comportamiento alfa.</span><span class="sxs-lookup"><span data-stu-id="ed22e-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ed22e-185">ColorSpace de origen, formato de píxel</span><span class="sxs-lookup"><span data-stu-id="ed22e-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="ed22e-186">ColorSpace de destino, formato de píxel</span><span class="sxs-lookup"><span data-stu-id="ed22e-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="ed22e-187">Comportamiento alfa</span><span class="sxs-lookup"><span data-stu-id="ed22e-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="ed22e-188">1 canal, formato de píxeles R $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ed22e-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ed22e-189">1 canal, formato de píxeles de R</span><span class="sxs-lookup"><span data-stu-id="ed22e-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="ed22e-190">(Sin datos alfa)</span><span class="sxs-lookup"><span data-stu-id="ed22e-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-191">1 canal, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-192">Los datos alfa se establecen en 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="ed22e-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ed22e-193">3 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-194">Los datos alfa se establecen en 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="ed22e-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-195">4 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-196">(Sin datos alfa)</span><span class="sxs-lookup"><span data-stu-id="ed22e-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="ed22e-197">1 canal, formato de píxel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ed22e-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ed22e-198">1 canal, formato de píxeles de R</span><span class="sxs-lookup"><span data-stu-id="ed22e-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="ed22e-199">Los datos alfa se descartan</span><span class="sxs-lookup"><span data-stu-id="ed22e-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-200">1 canal, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-201">Los datos alfa se pasan por</span><span class="sxs-lookup"><span data-stu-id="ed22e-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ed22e-202">3 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-203">Los datos alfa se pasan por</span><span class="sxs-lookup"><span data-stu-id="ed22e-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-204">4 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-205">Los datos alfa se descartan</span><span class="sxs-lookup"><span data-stu-id="ed22e-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="ed22e-206">3 Channel, formato de píxel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ed22e-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ed22e-207">1 canal, formato de píxeles de R</span><span class="sxs-lookup"><span data-stu-id="ed22e-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="ed22e-208">Los datos alfa se descartan</span><span class="sxs-lookup"><span data-stu-id="ed22e-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-209">1 canal, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-210">Los datos alfa se pasan por</span><span class="sxs-lookup"><span data-stu-id="ed22e-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ed22e-211">3 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-212">Los datos alfa se pasan por</span><span class="sxs-lookup"><span data-stu-id="ed22e-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-213">4 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-214">Los datos alfa se descartan</span><span class="sxs-lookup"><span data-stu-id="ed22e-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="ed22e-215">4 canales, formato de píxel RGBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="ed22e-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ed22e-216">1 canal, formato de píxeles de R</span><span class="sxs-lookup"><span data-stu-id="ed22e-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="ed22e-217">(Sin datos alfa)</span><span class="sxs-lookup"><span data-stu-id="ed22e-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-218">1 canal, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-219">Los datos alfa se establecen en 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="ed22e-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ed22e-220">3 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-221">Los datos alfa se establecen en 1 (opaco)</span><span class="sxs-lookup"><span data-stu-id="ed22e-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ed22e-222">4 canales, formato de píxel RGBA</span><span class="sxs-lookup"><span data-stu-id="ed22e-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="ed22e-223">(Sin datos alfa)</span><span class="sxs-lookup"><span data-stu-id="ed22e-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="ed22e-224">Modos de calidad</span><span class="sxs-lookup"><span data-stu-id="ed22e-224">Quality modes</span></span>

| <span data-ttu-id="ed22e-225">Mode</span><span class="sxs-lookup"><span data-stu-id="ed22e-225">Mode</span></span> | <span data-ttu-id="ed22e-226">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed22e-226">Description</span></span> |
|-|-|
| <span data-ttu-id="ed22e-227">Prueba de calidad de D2D1 \_ COLORMANAGEMENT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed22e-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="ed22e-228">Modo de calidad inferior.</span><span class="sxs-lookup"><span data-stu-id="ed22e-228">The lowest quality mode.</span></span> <span data-ttu-id="ed22e-229">Este modo requiere el nivel de característica 9 \_ 1 o superior.</span><span class="sxs-lookup"><span data-stu-id="ed22e-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="ed22e-230">D2D1 \_ COLORMANAGEMENT \_ calidad \_ normal</span><span class="sxs-lookup"><span data-stu-id="ed22e-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="ed22e-231">Modo de calidad normal.</span><span class="sxs-lookup"><span data-stu-id="ed22e-231">Normal quality mode.</span></span> <span data-ttu-id="ed22e-232">Este modo requiere el nivel de característica 9 \_ 1 o superior.</span><span class="sxs-lookup"><span data-stu-id="ed22e-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="ed22e-233">Calidad de D2D1 \_ COLORMANAGEMENT \_ \_ óptima</span><span class="sxs-lookup"><span data-stu-id="ed22e-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="ed22e-234">El modo de mejor calidad.</span><span class="sxs-lookup"><span data-stu-id="ed22e-234">The best quality mode.</span></span> <span data-ttu-id="ed22e-235">Este modo requiere el nivel de característica 10 \_ 0 o superior, así como los búferes de precisión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="ed22e-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="ed22e-236">Este modo admite la precisión de punto flotante, así como el intervalo extendido, tal como se define en la especificación de ICC v 4.3.</span><span class="sxs-lookup"><span data-stu-id="ed22e-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="ed22e-237">Se produce un error en el efecto de administración del color al dibujar si la aplicación solicita un modo de calidad que no es compatible con el hardware.</span><span class="sxs-lookup"><span data-stu-id="ed22e-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="ed22e-238">Puede determinar el nivel de característica cuando llame a [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span><span class="sxs-lookup"><span data-stu-id="ed22e-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="ed22e-239">Puede comprobar si hay compatibilidad con el búfer de punto flotante mediante una llamada a [**ID2D1EffectContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) con el valor [**D2D1 \_ buffer \_ Precision \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span><span class="sxs-lookup"><span data-stu-id="ed22e-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="ed22e-240">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed22e-240">Sample code</span></span>

<span data-ttu-id="ed22e-241">Para obtener un ejemplo de este efecto, descargue el [ejemplo de ajuste de foto de efectos de Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)y vea la lección 4 del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ed22e-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed22e-242">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed22e-242">Requirements</span></span>

| <span data-ttu-id="ed22e-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed22e-243">Requirement</span></span> | <span data-ttu-id="ed22e-244">Value</span><span class="sxs-lookup"><span data-stu-id="ed22e-244">Value</span></span> |
|-|-|
| <span data-ttu-id="ed22e-245">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed22e-245">Minimum supported client</span></span> | <span data-ttu-id="ed22e-246">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="ed22e-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ed22e-247">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed22e-247">Minimum supported server</span></span> | <span data-ttu-id="ed22e-248">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="ed22e-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ed22e-249">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed22e-249">Header</span></span> | <span data-ttu-id="ed22e-250">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ed22e-250">d2d1effects.h</span></span> |
| <span data-ttu-id="ed22e-251">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed22e-251">Library</span></span> | <span data-ttu-id="ed22e-252">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ed22e-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="ed22e-253">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed22e-253">Related topics</span></span>

* [<span data-ttu-id="ed22e-254">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="ed22e-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
