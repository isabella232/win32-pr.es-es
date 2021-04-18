---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Directiva de metadatos de la foto de System. Photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706999"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a><span data-ttu-id="efa77-103">Directiva de metadatos de la foto de System. Photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="efa77-103">System.Photo.CameraManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="efa77-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="efa77-104">The photo metadata policy for the [System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="efa77-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="efa77-105">PKEY</span></span>

<span data-ttu-id="efa77-106">PKEY \_ Photo \_ CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="efa77-106">PKEY\_Photo\_CameraManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="efa77-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="efa77-107">Containers</span></span>

<span data-ttu-id="efa77-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="efa77-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="efa77-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="efa77-109">Read-Only</span></span>

<span data-ttu-id="efa77-110">No</span><span class="sxs-lookup"><span data-stu-id="efa77-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="efa77-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="efa77-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="efa77-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="efa77-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="efa77-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="efa77-113">Input Type</span></span>

<span data-ttu-id="efa77-114">String.</span><span class="sxs-lookup"><span data-stu-id="efa77-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="efa77-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="efa77-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="efa77-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="efa77-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="efa77-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="efa77-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="efa77-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="efa77-118">Read Paths</span></span>



| <span data-ttu-id="efa77-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="efa77-119">Order</span></span> | <span data-ttu-id="efa77-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="efa77-120">Path</span></span>                   | <span data-ttu-id="efa77-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="efa77-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="efa77-122">1</span><span class="sxs-lookup"><span data-stu-id="efa77-122">1</span></span>     | <span data-ttu-id="efa77-123">/app1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="efa77-123">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="efa77-124">ascii</span><span class="sxs-lookup"><span data-stu-id="efa77-124">ascii</span></span>       |
| <span data-ttu-id="efa77-125">2</span><span class="sxs-lookup"><span data-stu-id="efa77-125">2</span></span>     | <span data-ttu-id="efa77-126">/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-126">/xmp/tiff:Make</span></span>         | <span data-ttu-id="efa77-127">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-127">unicode</span></span>     |
| <span data-ttu-id="efa77-128">3</span><span class="sxs-lookup"><span data-stu-id="efa77-128">3</span></span>     | <span data-ttu-id="efa77-129">/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-129">/xmp/tiff:make</span></span>         | <span data-ttu-id="efa77-130">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="efa77-131">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="efa77-131">Write Paths</span></span>



| <span data-ttu-id="efa77-132">Pedido</span><span class="sxs-lookup"><span data-stu-id="efa77-132">Order</span></span> | <span data-ttu-id="efa77-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="efa77-133">Path</span></span>                   | <span data-ttu-id="efa77-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="efa77-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="efa77-135">1</span><span class="sxs-lookup"><span data-stu-id="efa77-135">1</span></span>     | <span data-ttu-id="efa77-136">/app1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="efa77-136">/app1/ifd/{ushort=271}</span></span> | <span data-ttu-id="efa77-137">ascii</span><span class="sxs-lookup"><span data-stu-id="efa77-137">ascii</span></span>       |
| <span data-ttu-id="efa77-138">2</span><span class="sxs-lookup"><span data-stu-id="efa77-138">2</span></span>     | <span data-ttu-id="efa77-139">/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-139">/xmp/tiff:Make</span></span>         | <span data-ttu-id="efa77-140">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-140">unicode</span></span>     |
| <span data-ttu-id="efa77-141">3</span><span class="sxs-lookup"><span data-stu-id="efa77-141">3</span></span>     | <span data-ttu-id="efa77-142">/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-142">/xmp/tiff:make</span></span>         | <span data-ttu-id="efa77-143">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="efa77-144">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="efa77-144">Remove Paths</span></span>



| <span data-ttu-id="efa77-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="efa77-145">Order</span></span> | <span data-ttu-id="efa77-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="efa77-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="efa77-147">1</span><span class="sxs-lookup"><span data-stu-id="efa77-147">1</span></span>     | <span data-ttu-id="efa77-148">/app1/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="efa77-148">/app1/ifd/{ushort=271}</span></span> |
| <span data-ttu-id="efa77-149">2</span><span class="sxs-lookup"><span data-stu-id="efa77-149">2</span></span>     | <span data-ttu-id="efa77-150">/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-150">/xmp/tiff:Make</span></span>         |
| <span data-ttu-id="efa77-151">3</span><span class="sxs-lookup"><span data-stu-id="efa77-151">3</span></span>     | <span data-ttu-id="efa77-152">/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-152">/xmp/tiff:make</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="efa77-153">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="efa77-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="efa77-154">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="efa77-154">Read Paths</span></span>



| <span data-ttu-id="efa77-155">Pedido</span><span class="sxs-lookup"><span data-stu-id="efa77-155">Order</span></span> | <span data-ttu-id="efa77-156">Ruta</span><span class="sxs-lookup"><span data-stu-id="efa77-156">Path</span></span>               | <span data-ttu-id="efa77-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="efa77-157">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="efa77-158">1</span><span class="sxs-lookup"><span data-stu-id="efa77-158">1</span></span>     | <span data-ttu-id="efa77-159">/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="efa77-159">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="efa77-160">ascii</span><span class="sxs-lookup"><span data-stu-id="efa77-160">ascii</span></span>       |
| <span data-ttu-id="efa77-161">2</span><span class="sxs-lookup"><span data-stu-id="efa77-161">2</span></span>     | <span data-ttu-id="efa77-162">/IFD/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-162">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="efa77-163">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-163">unicode</span></span>     |
| <span data-ttu-id="efa77-164">3</span><span class="sxs-lookup"><span data-stu-id="efa77-164">3</span></span>     | <span data-ttu-id="efa77-165">/IFD/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-165">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="efa77-166">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="efa77-167">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="efa77-167">Write Paths</span></span>



| <span data-ttu-id="efa77-168">Pedido</span><span class="sxs-lookup"><span data-stu-id="efa77-168">Order</span></span> | <span data-ttu-id="efa77-169">Ruta</span><span class="sxs-lookup"><span data-stu-id="efa77-169">Path</span></span>               | <span data-ttu-id="efa77-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="efa77-170">Disk Format</span></span> |
|-------|--------------------|-------------|
| <span data-ttu-id="efa77-171">1</span><span class="sxs-lookup"><span data-stu-id="efa77-171">1</span></span>     | <span data-ttu-id="efa77-172">/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="efa77-172">/ifd/{ushort=271}</span></span>  | <span data-ttu-id="efa77-173">ascii</span><span class="sxs-lookup"><span data-stu-id="efa77-173">ascii</span></span>       |
| <span data-ttu-id="efa77-174">2</span><span class="sxs-lookup"><span data-stu-id="efa77-174">2</span></span>     | <span data-ttu-id="efa77-175">/IFD/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-175">/ifd/xmp/tiff:Make</span></span> | <span data-ttu-id="efa77-176">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-176">unicode</span></span>     |
| <span data-ttu-id="efa77-177">3</span><span class="sxs-lookup"><span data-stu-id="efa77-177">3</span></span>     | <span data-ttu-id="efa77-178">/IFD/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-178">/ifd/xmp/tiff:make</span></span> | <span data-ttu-id="efa77-179">unicode</span><span class="sxs-lookup"><span data-stu-id="efa77-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="efa77-180">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="efa77-180">Remove Paths</span></span>



| <span data-ttu-id="efa77-181">Pedido</span><span class="sxs-lookup"><span data-stu-id="efa77-181">Order</span></span> | <span data-ttu-id="efa77-182">Ruta</span><span class="sxs-lookup"><span data-stu-id="efa77-182">Path</span></span>               |
|-------|--------------------|
| <span data-ttu-id="efa77-183">1</span><span class="sxs-lookup"><span data-stu-id="efa77-183">1</span></span>     | <span data-ttu-id="efa77-184">/IFD/{ushort = 271}</span><span class="sxs-lookup"><span data-stu-id="efa77-184">/ifd/{ushort=271}</span></span>  |
| <span data-ttu-id="efa77-185">2</span><span class="sxs-lookup"><span data-stu-id="efa77-185">2</span></span>     | <span data-ttu-id="efa77-186">/IFD/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-186">/ifd/xmp/tiff:Make</span></span> |
| <span data-ttu-id="efa77-187">3</span><span class="sxs-lookup"><span data-stu-id="efa77-187">3</span></span>     | <span data-ttu-id="efa77-188">/IFD/XMP/TIFF: make</span><span class="sxs-lookup"><span data-stu-id="efa77-188">/ifd/xmp/tiff:make</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="efa77-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efa77-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="efa77-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efa77-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa77-191">System. Photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="efa77-191">System.Photo.CameraManufacturer</span></span>](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
