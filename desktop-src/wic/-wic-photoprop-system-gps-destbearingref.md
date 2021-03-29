---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Directiva de metadatos de la foto System. GPS. DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277620"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a><span data-ttu-id="80366-103">Directiva de metadatos de la foto System. GPS. DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-103">System.GPS.DestBearingRef Photo Metadata Policy</span></span>

<span data-ttu-id="80366-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md) .</span><span class="sxs-lookup"><span data-stu-id="80366-104">The photo metadata policy for the [System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="80366-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="80366-105">PKEY</span></span>

<span data-ttu-id="80366-106">PKEY \_ GPS \_ DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-106">PKEY\_GPS\_DestBearingRef</span></span>

### <a name="containers"></a><span data-ttu-id="80366-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="80366-107">Containers</span></span>

<span data-ttu-id="80366-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="80366-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="80366-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="80366-109">Read-Only</span></span>

<span data-ttu-id="80366-110">No</span><span class="sxs-lookup"><span data-stu-id="80366-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="80366-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="80366-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="80366-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="80366-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="80366-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="80366-113">Input Type</span></span>

<span data-ttu-id="80366-114">String.</span><span class="sxs-lookup"><span data-stu-id="80366-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="80366-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="80366-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="80366-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="80366-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="80366-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="80366-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="80366-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="80366-118">Read Paths</span></span>



| <span data-ttu-id="80366-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="80366-119">Order</span></span> | <span data-ttu-id="80366-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="80366-120">Path</span></span>                        | <span data-ttu-id="80366-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="80366-121">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="80366-122">1</span><span class="sxs-lookup"><span data-stu-id="80366-122">1</span></span>     | <span data-ttu-id="80366-123">/app1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="80366-123">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="80366-124">ascii</span><span class="sxs-lookup"><span data-stu-id="80366-124">ascii</span></span>       |
| <span data-ttu-id="80366-125">2</span><span class="sxs-lookup"><span data-stu-id="80366-125">2</span></span>     | <span data-ttu-id="80366-126">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-126">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="80366-127">unicode</span><span class="sxs-lookup"><span data-stu-id="80366-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80366-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="80366-128">Write Paths</span></span>



| <span data-ttu-id="80366-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="80366-129">Order</span></span> | <span data-ttu-id="80366-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="80366-130">Path</span></span>                        | <span data-ttu-id="80366-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="80366-131">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="80366-132">1</span><span class="sxs-lookup"><span data-stu-id="80366-132">1</span></span>     | <span data-ttu-id="80366-133">/app1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="80366-133">/app1/ifd/gps/{ushort=23}</span></span>   | <span data-ttu-id="80366-134">ascii</span><span class="sxs-lookup"><span data-stu-id="80366-134">ascii</span></span>       |
| <span data-ttu-id="80366-135">2</span><span class="sxs-lookup"><span data-stu-id="80366-135">2</span></span>     | <span data-ttu-id="80366-136">/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-136">/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="80366-137">unicode</span><span class="sxs-lookup"><span data-stu-id="80366-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80366-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="80366-138">Remove Paths</span></span>



| <span data-ttu-id="80366-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="80366-139">Order</span></span> | <span data-ttu-id="80366-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="80366-140">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="80366-141">1</span><span class="sxs-lookup"><span data-stu-id="80366-141">1</span></span>     | <span data-ttu-id="80366-142">/app1/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="80366-142">/app1/ifd/gps/{ushort=23}</span></span>   |
| <span data-ttu-id="80366-143">2</span><span class="sxs-lookup"><span data-stu-id="80366-143">2</span></span>     | <span data-ttu-id="80366-144">/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="80366-144">/xmp/exif:gpsdestbearingref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="80366-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="80366-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="80366-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="80366-146">Read Paths</span></span>



| <span data-ttu-id="80366-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="80366-147">Order</span></span> | <span data-ttu-id="80366-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="80366-148">Path</span></span>                            | <span data-ttu-id="80366-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="80366-149">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="80366-150">1</span><span class="sxs-lookup"><span data-stu-id="80366-150">1</span></span>     | <span data-ttu-id="80366-151">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="80366-151">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="80366-152">ascii</span><span class="sxs-lookup"><span data-stu-id="80366-152">ascii</span></span>       |
| <span data-ttu-id="80366-153">2</span><span class="sxs-lookup"><span data-stu-id="80366-153">2</span></span>     | <span data-ttu-id="80366-154">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-154">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="80366-155">unicode</span><span class="sxs-lookup"><span data-stu-id="80366-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="80366-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="80366-156">Write Paths</span></span>



| <span data-ttu-id="80366-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="80366-157">Order</span></span> | <span data-ttu-id="80366-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="80366-158">Path</span></span>                            | <span data-ttu-id="80366-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="80366-159">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="80366-160">1</span><span class="sxs-lookup"><span data-stu-id="80366-160">1</span></span>     | <span data-ttu-id="80366-161">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="80366-161">/ifd/gps/{ushort=23}</span></span>            | <span data-ttu-id="80366-162">ascii</span><span class="sxs-lookup"><span data-stu-id="80366-162">ascii</span></span>       |
| <span data-ttu-id="80366-163">2</span><span class="sxs-lookup"><span data-stu-id="80366-163">2</span></span>     | <span data-ttu-id="80366-164">/ifd/xmp/exif:GPSDestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-164">/ifd/xmp/exif:GPSDestBearingRef</span></span> | <span data-ttu-id="80366-165">unicode</span><span class="sxs-lookup"><span data-stu-id="80366-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="80366-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="80366-166">Remove Paths</span></span>



| <span data-ttu-id="80366-167">orden</span><span class="sxs-lookup"><span data-stu-id="80366-167">order</span></span> | <span data-ttu-id="80366-168">path</span><span class="sxs-lookup"><span data-stu-id="80366-168">path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="80366-169">1</span><span class="sxs-lookup"><span data-stu-id="80366-169">1</span></span>     | <span data-ttu-id="80366-170">/IFD/GPS/{ushort = 23}</span><span class="sxs-lookup"><span data-stu-id="80366-170">/ifd/gps/{ushort=23}</span></span>            |
| <span data-ttu-id="80366-171">2</span><span class="sxs-lookup"><span data-stu-id="80366-171">2</span></span>     | <span data-ttu-id="80366-172">/ifd/xmp/exif:gpsdestbearingref</span><span class="sxs-lookup"><span data-stu-id="80366-172">/ifd/xmp/exif:gpsdestbearingref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80366-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80366-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="80366-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80366-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80366-175">System. GPS. DestBearingRef</span><span class="sxs-lookup"><span data-stu-id="80366-175">System.GPS.DestBearingRef</span></span>](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
