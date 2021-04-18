---
description: Marcas de capacidad del controlador.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720280"
---
# <a name="d3dcaps2"></a><span data-ttu-id="9c0ed-103">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="9c0ed-103">D3DCAPS2</span></span>

<span data-ttu-id="9c0ed-104">Marcas de capacidad del controlador.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c0ed-105">#define</span><span class="sxs-lookup"><span data-stu-id="9c0ed-105">#define</span></span></td>
<td><span data-ttu-id="9c0ed-106">Value</span><span class="sxs-lookup"><span data-stu-id="9c0ed-106">Value</span></span></td>
<td><span data-ttu-id="9c0ed-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c0ed-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-108">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="9c0ed-108">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="9c0ed-109">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-109">0x40000000L</span></span></td>
<td><span data-ttu-id="9c0ed-110">El controlador es capaz de generar automáticamente mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-110">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="9c0ed-111">Para obtener más información, vea <a href="automatic-generation-of-mipmaps.md">generación automática de mapas MIP (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-111">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-112">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="9c0ed-112">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="9c0ed-113">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-113">0x00100000L</span></span></td>
<td><span data-ttu-id="9c0ed-114">El sistema tiene instalado un del calibrador que puede ajustar automáticamente la rampa de gamma para que el resultado sea idéntico en todos los sistemas que tienen un del calibrador.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-114">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="9c0ed-115">Para invocar el del calibrador al establecer nuevos niveles de gamma, use la marca D3DSGR_CALIBRATE al llamar a <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-115">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="9c0ed-116">La calibración de rampas de gamma incurre en cierta sobrecarga de procesamiento y no se debe utilizar con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-116">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-117">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="9c0ed-117">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="9c0ed-118">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-118">0x80000000L</span></span></td>
<td><span data-ttu-id="9c0ed-119">El dispositivo puede crear recursos que se pueden compartir.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-119">The device can create sharable resources.</span></span> <span data-ttu-id="9c0ed-120">Los métodos que crean recursos pueden establecer valores no NULL para los parámetros <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9c0ed-120">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c0ed-121">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9c0ed-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9c0ed-122">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-123">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="9c0ed-123">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="9c0ed-124">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-124">0x10000000L</span></span></td>
<td><span data-ttu-id="9c0ed-125">El controlador es capaz de administrar recursos.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-125">The driver is capable of managing resources.</span></span> <span data-ttu-id="9c0ed-126">En estos controladores, el controlador administrará D3DPOOL_MANAGED recursos.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-126">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="9c0ed-127">Para que Direct3D invalide el controlador para que Direct3D administre los recursos, use la marca D3DCREATE_DISABLE_DRIVER_MANAGEMENT al llamar a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-127">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-128">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="9c0ed-128">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="9c0ed-129">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-129">0x20000000L</span></span></td>
<td><span data-ttu-id="9c0ed-130">El controlador admite texturas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-130">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9c0ed-131">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="9c0ed-131">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="9c0ed-132">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-132">0x00020000L</span></span></td>
<td><span data-ttu-id="9c0ed-133">El controlador admite el ajuste de rampa gamma dinámica en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-133">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9c0ed-134">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="9c0ed-134">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="9c0ed-135">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="9c0ed-135">0x02000000L</span></span></td>
<td><span data-ttu-id="9c0ed-136">Sector no se usa.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-136">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9c0ed-137">El miembro D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="9c0ed-137">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="9c0ed-138">Información constante</span><span class="sxs-lookup"><span data-stu-id="9c0ed-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9c0ed-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c0ed-139">Header</span></span>                   | <span data-ttu-id="9c0ed-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="9c0ed-140">d3d9caps.h</span></span> |
| <span data-ttu-id="9c0ed-141">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="9c0ed-141">Minimum operating system</span></span> | <span data-ttu-id="9c0ed-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9c0ed-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9c0ed-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c0ed-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0ed-144">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9c0ed-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
