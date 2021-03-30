---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. isospeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Directiva de metadatos de fotografía de System. Photo. isospeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360919"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="7ab23-103">Directiva de metadatos de fotografía de System. Photo. isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="7ab23-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. isospeed](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="7ab23-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7ab23-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7ab23-105">PKEY</span></span>

<span data-ttu-id="7ab23-106">Isovelocidad de la \_ foto PKEY \_</span><span class="sxs-lookup"><span data-stu-id="7ab23-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="7ab23-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="7ab23-107">Containers</span></span>

<span data-ttu-id="7ab23-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7ab23-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7ab23-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7ab23-109">Read-Only</span></span>

<span data-ttu-id="7ab23-110">No</span><span class="sxs-lookup"><span data-stu-id="7ab23-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7ab23-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="7ab23-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7ab23-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="7ab23-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="7ab23-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="7ab23-113">Input Type</span></span>

<span data-ttu-id="7ab23-114">UShort</span><span class="sxs-lookup"><span data-stu-id="7ab23-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7ab23-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="7ab23-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7ab23-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="7ab23-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7ab23-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="7ab23-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7ab23-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7ab23-118">Read Paths</span></span>



| <span data-ttu-id="7ab23-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="7ab23-119">Order</span></span> | <span data-ttu-id="7ab23-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="7ab23-120">Path</span></span>                                    | <span data-ttu-id="7ab23-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7ab23-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="7ab23-122">1</span><span class="sxs-lookup"><span data-stu-id="7ab23-122">1</span></span>     | <span data-ttu-id="7ab23-123">/app1/IFD/Exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="7ab23-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="7ab23-124">ushort</span><span class="sxs-lookup"><span data-stu-id="7ab23-124">ushort</span></span>      |
| <span data-ttu-id="7ab23-125">2</span><span class="sxs-lookup"><span data-stu-id="7ab23-125">2</span></span>     | <span data-ttu-id="7ab23-126">/XMP/ <xmpseq> Exif: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="7ab23-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="7ab23-127">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-127">unicode</span></span>     |
| <span data-ttu-id="7ab23-128">3</span><span class="sxs-lookup"><span data-stu-id="7ab23-128">3</span></span>     | <span data-ttu-id="7ab23-129">/XMP/Exif: isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="7ab23-130">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7ab23-131">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7ab23-131">Write Paths</span></span>



| <span data-ttu-id="7ab23-132">Pedido</span><span class="sxs-lookup"><span data-stu-id="7ab23-132">Order</span></span> | <span data-ttu-id="7ab23-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="7ab23-133">Path</span></span>                                    | <span data-ttu-id="7ab23-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7ab23-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="7ab23-135">1</span><span class="sxs-lookup"><span data-stu-id="7ab23-135">1</span></span>     | <span data-ttu-id="7ab23-136">/app1/IFD/Exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="7ab23-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="7ab23-137">ushort</span><span class="sxs-lookup"><span data-stu-id="7ab23-137">ushort</span></span>      |
| <span data-ttu-id="7ab23-138">2</span><span class="sxs-lookup"><span data-stu-id="7ab23-138">2</span></span>     | <span data-ttu-id="7ab23-139">/XMP/ <xmpseq> Exif: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="7ab23-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="7ab23-140">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-140">unicode</span></span>     |
| <span data-ttu-id="7ab23-141">3</span><span class="sxs-lookup"><span data-stu-id="7ab23-141">3</span></span>     | <span data-ttu-id="7ab23-142">/XMP/Exif: isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="7ab23-143">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7ab23-144">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7ab23-144">Remove Paths</span></span>



| <span data-ttu-id="7ab23-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="7ab23-145">Order</span></span> | <span data-ttu-id="7ab23-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="7ab23-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="7ab23-147">1</span><span class="sxs-lookup"><span data-stu-id="7ab23-147">1</span></span>     | <span data-ttu-id="7ab23-148">/app1/IFD/Exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="7ab23-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="7ab23-149">2</span><span class="sxs-lookup"><span data-stu-id="7ab23-149">2</span></span>     | <span data-ttu-id="7ab23-150">/XMP/ <xmpseq> Exif: isospeedratings</span><span class="sxs-lookup"><span data-stu-id="7ab23-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="7ab23-151">3</span><span class="sxs-lookup"><span data-stu-id="7ab23-151">3</span></span>     | <span data-ttu-id="7ab23-152">/XMP/Exif: isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="7ab23-153">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="7ab23-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7ab23-154">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7ab23-154">Read Paths</span></span>



| <span data-ttu-id="7ab23-155">Pedido</span><span class="sxs-lookup"><span data-stu-id="7ab23-155">Order</span></span> | <span data-ttu-id="7ab23-156">Ruta</span><span class="sxs-lookup"><span data-stu-id="7ab23-156">Path</span></span>                                        | <span data-ttu-id="7ab23-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7ab23-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="7ab23-158">1</span><span class="sxs-lookup"><span data-stu-id="7ab23-158">1</span></span>     | <span data-ttu-id="7ab23-159">/IFD/Exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="7ab23-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="7ab23-160">ushort</span><span class="sxs-lookup"><span data-stu-id="7ab23-160">ushort</span></span>      |
| <span data-ttu-id="7ab23-161">2</span><span class="sxs-lookup"><span data-stu-id="7ab23-161">2</span></span>     | <span data-ttu-id="7ab23-162">/IFD/XMP/ <xmpseq> Exif: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="7ab23-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="7ab23-163">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-163">unicode</span></span>     |
| <span data-ttu-id="7ab23-164">3</span><span class="sxs-lookup"><span data-stu-id="7ab23-164">3</span></span>     | <span data-ttu-id="7ab23-165">/IFD/XMP/Exif: isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="7ab23-166">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7ab23-167">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7ab23-167">Write Paths</span></span>



| <span data-ttu-id="7ab23-168">Pedido</span><span class="sxs-lookup"><span data-stu-id="7ab23-168">Order</span></span> | <span data-ttu-id="7ab23-169">Ruta</span><span class="sxs-lookup"><span data-stu-id="7ab23-169">Path</span></span>                                        | <span data-ttu-id="7ab23-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7ab23-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="7ab23-171">1</span><span class="sxs-lookup"><span data-stu-id="7ab23-171">1</span></span>     | <span data-ttu-id="7ab23-172">/IFD/Exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="7ab23-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="7ab23-173">ushort</span><span class="sxs-lookup"><span data-stu-id="7ab23-173">ushort</span></span>      |
| <span data-ttu-id="7ab23-174">2</span><span class="sxs-lookup"><span data-stu-id="7ab23-174">2</span></span>     | <span data-ttu-id="7ab23-175">/IFD/XMP/ <xmpseq> Exif: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="7ab23-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="7ab23-176">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-176">unicode</span></span>     |
| <span data-ttu-id="7ab23-177">3</span><span class="sxs-lookup"><span data-stu-id="7ab23-177">3</span></span>     | <span data-ttu-id="7ab23-178">/IFD/XMP/Exif: isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="7ab23-179">unicode</span><span class="sxs-lookup"><span data-stu-id="7ab23-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7ab23-180">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7ab23-180">Remove Paths</span></span>



| <span data-ttu-id="7ab23-181">Pedido</span><span class="sxs-lookup"><span data-stu-id="7ab23-181">Order</span></span> | <span data-ttu-id="7ab23-182">Ruta</span><span class="sxs-lookup"><span data-stu-id="7ab23-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="7ab23-183">1</span><span class="sxs-lookup"><span data-stu-id="7ab23-183">1</span></span>     | <span data-ttu-id="7ab23-184">/IFD/Exif/{ushort = 34855}</span><span class="sxs-lookup"><span data-stu-id="7ab23-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="7ab23-185">2</span><span class="sxs-lookup"><span data-stu-id="7ab23-185">2</span></span>     | <span data-ttu-id="7ab23-186">/IFD/XMP/ <xmpseq> Exif: isospeedratings</span><span class="sxs-lookup"><span data-stu-id="7ab23-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="7ab23-187">3</span><span class="sxs-lookup"><span data-stu-id="7ab23-187">3</span></span>     | <span data-ttu-id="7ab23-188">/IFD/XMP/Exif: isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="7ab23-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab23-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ab23-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ab23-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ab23-191">System. Photo. isospeed</span><span class="sxs-lookup"><span data-stu-id="7ab23-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
