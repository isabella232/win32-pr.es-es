---
description: Marcas de funcionalidad primitiva de controladores varios.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343140"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="1b1bb-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="1b1bb-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="1b1bb-104">Marcas de funcionalidad primitiva de controladores varios.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b1bb-105">#Definir</span><span class="sxs-lookup"><span data-stu-id="1b1bb-105">#define</span></span></td>
<td><span data-ttu-id="1b1bb-106">Valor</span><span class="sxs-lookup"><span data-stu-id="1b1bb-106">Value</span></span></td>
<td><span data-ttu-id="1b1bb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b1bb-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="1b1bb-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="1b1bb-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-109">0x00000002L</span></span></td>
<td><span data-ttu-id="1b1bb-110">El dispositivo puede habilitar y deshabilitar la modificación del búfer de profundidad en las operaciones de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="1b1bb-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="1b1bb-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-112">0x00000010L</span></span></td>
<td><span data-ttu-id="1b1bb-113">El controlador no realiza la selección de triángulos.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="1b1bb-114">Corresponde al miembro D3DCULL_NONE del tipo <a href="/windows/desktop/direct3d9/d3dcull"><strong>enumerado D3DCULL.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b1bb-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="1b1bb-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="1b1bb-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-116">0x00000020L</span></span></td>
<td><span data-ttu-id="1b1bb-117">El controlador admite la selección de triángulos en el sentido de las agujas D3DRS_CULLMODE estado.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="1b1bb-118">(Esto solo se aplica a las primitivas de triángulo). Esta marca corresponde al miembro D3DCULL_CW del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerado D3DCULL.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b1bb-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="1b1bb-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="1b1bb-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-120">0x00000040L</span></span></td>
<td><span data-ttu-id="1b1bb-121">El controlador admite la selección en sentido contrario a las agujas del reloj a través D3DRS_CULLMODE estado.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="1b1bb-122">(Esto solo se aplica a las primitivas de triángulo). Esta marca corresponde al miembro D3DCULL_CCW del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerado D3DCULL.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1b1bb-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="1b1bb-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="1b1bb-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-124">0x00000100L</span></span></td>
<td><span data-ttu-id="1b1bb-125">El dispositivo admite escrituras por canal para el búfer de color de destino de representación a través D3DRS_COLORWRITEENABLE estado.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="1b1bb-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="1b1bb-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-127">0x00000200L</span></span></td>
<td><span data-ttu-id="1b1bb-128">El dispositivo recorta correctamente los puntos de escala de tamaño superiores a 1,0 a los planos de recorte definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="1b1bb-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="1b1bb-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-130">0x00000200L</span></span></td>
<td><span data-ttu-id="1b1bb-131">Clips de dispositivos primitivos de vértices transformados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="1b1bb-132">Especifique D3DUSAGE_DONOTCLIP cuando la canalización no debe realizar ningún recorte.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="1b1bb-133">En este caso, puede que sea necesario realizar recortes de software adicionales en tiempo de dibujo, lo que requiere que el búfer de vértices esté en la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="1b1bb-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="1b1bb-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-135">0x00000400L</span></span></td>
<td><span data-ttu-id="1b1bb-136">El dispositivo admite <a href="d3dta.md">D3DTA para</a> el registro temporal.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="1b1bb-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="1b1bb-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-138">0x00000800L</span></span></td>
<td><span data-ttu-id="1b1bb-139">El dispositivo admite operaciones de combinación alfa que no D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="1b1bb-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="1b1bb-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-141">0x00000100L</span></span></td>
<td><span data-ttu-id="1b1bb-142">Un dispositivo de referencia que no se representa.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="1b1bb-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="1b1bb-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-144">0x00004000L</span></span></td>
<td><span data-ttu-id="1b1bb-145">El dispositivo admite máscaras de escritura independientes para varias texturas de elementos o varios destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="1b1bb-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="1b1bb-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-147">0x00008000L</span></span></td>
<td><span data-ttu-id="1b1bb-148">El dispositivo admite constantes por fase.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-148">Device supports per-stage constants.</span></span> <span data-ttu-id="1b1bb-149">Vea D3DTSS_CONSTANT en <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="1b1bb-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="1b1bb-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-151">0x00200000L</span></span></td>
<td><span data-ttu-id="1b1bb-152">El dispositivo admite la conversión a sRGB después de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b1bb-153">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="1b1bb-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="1b1bb-154">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="1b1bb-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="1b1bb-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-156">0x00010000L</span></span></td>
<td><span data-ttu-id="1b1bb-157">El dispositivo admite caracteres alfa especulares y independientes.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="1b1bb-158">Muchos dispositivos usan el canal alfa especular para almacenar el factor de crecimiento.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="1b1bb-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="1b1bb-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-160">0x00020000L</span></span></td>
<td><span data-ttu-id="1b1bb-161">El dispositivo admite la configuración de mezcla independiente para el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="1b1bb-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="1b1bb-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-163">0x00040000L</span></span></td>
<td><span data-ttu-id="1b1bb-164">El dispositivo admite diferentes profundidades de bits para varios destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b1bb-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="1b1bb-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="1b1bb-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-166">0x00080000L</span></span></td>
<td><span data-ttu-id="1b1bb-167">El dispositivo admite operaciones de sombreador posterior a píxeles para varios destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b1bb-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="1b1bb-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="1b1bb-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="1b1bb-169">0x00100000L</span></span></td>
<td><span data-ttu-id="1b1bb-170">El dispositivo fija el factor de mezcla por vértice.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1b1bb-171">El miembro PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="1b1bb-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="1b1bb-172">Información constante</span><span class="sxs-lookup"><span data-stu-id="1b1bb-172">Constant Information</span></span>



| <span data-ttu-id="1b1bb-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b1bb-173">Requirement</span></span>                         |  <span data-ttu-id="1b1bb-174">Value</span><span class="sxs-lookup"><span data-stu-id="1b1bb-174">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="1b1bb-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b1bb-175">Header</span></span>                   | <span data-ttu-id="1b1bb-176">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="1b1bb-176">d3d9caps.h</span></span> |
| <span data-ttu-id="1b1bb-177">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="1b1bb-177">Minimum operating system</span></span> | <span data-ttu-id="1b1bb-178">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1b1bb-178">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1b1bb-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b1bb-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b1bb-180">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1b1bb-180">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
