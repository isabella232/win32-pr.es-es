---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Directiva de metadatos de la foto System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688493"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="79265-103">Directiva de metadatos de la foto System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="79265-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .</span><span class="sxs-lookup"><span data-stu-id="79265-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="79265-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="79265-105">PKEY</span></span>

<span data-ttu-id="79265-106">PKEY \_ DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="79265-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="79265-107">Containers</span></span>

<span data-ttu-id="79265-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="79265-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="79265-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="79265-109">Read-Only</span></span>

<span data-ttu-id="79265-110">No</span><span class="sxs-lookup"><span data-stu-id="79265-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="79265-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="79265-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="79265-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="79265-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="79265-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="79265-113">Input Type</span></span>

<span data-ttu-id="79265-114">\_Se acepta VT LPWStr o VT \_ LPSTR.</span><span class="sxs-lookup"><span data-stu-id="79265-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="79265-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="79265-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="79265-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="79265-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="79265-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="79265-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="79265-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="79265-118">Read Paths</span></span>



| <span data-ttu-id="79265-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="79265-119">Order</span></span> | <span data-ttu-id="79265-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="79265-120">Path</span></span>                         | <span data-ttu-id="79265-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="79265-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="79265-122">1</span><span class="sxs-lookup"><span data-stu-id="79265-122">1</span></span>     | <span data-ttu-id="79265-123">/app1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="79265-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="79265-124">ascii</span><span class="sxs-lookup"><span data-stu-id="79265-124">ascii</span></span>       |
| <span data-ttu-id="79265-125">2</span><span class="sxs-lookup"><span data-stu-id="79265-125">2</span></span>     | <span data-ttu-id="79265-126">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="79265-127">unicode</span><span class="sxs-lookup"><span data-stu-id="79265-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="79265-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="79265-128">Write Paths</span></span>



| <span data-ttu-id="79265-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="79265-129">Order</span></span> | <span data-ttu-id="79265-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="79265-130">Path</span></span>                         | <span data-ttu-id="79265-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="79265-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="79265-132">1</span><span class="sxs-lookup"><span data-stu-id="79265-132">1</span></span>     | <span data-ttu-id="79265-133">/app1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="79265-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="79265-134">ascii</span><span class="sxs-lookup"><span data-stu-id="79265-134">ascii</span></span>       |
| <span data-ttu-id="79265-135">2</span><span class="sxs-lookup"><span data-stu-id="79265-135">2</span></span>     | <span data-ttu-id="79265-136">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="79265-137">unicode</span><span class="sxs-lookup"><span data-stu-id="79265-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="79265-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="79265-138">Remove Paths</span></span>



| <span data-ttu-id="79265-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="79265-139">Order</span></span> | <span data-ttu-id="79265-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="79265-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="79265-141">1</span><span class="sxs-lookup"><span data-stu-id="79265-141">1</span></span>     | <span data-ttu-id="79265-142">/app1/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="79265-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="79265-143">2</span><span class="sxs-lookup"><span data-stu-id="79265-143">2</span></span>     | <span data-ttu-id="79265-144">/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="79265-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="79265-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="79265-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="79265-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="79265-146">Read Paths</span></span>



| <span data-ttu-id="79265-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="79265-147">Order</span></span> | <span data-ttu-id="79265-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="79265-148">Path</span></span>                             | <span data-ttu-id="79265-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="79265-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="79265-150">1</span><span class="sxs-lookup"><span data-stu-id="79265-150">1</span></span>     | <span data-ttu-id="79265-151">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="79265-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="79265-152">ascii</span><span class="sxs-lookup"><span data-stu-id="79265-152">ascii</span></span>       |
| <span data-ttu-id="79265-153">2</span><span class="sxs-lookup"><span data-stu-id="79265-153">2</span></span>     | <span data-ttu-id="79265-154">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="79265-155">unicode</span><span class="sxs-lookup"><span data-stu-id="79265-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="79265-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="79265-156">Write Paths</span></span>



| <span data-ttu-id="79265-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="79265-157">Order</span></span> | <span data-ttu-id="79265-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="79265-158">Path</span></span>                             | <span data-ttu-id="79265-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="79265-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="79265-160">1</span><span class="sxs-lookup"><span data-stu-id="79265-160">1</span></span>     | <span data-ttu-id="79265-161">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="79265-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="79265-162">ascii</span><span class="sxs-lookup"><span data-stu-id="79265-162">ascii</span></span>       |
| <span data-ttu-id="79265-163">2</span><span class="sxs-lookup"><span data-stu-id="79265-163">2</span></span>     | <span data-ttu-id="79265-164">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="79265-165">unicode</span><span class="sxs-lookup"><span data-stu-id="79265-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="79265-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="79265-166">Remove Paths</span></span>



| <span data-ttu-id="79265-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="79265-167">Order</span></span> | <span data-ttu-id="79265-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="79265-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="79265-169">1</span><span class="sxs-lookup"><span data-stu-id="79265-169">1</span></span>     | <span data-ttu-id="79265-170">/IFD/GPS/{ushort = 25}</span><span class="sxs-lookup"><span data-stu-id="79265-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="79265-171">2</span><span class="sxs-lookup"><span data-stu-id="79265-171">2</span></span>     | <span data-ttu-id="79265-172">/ifd/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="79265-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="79265-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79265-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="79265-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79265-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79265-175">System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="79265-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
