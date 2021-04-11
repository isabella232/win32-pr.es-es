---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Directiva de metadatos de la foto System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278837"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="a0629-103">Directiva de metadatos de la foto System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="a0629-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .</span><span class="sxs-lookup"><span data-stu-id="a0629-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a0629-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a0629-105">PKEY</span></span>

<span data-ttu-id="a0629-106">PKEY \_ GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="a0629-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a0629-107">Containers</span></span>

<span data-ttu-id="a0629-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a0629-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a0629-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0629-109">Read-Only</span></span>

<span data-ttu-id="a0629-110">No</span><span class="sxs-lookup"><span data-stu-id="a0629-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a0629-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="a0629-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a0629-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="a0629-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a0629-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a0629-113">Input Type</span></span>

<span data-ttu-id="a0629-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="a0629-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a0629-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="a0629-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a0629-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="a0629-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="a0629-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="a0629-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a0629-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a0629-118">Read Paths</span></span>



| <span data-ttu-id="a0629-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="a0629-119">Order</span></span> | <span data-ttu-id="a0629-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="a0629-120">Path</span></span>                         | <span data-ttu-id="a0629-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a0629-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="a0629-122">1</span><span class="sxs-lookup"><span data-stu-id="a0629-122">1</span></span>     | <span data-ttu-id="a0629-123">/app1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="a0629-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="a0629-124">ascii</span><span class="sxs-lookup"><span data-stu-id="a0629-124">ascii</span></span>       |
| <span data-ttu-id="a0629-125">2</span><span class="sxs-lookup"><span data-stu-id="a0629-125">2</span></span>     | <span data-ttu-id="a0629-126">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="a0629-127">unicode</span><span class="sxs-lookup"><span data-stu-id="a0629-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a0629-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a0629-128">Write Paths</span></span>



| <span data-ttu-id="a0629-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="a0629-129">Order</span></span> | <span data-ttu-id="a0629-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="a0629-130">Path</span></span>                         | <span data-ttu-id="a0629-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a0629-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="a0629-132">1</span><span class="sxs-lookup"><span data-stu-id="a0629-132">1</span></span>     | <span data-ttu-id="a0629-133">/app1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="a0629-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="a0629-134">ascii</span><span class="sxs-lookup"><span data-stu-id="a0629-134">ascii</span></span>       |
| <span data-ttu-id="a0629-135">2</span><span class="sxs-lookup"><span data-stu-id="a0629-135">2</span></span>     | <span data-ttu-id="a0629-136">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="a0629-137">unicode</span><span class="sxs-lookup"><span data-stu-id="a0629-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a0629-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a0629-138">Remove Paths</span></span>



| <span data-ttu-id="a0629-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="a0629-139">Order</span></span> | <span data-ttu-id="a0629-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="a0629-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="a0629-141">1</span><span class="sxs-lookup"><span data-stu-id="a0629-141">1</span></span>     | <span data-ttu-id="a0629-142">/app1/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="a0629-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="a0629-143">2</span><span class="sxs-lookup"><span data-stu-id="a0629-143">2</span></span>     | <span data-ttu-id="a0629-144">/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="a0629-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a0629-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="a0629-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a0629-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a0629-146">Read Paths</span></span>



| <span data-ttu-id="a0629-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="a0629-147">Order</span></span> | <span data-ttu-id="a0629-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="a0629-148">Path</span></span>                             | <span data-ttu-id="a0629-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a0629-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="a0629-150">1</span><span class="sxs-lookup"><span data-stu-id="a0629-150">1</span></span>     | <span data-ttu-id="a0629-151">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="a0629-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="a0629-152">ascii</span><span class="sxs-lookup"><span data-stu-id="a0629-152">ascii</span></span>       |
| <span data-ttu-id="a0629-153">2</span><span class="sxs-lookup"><span data-stu-id="a0629-153">2</span></span>     | <span data-ttu-id="a0629-154">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="a0629-155">unicode</span><span class="sxs-lookup"><span data-stu-id="a0629-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a0629-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a0629-156">Write Paths</span></span>



| <span data-ttu-id="a0629-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="a0629-157">Order</span></span> | <span data-ttu-id="a0629-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="a0629-158">Path</span></span>                             | <span data-ttu-id="a0629-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a0629-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="a0629-160">1</span><span class="sxs-lookup"><span data-stu-id="a0629-160">1</span></span>     | <span data-ttu-id="a0629-161">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="a0629-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="a0629-162">ascii</span><span class="sxs-lookup"><span data-stu-id="a0629-162">ascii</span></span>       |
| <span data-ttu-id="a0629-163">2</span><span class="sxs-lookup"><span data-stu-id="a0629-163">2</span></span>     | <span data-ttu-id="a0629-164">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="a0629-165">unicode</span><span class="sxs-lookup"><span data-stu-id="a0629-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a0629-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a0629-166">Remove Paths</span></span>



| <span data-ttu-id="a0629-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="a0629-167">Order</span></span> | <span data-ttu-id="a0629-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="a0629-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="a0629-169">1</span><span class="sxs-lookup"><span data-stu-id="a0629-169">1</span></span>     | <span data-ttu-id="a0629-170">/IFD/GPS/{ushort = 16}</span><span class="sxs-lookup"><span data-stu-id="a0629-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="a0629-171">2</span><span class="sxs-lookup"><span data-stu-id="a0629-171">2</span></span>     | <span data-ttu-id="a0629-172">/ifd/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="a0629-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a0629-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0629-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0629-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0629-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0629-175">System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="a0629-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
