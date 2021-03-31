---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Directiva de metadatos de la foto de System. Photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912622"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="3c05e-103">Directiva de metadatos de la foto de System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="3c05e-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="3c05e-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .</span><span class="sxs-lookup"><span data-stu-id="3c05e-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3c05e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3c05e-105">PKEY</span></span>

<span data-ttu-id="3c05e-106">PKEY \_ Photo \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="3c05e-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="3c05e-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="3c05e-107">Containers</span></span>

<span data-ttu-id="3c05e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3c05e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3c05e-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3c05e-109">Read-Only</span></span>

<span data-ttu-id="3c05e-110">No</span><span class="sxs-lookup"><span data-stu-id="3c05e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3c05e-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="3c05e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3c05e-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="3c05e-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="3c05e-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="3c05e-113">Input Type</span></span>

<span data-ttu-id="3c05e-114">String.</span><span class="sxs-lookup"><span data-stu-id="3c05e-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3c05e-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="3c05e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3c05e-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="3c05e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3c05e-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="3c05e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3c05e-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3c05e-118">Read Paths</span></span>



| <span data-ttu-id="3c05e-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="3c05e-119">Order</span></span> | <span data-ttu-id="3c05e-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="3c05e-120">Path</span></span>                   | <span data-ttu-id="3c05e-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3c05e-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3c05e-122">1</span><span class="sxs-lookup"><span data-stu-id="3c05e-122">1</span></span>     | <span data-ttu-id="3c05e-123">/app1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="3c05e-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="3c05e-124">ascii</span><span class="sxs-lookup"><span data-stu-id="3c05e-124">ascii</span></span>       |
| <span data-ttu-id="3c05e-125">2</span><span class="sxs-lookup"><span data-stu-id="3c05e-125">2</span></span>     | <span data-ttu-id="3c05e-126">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="3c05e-127">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-127">unicode</span></span>     |
| <span data-ttu-id="3c05e-128">3</span><span class="sxs-lookup"><span data-stu-id="3c05e-128">3</span></span>     | <span data-ttu-id="3c05e-129">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="3c05e-130">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3c05e-131">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3c05e-131">Write Paths</span></span>



| <span data-ttu-id="3c05e-132">Pedido</span><span class="sxs-lookup"><span data-stu-id="3c05e-132">Order</span></span> | <span data-ttu-id="3c05e-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="3c05e-133">Path</span></span>                   | <span data-ttu-id="3c05e-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3c05e-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3c05e-135">1</span><span class="sxs-lookup"><span data-stu-id="3c05e-135">1</span></span>     | <span data-ttu-id="3c05e-136">/app1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="3c05e-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="3c05e-137">ascii</span><span class="sxs-lookup"><span data-stu-id="3c05e-137">ascii</span></span>       |
| <span data-ttu-id="3c05e-138">2</span><span class="sxs-lookup"><span data-stu-id="3c05e-138">2</span></span>     | <span data-ttu-id="3c05e-139">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="3c05e-140">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-140">unicode</span></span>     |
| <span data-ttu-id="3c05e-141">3</span><span class="sxs-lookup"><span data-stu-id="3c05e-141">3</span></span>     | <span data-ttu-id="3c05e-142">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="3c05e-143">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3c05e-144">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3c05e-144">Remove Paths</span></span>



| <span data-ttu-id="3c05e-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="3c05e-145">Order</span></span> | <span data-ttu-id="3c05e-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="3c05e-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="3c05e-147">1</span><span class="sxs-lookup"><span data-stu-id="3c05e-147">1</span></span>     | <span data-ttu-id="3c05e-148">/app1/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="3c05e-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="3c05e-149">2</span><span class="sxs-lookup"><span data-stu-id="3c05e-149">2</span></span>     | <span data-ttu-id="3c05e-150">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="3c05e-151">3</span><span class="sxs-lookup"><span data-stu-id="3c05e-151">3</span></span>     | <span data-ttu-id="3c05e-152">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="3c05e-153">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="3c05e-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3c05e-154">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3c05e-154">Read Paths</span></span>



| <span data-ttu-id="3c05e-155">Pedido</span><span class="sxs-lookup"><span data-stu-id="3c05e-155">Order</span></span> | <span data-ttu-id="3c05e-156">Ruta</span><span class="sxs-lookup"><span data-stu-id="3c05e-156">Path</span></span>                | <span data-ttu-id="3c05e-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3c05e-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="3c05e-158">1</span><span class="sxs-lookup"><span data-stu-id="3c05e-158">1</span></span>     | <span data-ttu-id="3c05e-159">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="3c05e-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="3c05e-160">ascii</span><span class="sxs-lookup"><span data-stu-id="3c05e-160">ascii</span></span>       |
| <span data-ttu-id="3c05e-161">2</span><span class="sxs-lookup"><span data-stu-id="3c05e-161">2</span></span>     | <span data-ttu-id="3c05e-162">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="3c05e-163">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-163">unicode</span></span>     |
| <span data-ttu-id="3c05e-164">3</span><span class="sxs-lookup"><span data-stu-id="3c05e-164">3</span></span>     | <span data-ttu-id="3c05e-165">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="3c05e-166">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3c05e-167">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3c05e-167">Write Paths</span></span>



| <span data-ttu-id="3c05e-168">Pedido</span><span class="sxs-lookup"><span data-stu-id="3c05e-168">Order</span></span> | <span data-ttu-id="3c05e-169">Ruta</span><span class="sxs-lookup"><span data-stu-id="3c05e-169">Path</span></span>                | <span data-ttu-id="3c05e-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3c05e-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="3c05e-171">1</span><span class="sxs-lookup"><span data-stu-id="3c05e-171">1</span></span>     | <span data-ttu-id="3c05e-172">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="3c05e-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="3c05e-173">ascii</span><span class="sxs-lookup"><span data-stu-id="3c05e-173">ascii</span></span>       |
| <span data-ttu-id="3c05e-174">2</span><span class="sxs-lookup"><span data-stu-id="3c05e-174">2</span></span>     | <span data-ttu-id="3c05e-175">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="3c05e-176">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-176">unicode</span></span>     |
| <span data-ttu-id="3c05e-177">3</span><span class="sxs-lookup"><span data-stu-id="3c05e-177">3</span></span>     | <span data-ttu-id="3c05e-178">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="3c05e-179">unicode</span><span class="sxs-lookup"><span data-stu-id="3c05e-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3c05e-180">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3c05e-180">Remove Paths</span></span>



| <span data-ttu-id="3c05e-181">Pedido</span><span class="sxs-lookup"><span data-stu-id="3c05e-181">Order</span></span> | <span data-ttu-id="3c05e-182">Ruta</span><span class="sxs-lookup"><span data-stu-id="3c05e-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="3c05e-183">1</span><span class="sxs-lookup"><span data-stu-id="3c05e-183">1</span></span>     | <span data-ttu-id="3c05e-184">/IFD/{ushort = 272}</span><span class="sxs-lookup"><span data-stu-id="3c05e-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="3c05e-185">2</span><span class="sxs-lookup"><span data-stu-id="3c05e-185">2</span></span>     | <span data-ttu-id="3c05e-186">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="3c05e-187">3</span><span class="sxs-lookup"><span data-stu-id="3c05e-187">3</span></span>     | <span data-ttu-id="3c05e-188">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="3c05e-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3c05e-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c05e-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c05e-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c05e-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c05e-191">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="3c05e-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
