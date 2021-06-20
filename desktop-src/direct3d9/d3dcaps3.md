---
description: Consulte una lista de las marcas de funcionalidad del controlador D3DCAPS3. Incluye las definiciones, valores y descripciones con vínculos a las API.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b28614b2b2ea3c20f828b39f2b8926cb484a88c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408268"
---
# <a name="d3dcaps3"></a><span data-ttu-id="c87cd-104">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="c87cd-104">D3DCAPS3</span></span>

<span data-ttu-id="c87cd-105">Marcas de funcionalidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="c87cd-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c87cd-106">#Definir</span><span class="sxs-lookup"><span data-stu-id="c87cd-106">#define</span></span></td>
<td><span data-ttu-id="c87cd-107">Valor</span><span class="sxs-lookup"><span data-stu-id="c87cd-107">Value</span></span></td>
<td><span data-ttu-id="c87cd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c87cd-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c87cd-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="c87cd-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="c87cd-110">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="c87cd-110">0x00000020L</span></span></td>
<td><span data-ttu-id="c87cd-111">Indica que el dispositivo puede respetar el estado D3DRS_ALPHABLENDENABLE representación en modo de pantalla completa mientras se usa el efecto de intercambio FLIP o DISCARD.</span><span class="sxs-lookup"><span data-stu-id="c87cd-111">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="c87cd-112">Esto solo se aplica cuando los estados D3DRS_SRCBLEND o D3DRS_DESTBLEND están establecidos en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c87cd-112">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="c87cd-113">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="c87cd-113">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="c87cd-114">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="c87cd-114">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="c87cd-115">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="c87cd-115">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="c87cd-116">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="c87cd-116">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c87cd-117">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="c87cd-117">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="c87cd-118">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="c87cd-118">0x00000100L</span></span></td>
<td><span data-ttu-id="c87cd-119">El dispositivo puede acelerar una copia de memoria de la memoria del sistema a la memoria de vídeo local.</span><span class="sxs-lookup"><span data-stu-id="c87cd-119">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="c87cd-120">Este límite garantiza que las <a href="/windows/desktop/api"><strong>llamadas UpdateSurface</strong></a> <a href="/windows/desktop/api"><strong>y UpdateTexture</strong></a> se acelerarán por hardware.</span><span class="sxs-lookup"><span data-stu-id="c87cd-120">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="c87cd-121">Si este límite no está presente, estas llamadas se realizarán correctamente, pero serán más lentas.</span><span class="sxs-lookup"><span data-stu-id="c87cd-121">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c87cd-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="c87cd-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="c87cd-123">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="c87cd-123">0x00000200L</span></span></td>
<td><span data-ttu-id="c87cd-124">El dispositivo puede acelerar una copia de memoria de la memoria de vídeo local a la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="c87cd-124">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="c87cd-125">Este límite garantiza que las <a href="/windows/desktop/api"><strong>llamadas a GetRenderTargetData</strong></a> se acelerarán por hardware.</span><span class="sxs-lookup"><span data-stu-id="c87cd-125">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="c87cd-126">Si este límite no está presente, esta llamada se realizará correctamente, pero será más lenta.</span><span class="sxs-lookup"><span data-stu-id="c87cd-126">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c87cd-127">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="c87cd-127">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="c87cd-128">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="c87cd-128">0x00000400L</span></span></td>
<td><span data-ttu-id="c87cd-129">El controlador de pantalla admite el DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="c87cd-129">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="c87cd-130">Para obtener más información sobre DXVA-HD DDI, consulte <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span><span class="sxs-lookup"><span data-stu-id="c87cd-130">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c87cd-131">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c87cd-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c87cd-132">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c87cd-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c87cd-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="c87cd-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="c87cd-134">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="c87cd-134">0x00000080L</span></span></td>
<td><span data-ttu-id="c87cd-135">Indica que el dispositivo puede realizar la corrección gamma desde un búfer de reserva con ventana (que contiene contenido lineal) a un escritorio sRGB.</span><span class="sxs-lookup"><span data-stu-id="c87cd-135">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c87cd-136">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="c87cd-136">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="c87cd-137">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="c87cd-137">0x8000001fL</span></span></td>
<td><span data-ttu-id="c87cd-138">Reservado; no se usa.</span><span class="sxs-lookup"><span data-stu-id="c87cd-138">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c87cd-139">El miembro D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="c87cd-139">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="c87cd-140">Información constante</span><span class="sxs-lookup"><span data-stu-id="c87cd-140">Constant Information</span></span>



|  <span data-ttu-id="c87cd-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c87cd-141">Requirement</span></span>                        | <span data-ttu-id="c87cd-142">Value</span><span class="sxs-lookup"><span data-stu-id="c87cd-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c87cd-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c87cd-143">Header</span></span>                   | <span data-ttu-id="c87cd-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="c87cd-144">d3d9caps.h</span></span> |
| <span data-ttu-id="c87cd-145">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="c87cd-145">Minimum operating system</span></span> | <span data-ttu-id="c87cd-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c87cd-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c87cd-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c87cd-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c87cd-148">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c87cd-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




