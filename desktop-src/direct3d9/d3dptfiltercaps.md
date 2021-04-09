---
description: Constantes de filtrado de texturas.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080284"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="1f847-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="1f847-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="1f847-104">Constantes de filtrado de texturas.</span><span class="sxs-lookup"><span data-stu-id="1f847-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f847-105">#define</span><span class="sxs-lookup"><span data-stu-id="1f847-105">#define</span></span></td>
<td><span data-ttu-id="1f847-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f847-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="1f847-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="1f847-108">El dispositivo admite el filtrado de circunvolución monocromática.</span><span class="sxs-lookup"><span data-stu-id="1f847-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="1f847-109">Este filtro se representa mediante el miembro D3DTEXF_CONVOLUTIONMONO del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f847-110">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="1f847-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="1f847-111">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="1f847-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f847-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="1f847-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="1f847-113">El dispositivo admite el filtrado de muestra de punto por fase para aumentar las texturas.</span><span class="sxs-lookup"><span data-stu-id="1f847-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="1f847-114">El filtro de aumento de punto-muestra se representa mediante el D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="1f847-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="1f847-116">El dispositivo admite el filtrado de interpolación bilineal por fase para la lupa.</span><span class="sxs-lookup"><span data-stu-id="1f847-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="1f847-117">El filtro mipmapping de interpolación bilineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f847-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="1f847-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="1f847-119">El dispositivo admite el filtrado anisotrópico por fase para aumentar las texturas.</span><span class="sxs-lookup"><span data-stu-id="1f847-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="1f847-120">El filtro de ampliación anisotrópico se representa mediante el D3DTEXF_ANISOTROPIC miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="1f847-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="1f847-122">El dispositivo admite el filtrado de ejemplo pyramidal por fases para aumentar las texturas.</span><span class="sxs-lookup"><span data-stu-id="1f847-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="1f847-123">El filtro de lupa pyramidal se representa mediante el miembro D3DTEXF_PYRAMIDALQUAD del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f847-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="1f847-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="1f847-125">El dispositivo admite el filtrado cuádruple gaussiano de cada fase para aumentar las texturas.</span><span class="sxs-lookup"><span data-stu-id="1f847-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="1f847-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="1f847-127">El dispositivo admite el filtrado de muestra de punto por fase para las texturas de minificar.</span><span class="sxs-lookup"><span data-stu-id="1f847-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="1f847-128">El filtro minificación de punto-muestra se representa mediante el miembro D3DTEXF_POINT del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f847-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="1f847-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="1f847-130">El dispositivo admite el filtrado lineal por fase para las texturas de minificar.</span><span class="sxs-lookup"><span data-stu-id="1f847-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="1f847-131">El filtro minificación lineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="1f847-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="1f847-133">El dispositivo admite el filtrado anisotrópico por fase para las texturas de minificar.</span><span class="sxs-lookup"><span data-stu-id="1f847-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="1f847-134">El filtro minificación anisotrópico se representa mediante el miembro D3DTEXF_ANISOTROPIC del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f847-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="1f847-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="1f847-136">El dispositivo admite el filtrado de ejemplo pyramidal por fases para las texturas de minificar.</span><span class="sxs-lookup"><span data-stu-id="1f847-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="1f847-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="1f847-138">El dispositivo admite el filtrado cuádruple gaussiano por fase para las texturas de minificar.</span><span class="sxs-lookup"><span data-stu-id="1f847-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f847-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="1f847-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="1f847-140">El dispositivo admite el filtrado de muestra de punto por fase para los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="1f847-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="1f847-141">El filtro mipmapping de punto-muestra se representa mediante el miembro D3DTEXF_POINT del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f847-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="1f847-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="1f847-143">El dispositivo admite el filtrado de interpolación bilineal por fase para los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="1f847-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="1f847-144">El filtro mipmapping de interpolación bilineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1f847-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1f847-145">Estas constantes se utilizan en los miembros TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps y VertexTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="1f847-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="1f847-146">Información constante</span><span class="sxs-lookup"><span data-stu-id="1f847-146">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="1f847-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f847-147">Header</span></span>                   | <span data-ttu-id="1f847-148">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="1f847-148">d3d9caps.h</span></span> |
| <span data-ttu-id="1f847-149">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="1f847-149">Minimum operating system</span></span> | <span data-ttu-id="1f847-150">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1f847-150">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1f847-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f847-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f847-152">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1f847-152">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
