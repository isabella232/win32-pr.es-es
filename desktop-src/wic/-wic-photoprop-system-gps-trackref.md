---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Directiva de metadatos de la foto System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279375"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="e240f-103">Directiva de metadatos de la foto System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="e240f-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .</span><span class="sxs-lookup"><span data-stu-id="e240f-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e240f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e240f-105">PKEY</span></span>

<span data-ttu-id="e240f-106">PKEY \_ GPS \_ TrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="e240f-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="e240f-107">Containers</span></span>

<span data-ttu-id="e240f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e240f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e240f-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e240f-109">Read-Only</span></span>

<span data-ttu-id="e240f-110">No</span><span class="sxs-lookup"><span data-stu-id="e240f-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e240f-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="e240f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e240f-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="e240f-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="e240f-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="e240f-113">Input Type</span></span>

<span data-ttu-id="e240f-114">String</span><span class="sxs-lookup"><span data-stu-id="e240f-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e240f-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="e240f-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e240f-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="e240f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="e240f-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="e240f-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e240f-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e240f-118">Read Paths</span></span>



| <span data-ttu-id="e240f-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="e240f-119">Order</span></span> | <span data-ttu-id="e240f-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="e240f-120">Path</span></span>                      | <span data-ttu-id="e240f-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e240f-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e240f-122">1</span><span class="sxs-lookup"><span data-stu-id="e240f-122">1</span></span>     | <span data-ttu-id="e240f-123">/app1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="e240f-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="e240f-124">ascii</span><span class="sxs-lookup"><span data-stu-id="e240f-124">ascii</span></span>       |
| <span data-ttu-id="e240f-125">2</span><span class="sxs-lookup"><span data-stu-id="e240f-125">2</span></span>     | <span data-ttu-id="e240f-126">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="e240f-127">unicode</span><span class="sxs-lookup"><span data-stu-id="e240f-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e240f-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e240f-128">Write Paths</span></span>



| <span data-ttu-id="e240f-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="e240f-129">Order</span></span> | <span data-ttu-id="e240f-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="e240f-130">Path</span></span>                      | <span data-ttu-id="e240f-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e240f-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e240f-132">1</span><span class="sxs-lookup"><span data-stu-id="e240f-132">1</span></span>     | <span data-ttu-id="e240f-133">/app1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="e240f-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="e240f-134">ascii</span><span class="sxs-lookup"><span data-stu-id="e240f-134">ascii</span></span>       |
| <span data-ttu-id="e240f-135">2</span><span class="sxs-lookup"><span data-stu-id="e240f-135">2</span></span>     | <span data-ttu-id="e240f-136">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="e240f-137">unicode</span><span class="sxs-lookup"><span data-stu-id="e240f-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e240f-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e240f-138">Remove Paths</span></span>



| <span data-ttu-id="e240f-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="e240f-139">Order</span></span> | <span data-ttu-id="e240f-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="e240f-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="e240f-141">1</span><span class="sxs-lookup"><span data-stu-id="e240f-141">1</span></span>     | <span data-ttu-id="e240f-142">/app1/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="e240f-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="e240f-143">2</span><span class="sxs-lookup"><span data-stu-id="e240f-143">2</span></span>     | <span data-ttu-id="e240f-144">/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="e240f-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="e240f-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="e240f-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e240f-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e240f-146">Read Paths</span></span>



| <span data-ttu-id="e240f-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="e240f-147">Order</span></span> | <span data-ttu-id="e240f-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="e240f-148">Path</span></span>                      | <span data-ttu-id="e240f-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e240f-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e240f-150">1</span><span class="sxs-lookup"><span data-stu-id="e240f-150">1</span></span>     | <span data-ttu-id="e240f-151">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="e240f-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="e240f-152">ascii</span><span class="sxs-lookup"><span data-stu-id="e240f-152">ascii</span></span>       |
| <span data-ttu-id="e240f-153">2</span><span class="sxs-lookup"><span data-stu-id="e240f-153">2</span></span>     | <span data-ttu-id="e240f-154">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="e240f-155">unicode</span><span class="sxs-lookup"><span data-stu-id="e240f-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e240f-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e240f-156">Write Paths</span></span>



| <span data-ttu-id="e240f-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="e240f-157">Order</span></span> | <span data-ttu-id="e240f-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="e240f-158">Path</span></span>                      | <span data-ttu-id="e240f-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e240f-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e240f-160">1</span><span class="sxs-lookup"><span data-stu-id="e240f-160">1</span></span>     | <span data-ttu-id="e240f-161">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="e240f-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="e240f-162">ascii</span><span class="sxs-lookup"><span data-stu-id="e240f-162">ascii</span></span>       |
| <span data-ttu-id="e240f-163">2</span><span class="sxs-lookup"><span data-stu-id="e240f-163">2</span></span>     | <span data-ttu-id="e240f-164">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="e240f-165">unicode</span><span class="sxs-lookup"><span data-stu-id="e240f-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e240f-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e240f-166">Remove Paths</span></span>



| <span data-ttu-id="e240f-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="e240f-167">Order</span></span> | <span data-ttu-id="e240f-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="e240f-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="e240f-169">1</span><span class="sxs-lookup"><span data-stu-id="e240f-169">1</span></span>     | <span data-ttu-id="e240f-170">/IFD/GPS/{ushort = 14}</span><span class="sxs-lookup"><span data-stu-id="e240f-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="e240f-171">2</span><span class="sxs-lookup"><span data-stu-id="e240f-171">2</span></span>     | <span data-ttu-id="e240f-172">/ifd/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="e240f-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e240f-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e240f-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e240f-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e240f-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e240f-175">System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="e240f-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
