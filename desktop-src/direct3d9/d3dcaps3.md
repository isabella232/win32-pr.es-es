---
description: Marcas de funcionalidad del controlador.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343370"
---
# <a name="d3dcaps3"></a><span data-ttu-id="cf7f2-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="cf7f2-103">D3DCAPS3</span></span>

<span data-ttu-id="cf7f2-104">Marcas de funcionalidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf7f2-105">#Definir</span><span class="sxs-lookup"><span data-stu-id="cf7f2-105">#define</span></span></td>
<td><span data-ttu-id="cf7f2-106">Valor</span><span class="sxs-lookup"><span data-stu-id="cf7f2-106">Value</span></span></td>
<td><span data-ttu-id="cf7f2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf7f2-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf7f2-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="cf7f2-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="cf7f2-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="cf7f2-109">0x00000020L</span></span></td>
<td><span data-ttu-id="cf7f2-110">Indica que el dispositivo puede respetar el estado D3DRS_ALPHABLENDENABLE representación en modo de pantalla completa mientras se usa el efecto de intercambio FLIP o DISCARD.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="cf7f2-111">Esto solo se aplica cuando los estados D3DRS_SRCBLEND o D3DRS_DESTBLEND están establecidos en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf7f2-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="cf7f2-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="cf7f2-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="cf7f2-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="cf7f2-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="cf7f2-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="cf7f2-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="cf7f2-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="cf7f2-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf7f2-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="cf7f2-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="cf7f2-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="cf7f2-117">0x00000100L</span></span></td>
<td><span data-ttu-id="cf7f2-118">El dispositivo puede acelerar una copia de memoria de la memoria del sistema a la memoria de vídeo local.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="cf7f2-119">Este límite garantiza que las <a href="/windows/desktop/api"><strong>llamadas UpdateSurface</strong></a> <a href="/windows/desktop/api"><strong>y UpdateTexture</strong></a> se acelerarán por hardware.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="cf7f2-120">Si este límite no está presente, estas llamadas se realizarán correctamente, pero serán más lentas.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf7f2-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="cf7f2-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="cf7f2-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="cf7f2-122">0x00000200L</span></span></td>
<td><span data-ttu-id="cf7f2-123">El dispositivo puede acelerar una copia de memoria de la memoria de vídeo local a la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="cf7f2-124">Este límite garantiza que las <a href="/windows/desktop/api"><strong>llamadas a GetRenderTargetData</strong></a> se acelerarán por hardware.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="cf7f2-125">Si este límite no está presente, esta llamada se realizará correctamente, pero será más lenta.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf7f2-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="cf7f2-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="cf7f2-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="cf7f2-127">0x00000400L</span></span></td>
<td><span data-ttu-id="cf7f2-128">El controlador de pantalla admite el DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="cf7f2-129">Para obtener más información sobre DXVA-HD DDI, vea <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf7f2-130">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="cf7f2-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="cf7f2-131">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf7f2-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="cf7f2-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="cf7f2-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="cf7f2-133">0x00000080L</span></span></td>
<td><span data-ttu-id="cf7f2-134">Indica que el dispositivo puede realizar la corrección gamma desde un búfer de reserva con ventanas (que contiene contenido lineal) a un escritorio sRGB.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf7f2-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="cf7f2-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="cf7f2-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="cf7f2-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="cf7f2-137">Reservado; no se usa.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf7f2-138">El miembro D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="cf7f2-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="cf7f2-139">Información constante</span><span class="sxs-lookup"><span data-stu-id="cf7f2-139">Constant Information</span></span>



|  <span data-ttu-id="cf7f2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf7f2-140">Requirement</span></span>                        | <span data-ttu-id="cf7f2-141">Value</span><span class="sxs-lookup"><span data-stu-id="cf7f2-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="cf7f2-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf7f2-142">Header</span></span>                   | <span data-ttu-id="cf7f2-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="cf7f2-143">d3d9caps.h</span></span> |
| <span data-ttu-id="cf7f2-144">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="cf7f2-144">Minimum operating system</span></span> | <span data-ttu-id="cf7f2-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cf7f2-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cf7f2-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf7f2-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf7f2-147">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="cf7f2-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




