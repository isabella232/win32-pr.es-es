---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Differential.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Directiva de metadatos de fotografía de System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361314"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="a34d1-103">Directiva de metadatos de fotografía de System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="a34d1-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="a34d1-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Differential](../properties/props-system-gps-differential.md) .</span><span class="sxs-lookup"><span data-stu-id="a34d1-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a34d1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a34d1-105">PKEY</span></span>

<span data-ttu-id="a34d1-106">\_Diferencial de GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="a34d1-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="a34d1-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a34d1-107">Containers</span></span>

<span data-ttu-id="a34d1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a34d1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a34d1-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a34d1-109">Read-Only</span></span>

<span data-ttu-id="a34d1-110">No</span><span class="sxs-lookup"><span data-stu-id="a34d1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a34d1-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="a34d1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a34d1-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="a34d1-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="a34d1-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="a34d1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="a34d1-114">VT \_ UI1, VT \_ UI2 y VT \_ UI4 se aceptan.</span><span class="sxs-lookup"><span data-stu-id="a34d1-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a34d1-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="a34d1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a34d1-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="a34d1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="a34d1-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="a34d1-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a34d1-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a34d1-118">Read Paths</span></span>



| <span data-ttu-id="a34d1-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="a34d1-119">Order</span></span> | <span data-ttu-id="a34d1-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="a34d1-120">Path</span></span>                      | <span data-ttu-id="a34d1-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a34d1-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a34d1-122">1</span><span class="sxs-lookup"><span data-stu-id="a34d1-122">1</span></span>     | <span data-ttu-id="a34d1-123">/app1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="a34d1-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="a34d1-124">ushort</span><span class="sxs-lookup"><span data-stu-id="a34d1-124">ushort</span></span>      |
| <span data-ttu-id="a34d1-125">2</span><span class="sxs-lookup"><span data-stu-id="a34d1-125">2</span></span>     | <span data-ttu-id="a34d1-126">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="a34d1-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="a34d1-127">unicode</span><span class="sxs-lookup"><span data-stu-id="a34d1-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a34d1-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a34d1-128">Write Paths</span></span>



| <span data-ttu-id="a34d1-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="a34d1-129">Order</span></span> | <span data-ttu-id="a34d1-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="a34d1-130">Path</span></span>                      | <span data-ttu-id="a34d1-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a34d1-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a34d1-132">1</span><span class="sxs-lookup"><span data-stu-id="a34d1-132">1</span></span>     | <span data-ttu-id="a34d1-133">/app1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="a34d1-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="a34d1-134">ushort</span><span class="sxs-lookup"><span data-stu-id="a34d1-134">ushort</span></span>      |
| <span data-ttu-id="a34d1-135">2</span><span class="sxs-lookup"><span data-stu-id="a34d1-135">2</span></span>     | <span data-ttu-id="a34d1-136">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="a34d1-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="a34d1-137">unicode</span><span class="sxs-lookup"><span data-stu-id="a34d1-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a34d1-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a34d1-138">Remove Paths</span></span>



| <span data-ttu-id="a34d1-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="a34d1-139">Order</span></span> | <span data-ttu-id="a34d1-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="a34d1-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a34d1-141">1</span><span class="sxs-lookup"><span data-stu-id="a34d1-141">1</span></span>     | <span data-ttu-id="a34d1-142">/app1/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="a34d1-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="a34d1-143">2</span><span class="sxs-lookup"><span data-stu-id="a34d1-143">2</span></span>     | <span data-ttu-id="a34d1-144">/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="a34d1-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a34d1-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="a34d1-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a34d1-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a34d1-146">Read Paths</span></span>



| <span data-ttu-id="a34d1-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="a34d1-147">Order</span></span> | <span data-ttu-id="a34d1-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="a34d1-148">Path</span></span>                          | <span data-ttu-id="a34d1-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a34d1-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a34d1-150">1</span><span class="sxs-lookup"><span data-stu-id="a34d1-150">1</span></span>     | <span data-ttu-id="a34d1-151">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="a34d1-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="a34d1-152">ushort</span><span class="sxs-lookup"><span data-stu-id="a34d1-152">ushort</span></span>      |
| <span data-ttu-id="a34d1-153">2</span><span class="sxs-lookup"><span data-stu-id="a34d1-153">2</span></span>     | <span data-ttu-id="a34d1-154">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="a34d1-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="a34d1-155">unicode</span><span class="sxs-lookup"><span data-stu-id="a34d1-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a34d1-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a34d1-156">Write Paths</span></span>



| <span data-ttu-id="a34d1-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="a34d1-157">Order</span></span> | <span data-ttu-id="a34d1-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="a34d1-158">Path</span></span>                          | <span data-ttu-id="a34d1-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a34d1-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a34d1-160">1</span><span class="sxs-lookup"><span data-stu-id="a34d1-160">1</span></span>     | <span data-ttu-id="a34d1-161">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="a34d1-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="a34d1-162">ushort</span><span class="sxs-lookup"><span data-stu-id="a34d1-162">ushort</span></span>      |
| <span data-ttu-id="a34d1-163">2</span><span class="sxs-lookup"><span data-stu-id="a34d1-163">2</span></span>     | <span data-ttu-id="a34d1-164">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="a34d1-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="a34d1-165">unicode</span><span class="sxs-lookup"><span data-stu-id="a34d1-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a34d1-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a34d1-166">Remove Paths</span></span>



| <span data-ttu-id="a34d1-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="a34d1-167">Order</span></span> | <span data-ttu-id="a34d1-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="a34d1-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a34d1-169">1</span><span class="sxs-lookup"><span data-stu-id="a34d1-169">1</span></span>     | <span data-ttu-id="a34d1-170">/IFD/GPS/{ushort = 30}</span><span class="sxs-lookup"><span data-stu-id="a34d1-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="a34d1-171">2</span><span class="sxs-lookup"><span data-stu-id="a34d1-171">2</span></span>     | <span data-ttu-id="a34d1-172">/ifd/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="a34d1-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a34d1-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a34d1-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a34d1-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a34d1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a34d1-175">System. GPS. Differential</span><span class="sxs-lookup"><span data-stu-id="a34d1-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
