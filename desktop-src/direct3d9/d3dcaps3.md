---
description: Marcas de capacidad del controlador.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714859"
---
# <a name="d3dcaps3"></a><span data-ttu-id="a7ef3-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="a7ef3-103">D3DCAPS3</span></span>

<span data-ttu-id="a7ef3-104">Marcas de capacidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7ef3-105">#define</span><span class="sxs-lookup"><span data-stu-id="a7ef3-105">#define</span></span></td>
<td><span data-ttu-id="a7ef3-106">Value</span><span class="sxs-lookup"><span data-stu-id="a7ef3-106">Value</span></span></td>
<td><span data-ttu-id="a7ef3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7ef3-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ef3-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a7ef3-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="a7ef3-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="a7ef3-109">0x00000020L</span></span></td>
<td><span data-ttu-id="a7ef3-110">Indica que el dispositivo puede respetar el estado de representación de D3DRS_ALPHABLENDENABLE en modo de pantalla completa mientras se usa el efecto de intercambio VOLTEAr o descartar.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="a7ef3-111">Esto solo se aplica cuando los Estados D3DRS_SRCBLEND o D3DRS_DESTBLEND se establecen en uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7ef3-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="a7ef3-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="a7ef3-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="a7ef3-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="a7ef3-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="a7ef3-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="a7ef3-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="a7ef3-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="a7ef3-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ef3-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="a7ef3-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="a7ef3-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a7ef3-117">0x00000100L</span></span></td>
<td><span data-ttu-id="a7ef3-118">El dispositivo puede acelerar una copia de memoria de la memoria del sistema a la memoria de vídeo local.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="a7ef3-119">Este extremo garantiza que las llamadas a <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> y <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> se acelerarán por hardware.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="a7ef3-120">Si este Cap está ausente, estas llamadas se realizarán correctamente, pero serán más lentas.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ef3-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="a7ef3-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="a7ef3-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="a7ef3-122">0x00000200L</span></span></td>
<td><span data-ttu-id="a7ef3-123">El dispositivo puede acelerar una copia de memoria de la memoria de vídeo local a la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="a7ef3-124">Este extremo garantiza que las llamadas a <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> se acelerarán por hardware.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="a7ef3-125">Si este Cap está ausente, esta llamada se realizará correctamente, pero será más lenta.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ef3-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="a7ef3-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="a7ef3-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="a7ef3-127">0x00000400L</span></span></td>
<td><span data-ttu-id="a7ef3-128">El controlador de pantalla es compatible con la DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="a7ef3-129">Para obtener más información acerca de los datos de DDI, consulte <a href="https://msdn.microsoft.com/library/dd835176.aspx">procesamiento de High-Definition vídeo</a>.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7ef3-130">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a7ef3-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a7ef3-131">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7ef3-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="a7ef3-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="a7ef3-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="a7ef3-133">0x00000080L</span></span></td>
<td><span data-ttu-id="a7ef3-134">Indica que el dispositivo puede realizar la corrección gamma desde un búfer de retroceso en ventanas (que contiene contenido lineal) a un escritorio sRGB.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7ef3-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="a7ef3-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="a7ef3-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="a7ef3-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="a7ef3-137">Sector no se usa.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a7ef3-138">El miembro D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="a7ef3-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a7ef3-139">Información constante</span><span class="sxs-lookup"><span data-stu-id="a7ef3-139">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a7ef3-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7ef3-140">Header</span></span>                   | <span data-ttu-id="a7ef3-141">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a7ef3-141">d3d9caps.h</span></span> |
| <span data-ttu-id="a7ef3-142">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="a7ef3-142">Minimum operating system</span></span> | <span data-ttu-id="a7ef3-143">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a7ef3-143">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a7ef3-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7ef3-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ef3-145">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a7ef3-145">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




