---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Directiva de metadatos de la foto de System. Photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717149"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="ed76d-103">Directiva de metadatos de la foto de System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="ed76d-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="ed76d-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) .</span><span class="sxs-lookup"><span data-stu-id="ed76d-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ed76d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ed76d-105">PKEY</span></span>

<span data-ttu-id="ed76d-106">PKEY \_ Photo \_ DateTaken</span><span class="sxs-lookup"><span data-stu-id="ed76d-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="ed76d-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="ed76d-107">Containers</span></span>

<span data-ttu-id="ed76d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ed76d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ed76d-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed76d-109">Read-Only</span></span>

<span data-ttu-id="ed76d-110">No</span><span class="sxs-lookup"><span data-stu-id="ed76d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ed76d-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="ed76d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ed76d-112">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="ed76d-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="ed76d-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="ed76d-113">Input Type</span></span>

<span data-ttu-id="ed76d-114">DateTime</span><span class="sxs-lookup"><span data-stu-id="ed76d-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ed76d-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="ed76d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ed76d-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="ed76d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ed76d-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="ed76d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed76d-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-118">Read Paths</span></span>



| <span data-ttu-id="ed76d-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-119">Order</span></span> | <span data-ttu-id="ed76d-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-120">Path</span></span>                                  | <span data-ttu-id="ed76d-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ed76d-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="ed76d-122">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-122">1</span></span>     | <span data-ttu-id="ed76d-123">/app1/IFD/Exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="ed76d-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="ed76d-124">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-124">ascii</span></span>       |
| <span data-ttu-id="ed76d-125">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-125">2</span></span>     | <span data-ttu-id="ed76d-126">/app13/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="ed76d-127">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-127">unicode</span></span>     |
| <span data-ttu-id="ed76d-128">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-128">3</span></span>     | <span data-ttu-id="ed76d-129">/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="ed76d-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="ed76d-130">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-130">unicode</span></span>     |
| <span data-ttu-id="ed76d-131">4</span><span class="sxs-lookup"><span data-stu-id="ed76d-131">4</span></span>     | <span data-ttu-id="ed76d-132">/app1/IFD/Exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="ed76d-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="ed76d-133">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-133">ascii</span></span>       |
| <span data-ttu-id="ed76d-134">5</span><span class="sxs-lookup"><span data-stu-id="ed76d-134">5</span></span>     | <span data-ttu-id="ed76d-135">/app13/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="ed76d-136">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-136">unicode</span></span>     |
| <span data-ttu-id="ed76d-137">6</span><span class="sxs-lookup"><span data-stu-id="ed76d-137">6</span></span>     | <span data-ttu-id="ed76d-138">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="ed76d-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="ed76d-139">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed76d-140">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-140">Write Paths</span></span>



| <span data-ttu-id="ed76d-141">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-141">Order</span></span> | <span data-ttu-id="ed76d-142">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-142">Path</span></span>                                  | <span data-ttu-id="ed76d-143">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ed76d-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="ed76d-144">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-144">1</span></span>     | <span data-ttu-id="ed76d-145">/app1/IFD/Exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="ed76d-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="ed76d-146">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-146">ascii</span></span>       |
| <span data-ttu-id="ed76d-147">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-147">2</span></span>     | <span data-ttu-id="ed76d-148">/app13/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="ed76d-149">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-149">unicode</span></span>     |
| <span data-ttu-id="ed76d-150">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-150">3</span></span>     | <span data-ttu-id="ed76d-151">/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="ed76d-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="ed76d-152">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-152">unicode</span></span>     |
| <span data-ttu-id="ed76d-153">4</span><span class="sxs-lookup"><span data-stu-id="ed76d-153">4</span></span>     | <span data-ttu-id="ed76d-154">/app1/IFD/Exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="ed76d-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="ed76d-155">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-155">ascii</span></span>       |
| <span data-ttu-id="ed76d-156">5</span><span class="sxs-lookup"><span data-stu-id="ed76d-156">5</span></span>     | <span data-ttu-id="ed76d-157">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="ed76d-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="ed76d-158">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed76d-159">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-159">Remove Paths</span></span>



| <span data-ttu-id="ed76d-160">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-160">Order</span></span> | <span data-ttu-id="ed76d-161">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="ed76d-162">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-162">1</span></span>     | <span data-ttu-id="ed76d-163">/app1/IFD/Exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="ed76d-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="ed76d-164">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-164">2</span></span>     | <span data-ttu-id="ed76d-165">/app1/IFD/Exif/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="ed76d-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="ed76d-166">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-166">3</span></span>     | <span data-ttu-id="ed76d-167">/app1/IFD/Exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="ed76d-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="ed76d-168">4</span><span class="sxs-lookup"><span data-stu-id="ed76d-168">4</span></span>     | <span data-ttu-id="ed76d-169">/app1/IFD/Exif/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="ed76d-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="ed76d-170">5</span><span class="sxs-lookup"><span data-stu-id="ed76d-170">5</span></span>     | <span data-ttu-id="ed76d-171">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="ed76d-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="ed76d-172">6</span><span class="sxs-lookup"><span data-stu-id="ed76d-172">6</span></span>     | <span data-ttu-id="ed76d-173">/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="ed76d-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="ed76d-174">7</span><span class="sxs-lookup"><span data-stu-id="ed76d-174">7</span></span>     | <span data-ttu-id="ed76d-175">/app13/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="ed76d-176">8</span><span class="sxs-lookup"><span data-stu-id="ed76d-176">8</span></span>     | <span data-ttu-id="ed76d-177">/app13/IRB/8bimiptc/IPTC/Time creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="ed76d-178">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="ed76d-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed76d-179">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-179">Read Paths</span></span>



| <span data-ttu-id="ed76d-180">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-180">Order</span></span> | <span data-ttu-id="ed76d-181">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-181">Path</span></span>                                | <span data-ttu-id="ed76d-182">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ed76d-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="ed76d-183">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-183">1</span></span>     | <span data-ttu-id="ed76d-184">/IFD/Exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="ed76d-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="ed76d-185">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-185">ascii</span></span>       |
| <span data-ttu-id="ed76d-186">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-186">2</span></span>     | <span data-ttu-id="ed76d-187">/IFD/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="ed76d-188">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-188">unicode</span></span>     |
| <span data-ttu-id="ed76d-189">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-189">3</span></span>     | <span data-ttu-id="ed76d-190">/IFD/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="ed76d-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="ed76d-191">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-191">unicode</span></span>     |
| <span data-ttu-id="ed76d-192">4</span><span class="sxs-lookup"><span data-stu-id="ed76d-192">4</span></span>     | <span data-ttu-id="ed76d-193">/IFD/Exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="ed76d-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="ed76d-194">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-194">ascii</span></span>       |
| <span data-ttu-id="ed76d-195">5</span><span class="sxs-lookup"><span data-stu-id="ed76d-195">5</span></span>     | <span data-ttu-id="ed76d-196">/IFD/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="ed76d-197">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-197">unicode</span></span>     |
| <span data-ttu-id="ed76d-198">6</span><span class="sxs-lookup"><span data-stu-id="ed76d-198">6</span></span>     | <span data-ttu-id="ed76d-199">/IFD/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="ed76d-200">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-200">unicode</span></span>     |
| <span data-ttu-id="ed76d-201">7</span><span class="sxs-lookup"><span data-stu-id="ed76d-201">7</span></span>     | <span data-ttu-id="ed76d-202">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="ed76d-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="ed76d-203">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ed76d-204">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-204">Write Paths</span></span>



| <span data-ttu-id="ed76d-205">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-205">Order</span></span> | <span data-ttu-id="ed76d-206">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-206">Path</span></span>                                | <span data-ttu-id="ed76d-207">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ed76d-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="ed76d-208">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-208">1</span></span>     | <span data-ttu-id="ed76d-209">/IFD/Exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="ed76d-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="ed76d-210">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-210">ascii</span></span>       |
| <span data-ttu-id="ed76d-211">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-211">2</span></span>     | <span data-ttu-id="ed76d-212">/IFD/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="ed76d-213">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-213">unicode</span></span>     |
| <span data-ttu-id="ed76d-214">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-214">3</span></span>     | <span data-ttu-id="ed76d-215">/IFD/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="ed76d-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="ed76d-216">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-216">unicode</span></span>     |
| <span data-ttu-id="ed76d-217">4</span><span class="sxs-lookup"><span data-stu-id="ed76d-217">4</span></span>     | <span data-ttu-id="ed76d-218">/IFD/Exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="ed76d-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="ed76d-219">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-219">ascii</span></span>       |
| <span data-ttu-id="ed76d-220">5</span><span class="sxs-lookup"><span data-stu-id="ed76d-220">5</span></span>     | <span data-ttu-id="ed76d-221">/IFD/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="ed76d-222">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-222">unicode</span></span>     |
| <span data-ttu-id="ed76d-223">6</span><span class="sxs-lookup"><span data-stu-id="ed76d-223">6</span></span>     | <span data-ttu-id="ed76d-224">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="ed76d-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="ed76d-225">unicode</span><span class="sxs-lookup"><span data-stu-id="ed76d-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ed76d-226">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-226">Remove Paths</span></span>



| <span data-ttu-id="ed76d-227">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-227">Order</span></span> | <span data-ttu-id="ed76d-228">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="ed76d-229">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-229">1</span></span>     | <span data-ttu-id="ed76d-230">/IFD/Exif/{ushort = 36867}</span><span class="sxs-lookup"><span data-stu-id="ed76d-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="ed76d-231">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-231">2</span></span>     | <span data-ttu-id="ed76d-232">/IFD/Exif/{ushort = 37521}</span><span class="sxs-lookup"><span data-stu-id="ed76d-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="ed76d-233">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-233">3</span></span>     | <span data-ttu-id="ed76d-234">/IFD/Exif/{ushort = 36868}</span><span class="sxs-lookup"><span data-stu-id="ed76d-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="ed76d-235">4</span><span class="sxs-lookup"><span data-stu-id="ed76d-235">4</span></span>     | <span data-ttu-id="ed76d-236">/IFD/Exif/{ushort = 37522}</span><span class="sxs-lookup"><span data-stu-id="ed76d-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="ed76d-237">5</span><span class="sxs-lookup"><span data-stu-id="ed76d-237">5</span></span>     | <span data-ttu-id="ed76d-238">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="ed76d-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="ed76d-239">6</span><span class="sxs-lookup"><span data-stu-id="ed76d-239">6</span></span>     | <span data-ttu-id="ed76d-240">/IFD/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="ed76d-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="ed76d-241">7</span><span class="sxs-lookup"><span data-stu-id="ed76d-241">7</span></span>     | <span data-ttu-id="ed76d-242">/IFD/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="ed76d-243">8</span><span class="sxs-lookup"><span data-stu-id="ed76d-243">8</span></span>     | <span data-ttu-id="ed76d-244">/IFD/IPTC/Time creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="ed76d-245">9</span><span class="sxs-lookup"><span data-stu-id="ed76d-245">9</span></span>     | <span data-ttu-id="ed76d-246">/IFD/IRB/8bimiptc/IPTC/Date creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="ed76d-247">10</span><span class="sxs-lookup"><span data-stu-id="ed76d-247">10</span></span>    | <span data-ttu-id="ed76d-248">/IFD/IRB/8bimiptc/IPTC/Time creado</span><span class="sxs-lookup"><span data-stu-id="ed76d-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="ed76d-249">Directiva PNG</span><span class="sxs-lookup"><span data-stu-id="ed76d-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ed76d-250">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-250">Read Paths</span></span>



| <span data-ttu-id="ed76d-251">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-251">Order</span></span> | <span data-ttu-id="ed76d-252">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-252">Path</span></span>                      | <span data-ttu-id="ed76d-253">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ed76d-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ed76d-254">1</span><span class="sxs-lookup"><span data-stu-id="ed76d-254">1</span></span>     | <span data-ttu-id="ed76d-255">/\[\*\]Hora de creación y texto</span><span class="sxs-lookup"><span data-stu-id="ed76d-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="ed76d-256">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="ed76d-257">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-257">Write Paths</span></span>



| <span data-ttu-id="ed76d-258">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-258">Order</span></span> | <span data-ttu-id="ed76d-259">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-259">Path</span></span>                      | <span data-ttu-id="ed76d-260">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ed76d-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ed76d-261">2</span><span class="sxs-lookup"><span data-stu-id="ed76d-261">2</span></span>     | <span data-ttu-id="ed76d-262">/\[\*\]Hora de creación y texto</span><span class="sxs-lookup"><span data-stu-id="ed76d-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="ed76d-263">ascii</span><span class="sxs-lookup"><span data-stu-id="ed76d-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="ed76d-264">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ed76d-264">Remove Paths</span></span>



| <span data-ttu-id="ed76d-265">Pedido</span><span class="sxs-lookup"><span data-stu-id="ed76d-265">Order</span></span> | <span data-ttu-id="ed76d-266">Ruta</span><span class="sxs-lookup"><span data-stu-id="ed76d-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ed76d-267">3</span><span class="sxs-lookup"><span data-stu-id="ed76d-267">3</span></span>     | <span data-ttu-id="ed76d-268">/\[\*\]Hora de creación y texto</span><span class="sxs-lookup"><span data-stu-id="ed76d-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ed76d-269">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed76d-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed76d-270">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed76d-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed76d-271">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="ed76d-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
