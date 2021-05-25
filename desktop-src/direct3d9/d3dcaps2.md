---
description: Consulte una lista de marcas de funcionalidad del controlador. Incluye las definiciones, valores y descripciones con vínculos a las API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343380"
---
# <a name="d3dcaps2"></a><span data-ttu-id="2f993-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="2f993-104">D3DCAPS2</span></span>

<span data-ttu-id="2f993-105">Marcas de funcionalidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="2f993-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f993-106">#Definir</span><span class="sxs-lookup"><span data-stu-id="2f993-106">#define</span></span></td>
<td><span data-ttu-id="2f993-107">Valor</span><span class="sxs-lookup"><span data-stu-id="2f993-107">Value</span></span></td>
<td><span data-ttu-id="2f993-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f993-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f993-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="2f993-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="2f993-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="2f993-110">0x40000000L</span></span></td>
<td><span data-ttu-id="2f993-111">El controlador es capaz de generar automáticamente mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="2f993-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="2f993-112">Para obtener más información, vea Generación automática de <a href="automatic-generation-of-mipmaps.md">mapas Mip (Direct3D 9).</a></span><span class="sxs-lookup"><span data-stu-id="2f993-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f993-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="2f993-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="2f993-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="2f993-114">0x00100000L</span></span></td>
<td><span data-ttu-id="2f993-115">El sistema tiene instalado un calibrador que puede ajustar automáticamente la rampa gamma para que el resultado sea idéntico en todos los sistemas que tienen un calibrador.</span><span class="sxs-lookup"><span data-stu-id="2f993-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="2f993-116">Para invocar el calibrador al establecer nuevos niveles gamma, use la D3DSGR_CALIBRATE al llamar a <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2f993-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="2f993-117">La calibración de las rampas gamma incurre en cierta sobrecarga de procesamiento y no se debe usar con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="2f993-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f993-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="2f993-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="2f993-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="2f993-119">0x80000000L</span></span></td>
<td><span data-ttu-id="2f993-120">El dispositivo puede crear recursos que se pueden compartir.</span><span class="sxs-lookup"><span data-stu-id="2f993-120">The device can create sharable resources.</span></span> <span data-ttu-id="2f993-121">Los métodos que crean recursos pueden establecer valores que no son NULL para sus <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>parámetros pSharedHandle.</strong></a></span><span class="sxs-lookup"><span data-stu-id="2f993-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f993-122">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="2f993-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="2f993-123">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="2f993-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f993-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="2f993-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="2f993-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="2f993-125">0x10000000L</span></span></td>
<td><span data-ttu-id="2f993-126">El controlador es capaz de administrar recursos.</span><span class="sxs-lookup"><span data-stu-id="2f993-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="2f993-127">En estos controladores, D3DPOOL_MANAGED los recursos se administrarán mediante el controlador.</span><span class="sxs-lookup"><span data-stu-id="2f993-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="2f993-128">Para que Direct3D invalide el controlador para que Direct3D administre los recursos, use la marca D3DCREATE_DISABLE_DRIVER_MANAGEMENT al llamar a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2f993-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f993-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="2f993-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="2f993-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="2f993-130">0x20000000L</span></span></td>
<td><span data-ttu-id="2f993-131">El controlador admite texturas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2f993-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f993-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="2f993-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="2f993-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="2f993-133">0x00020000L</span></span></td>
<td><span data-ttu-id="2f993-134">El controlador admite el ajuste dinámico de la rampa gamma en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="2f993-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f993-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="2f993-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="2f993-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="2f993-136">0x02000000L</span></span></td>
<td><span data-ttu-id="2f993-137">Reservado; no se usa.</span><span class="sxs-lookup"><span data-stu-id="2f993-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2f993-138">El miembro D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="2f993-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="2f993-139">Información constante</span><span class="sxs-lookup"><span data-stu-id="2f993-139">Constant Information</span></span>



|  <span data-ttu-id="2f993-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f993-140">Requirement</span></span>                        | <span data-ttu-id="2f993-141">Value</span><span class="sxs-lookup"><span data-stu-id="2f993-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="2f993-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f993-142">Header</span></span>                   | <span data-ttu-id="2f993-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="2f993-143">d3d9caps.h</span></span> |
| <span data-ttu-id="2f993-144">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="2f993-144">Minimum operating system</span></span> | <span data-ttu-id="2f993-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2f993-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2f993-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f993-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f993-147">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f993-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
