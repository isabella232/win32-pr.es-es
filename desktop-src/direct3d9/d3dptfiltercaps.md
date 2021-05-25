---
description: Constantes de filtrado de textura.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343090"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="3a973-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="3a973-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="3a973-104">Constantes de filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="3a973-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a973-105">#Definir</span><span class="sxs-lookup"><span data-stu-id="3a973-105">#define</span></span></td>
<td><span data-ttu-id="3a973-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a973-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="3a973-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="3a973-108">El dispositivo admite el filtrado de convolución monocromática.</span><span class="sxs-lookup"><span data-stu-id="3a973-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="3a973-109">Este filtro se representa mediante el D3DTEXF_CONVOLUTIONMONO del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a973-110">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="3a973-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="3a973-111">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="3a973-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a973-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="3a973-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="3a973-113">El dispositivo admite el filtrado de muestras de punto por fase para las texturas de aumento.</span><span class="sxs-lookup"><span data-stu-id="3a973-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="3a973-114">El filtro de ampliación de ejemplo de punto se representa D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="3a973-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="3a973-116">El dispositivo admite el filtrado de interpolación bilineal por fase para la lupa de mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="3a973-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="3a973-117">El filtro mipmapping de interpolación bilineal se representa D3DTEXF_LINEAR miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a973-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="3a973-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="3a973-119">El dispositivo admite el filtrado anisotropico por fase para las texturas de aumento.</span><span class="sxs-lookup"><span data-stu-id="3a973-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="3a973-120">El filtro de ampliación anisotropica se representa mediante D3DTEXF_ANISOTROPIC miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="3a973-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="3a973-122">El dispositivo admite el filtrado de muestras piramidales por fase para las texturas de lupa.</span><span class="sxs-lookup"><span data-stu-id="3a973-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="3a973-123">El filtro de lupa piramidal se representa mediante D3DTEXF_PYRAMIDALQUAD miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a973-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="3a973-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="3a973-125">El dispositivo admite el filtrado de cuadrándes gaussiano por fase para las texturas de lupa.</span><span class="sxs-lookup"><span data-stu-id="3a973-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="3a973-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="3a973-127">El dispositivo admite el filtrado de muestras de punto por fase para la compresión de texturas.</span><span class="sxs-lookup"><span data-stu-id="3a973-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="3a973-128">El filtro de minificación de ejemplo de punto se representa mediante D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a973-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="3a973-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="3a973-130">El dispositivo admite el filtrado lineal por fase para la compresión de texturas.</span><span class="sxs-lookup"><span data-stu-id="3a973-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="3a973-131">El filtro de minificación lineal se representa mediante D3DTEXF_LINEAR miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="3a973-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="3a973-133">El dispositivo admite el filtrado anisotropico por fase para la compresión de texturas.</span><span class="sxs-lookup"><span data-stu-id="3a973-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="3a973-134">El filtro de minificación anisotropica se representa mediante D3DTEXF_ANISOTROPIC miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a973-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="3a973-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="3a973-136">El dispositivo admite el filtrado de muestras piramidales por fase para la compresión de texturas.</span><span class="sxs-lookup"><span data-stu-id="3a973-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="3a973-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="3a973-138">El dispositivo admite el filtrado de cuadrándes gaussiano por fase para la compresión de texturas.</span><span class="sxs-lookup"><span data-stu-id="3a973-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a973-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="3a973-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="3a973-140">El dispositivo admite el filtrado de ejemplo de punto por fase para mapas mip.</span><span class="sxs-lookup"><span data-stu-id="3a973-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="3a973-141">El filtro mipmapping de ejemplo de punto se representa mediante el miembro D3DTEXF_POINT del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a973-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="3a973-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="3a973-143">El dispositivo admite el filtrado de interpolación bilineal por fase para mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="3a973-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="3a973-144">El filtro mipmapping de interpolación bilineal se representa mediante D3DTEXF_LINEAR miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3a973-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3a973-145">Estas constantes las usan los miembros TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps y VertexTextureFilterCaps de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="3a973-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="3a973-146">Información constante</span><span class="sxs-lookup"><span data-stu-id="3a973-146">Constant Information</span></span>



|  <span data-ttu-id="3a973-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a973-147">Requirement</span></span>                        | <span data-ttu-id="3a973-148">Value</span><span class="sxs-lookup"><span data-stu-id="3a973-148">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="3a973-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a973-149">Header</span></span>                   | <span data-ttu-id="3a973-150">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="3a973-150">d3d9caps.h</span></span> |
| <span data-ttu-id="3a973-151">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="3a973-151">Minimum operating system</span></span> | <span data-ttu-id="3a973-152">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3a973-152">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3a973-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a973-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a973-154">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="3a973-154">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
