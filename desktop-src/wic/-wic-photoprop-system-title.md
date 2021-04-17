---
description: La Directiva de metadatos de la fotografía para la propiedad System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Directiva de metadatos de foto de System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706833"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="32e6c-103">Directiva de metadatos de foto de System. title</span><span class="sxs-lookup"><span data-stu-id="32e6c-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="32e6c-104">La Directiva de metadatos de la fotografía para la propiedad [System. title](../properties/props-system-title.md) .</span><span class="sxs-lookup"><span data-stu-id="32e6c-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="32e6c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="32e6c-105">PKEY</span></span>

<span data-ttu-id="32e6c-106">Título de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="32e6c-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="32e6c-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="32e6c-107">Containers</span></span>

<span data-ttu-id="32e6c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="32e6c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="32e6c-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="32e6c-109">Read-Only</span></span>

<span data-ttu-id="32e6c-110">No</span><span class="sxs-lookup"><span data-stu-id="32e6c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="32e6c-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="32e6c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="32e6c-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="32e6c-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="32e6c-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="32e6c-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="32e6c-114">VT \_ LPWStr o VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="32e6c-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="32e6c-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="32e6c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="32e6c-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="32e6c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="32e6c-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="32e6c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="32e6c-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="32e6c-118">Read Paths</span></span>



| <span data-ttu-id="32e6c-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="32e6c-119">Order</span></span> | <span data-ttu-id="32e6c-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="32e6c-120">Path</span></span>                                | <span data-ttu-id="32e6c-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="32e6c-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="32e6c-122">1</span><span class="sxs-lookup"><span data-stu-id="32e6c-122">1</span></span>     | <span data-ttu-id="32e6c-123">/app1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="32e6c-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="32e6c-124">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-124">unicode\_bytes</span></span> |
| <span data-ttu-id="32e6c-125">2</span><span class="sxs-lookup"><span data-stu-id="32e6c-125">2</span></span>     | <span data-ttu-id="32e6c-126">/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="32e6c-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="32e6c-127">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-127">unicode</span></span>        |
| <span data-ttu-id="32e6c-128">3</span><span class="sxs-lookup"><span data-stu-id="32e6c-128">3</span></span>     | <span data-ttu-id="32e6c-129">/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="32e6c-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="32e6c-130">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-130">unicode</span></span>        |
| <span data-ttu-id="32e6c-131">4</span><span class="sxs-lookup"><span data-stu-id="32e6c-131">4</span></span>     | <span data-ttu-id="32e6c-132">/app1/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="32e6c-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="32e6c-133">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-133">unicode</span></span>        |
| <span data-ttu-id="32e6c-134">5</span><span class="sxs-lookup"><span data-stu-id="32e6c-134">5</span></span>     | <span data-ttu-id="32e6c-135">/app1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="32e6c-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="32e6c-136">ascii</span><span class="sxs-lookup"><span data-stu-id="32e6c-136">ascii</span></span>          |
| <span data-ttu-id="32e6c-137">6</span><span class="sxs-lookup"><span data-stu-id="32e6c-137">6</span></span>     | <span data-ttu-id="32e6c-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="32e6c-139">7</span><span class="sxs-lookup"><span data-stu-id="32e6c-139">7</span></span>     | <span data-ttu-id="32e6c-140">/XMP/ <xmpalt> DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="32e6c-141">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-141">unicode</span></span>        |
| <span data-ttu-id="32e6c-142">8</span><span class="sxs-lookup"><span data-stu-id="32e6c-142">8</span></span>     | <span data-ttu-id="32e6c-143">/XMP/DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="32e6c-144">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-144">unicode</span></span>        |
| <span data-ttu-id="32e6c-145">9</span><span class="sxs-lookup"><span data-stu-id="32e6c-145">9</span></span>     | <span data-ttu-id="32e6c-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="32e6c-147">10</span><span class="sxs-lookup"><span data-stu-id="32e6c-147">10</span></span>    | <span data-ttu-id="32e6c-148">/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="32e6c-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="32e6c-149">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="32e6c-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="32e6c-150">Write Paths</span></span>



| <span data-ttu-id="32e6c-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="32e6c-151">Order</span></span> | <span data-ttu-id="32e6c-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="32e6c-152">Path</span></span>                                | <span data-ttu-id="32e6c-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="32e6c-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="32e6c-154">1</span><span class="sxs-lookup"><span data-stu-id="32e6c-154">1</span></span>     | <span data-ttu-id="32e6c-155">/app1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="32e6c-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="32e6c-156">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-156">unicode\_bytes</span></span> |
| <span data-ttu-id="32e6c-157">2</span><span class="sxs-lookup"><span data-stu-id="32e6c-157">2</span></span>     | <span data-ttu-id="32e6c-158">/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="32e6c-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="32e6c-159">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-159">unicode</span></span>        |
| <span data-ttu-id="32e6c-160">3</span><span class="sxs-lookup"><span data-stu-id="32e6c-160">3</span></span>     | <span data-ttu-id="32e6c-161">/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="32e6c-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="32e6c-162">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-162">unicode</span></span>        |
| <span data-ttu-id="32e6c-163">4</span><span class="sxs-lookup"><span data-stu-id="32e6c-163">4</span></span>     | <span data-ttu-id="32e6c-164">/app1/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="32e6c-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="32e6c-165">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-165">unicode</span></span>        |
| <span data-ttu-id="32e6c-166">5</span><span class="sxs-lookup"><span data-stu-id="32e6c-166">5</span></span>     | <span data-ttu-id="32e6c-167">/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="32e6c-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="32e6c-168">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-168">unicode</span></span>        |
| <span data-ttu-id="32e6c-169">6</span><span class="sxs-lookup"><span data-stu-id="32e6c-169">6</span></span>     | <span data-ttu-id="32e6c-170">/app1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="32e6c-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="32e6c-171">ascii</span><span class="sxs-lookup"><span data-stu-id="32e6c-171">ascii</span></span>          |
| <span data-ttu-id="32e6c-172">7</span><span class="sxs-lookup"><span data-stu-id="32e6c-172">7</span></span>     | <span data-ttu-id="32e6c-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="32e6c-174">8</span><span class="sxs-lookup"><span data-stu-id="32e6c-174">8</span></span>     | <span data-ttu-id="32e6c-175">/XMP/DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="32e6c-176">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-176">unicode</span></span>        |
| <span data-ttu-id="32e6c-177">9</span><span class="sxs-lookup"><span data-stu-id="32e6c-177">9</span></span>     | <span data-ttu-id="32e6c-178">/XMP/ <xmpalt> DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="32e6c-179">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="32e6c-180">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="32e6c-180">Remove Paths</span></span>



| <span data-ttu-id="32e6c-181">Pedido</span><span class="sxs-lookup"><span data-stu-id="32e6c-181">Order</span></span> | <span data-ttu-id="32e6c-182">Ruta</span><span class="sxs-lookup"><span data-stu-id="32e6c-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="32e6c-183">1</span><span class="sxs-lookup"><span data-stu-id="32e6c-183">1</span></span>     | <span data-ttu-id="32e6c-184">/app1/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="32e6c-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="32e6c-185">2</span><span class="sxs-lookup"><span data-stu-id="32e6c-185">2</span></span>     | <span data-ttu-id="32e6c-186">/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="32e6c-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="32e6c-187">3</span><span class="sxs-lookup"><span data-stu-id="32e6c-187">3</span></span>     | <span data-ttu-id="32e6c-188">/app1/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="32e6c-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="32e6c-189">4</span><span class="sxs-lookup"><span data-stu-id="32e6c-189">4</span></span>     | <span data-ttu-id="32e6c-190">/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="32e6c-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="32e6c-191">5</span><span class="sxs-lookup"><span data-stu-id="32e6c-191">5</span></span>     | <span data-ttu-id="32e6c-192">/app1/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="32e6c-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="32e6c-193">6</span><span class="sxs-lookup"><span data-stu-id="32e6c-193">6</span></span>     | <span data-ttu-id="32e6c-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="32e6c-195">7</span><span class="sxs-lookup"><span data-stu-id="32e6c-195">7</span></span>     | <span data-ttu-id="32e6c-196">/XMP/DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="32e6c-197">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="32e6c-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="32e6c-198">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="32e6c-198">Read Paths</span></span>



| <span data-ttu-id="32e6c-199">Pedido</span><span class="sxs-lookup"><span data-stu-id="32e6c-199">Order</span></span> | <span data-ttu-id="32e6c-200">Ruta</span><span class="sxs-lookup"><span data-stu-id="32e6c-200">Path</span></span>                                    | <span data-ttu-id="32e6c-201">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="32e6c-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="32e6c-202">1</span><span class="sxs-lookup"><span data-stu-id="32e6c-202">1</span></span>     | <span data-ttu-id="32e6c-203">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="32e6c-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="32e6c-204">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-204">unicode\_bytes</span></span> |
| <span data-ttu-id="32e6c-205">2</span><span class="sxs-lookup"><span data-stu-id="32e6c-205">2</span></span>     | <span data-ttu-id="32e6c-206">/IFD/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="32e6c-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="32e6c-207">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-207">unicode</span></span>        |
| <span data-ttu-id="32e6c-208">3</span><span class="sxs-lookup"><span data-stu-id="32e6c-208">3</span></span>     | <span data-ttu-id="32e6c-209">/IFD/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="32e6c-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="32e6c-210">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-210">unicode</span></span>        |
| <span data-ttu-id="32e6c-211">4</span><span class="sxs-lookup"><span data-stu-id="32e6c-211">4</span></span>     | <span data-ttu-id="32e6c-212">/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="32e6c-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="32e6c-213">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-213">unicode</span></span>        |
| <span data-ttu-id="32e6c-214">5</span><span class="sxs-lookup"><span data-stu-id="32e6c-214">5</span></span>     | <span data-ttu-id="32e6c-215">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="32e6c-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="32e6c-216">ascii</span><span class="sxs-lookup"><span data-stu-id="32e6c-216">ascii</span></span>          |
| <span data-ttu-id="32e6c-217">6</span><span class="sxs-lookup"><span data-stu-id="32e6c-217">6</span></span>     | <span data-ttu-id="32e6c-218">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="32e6c-219">7</span><span class="sxs-lookup"><span data-stu-id="32e6c-219">7</span></span>     | <span data-ttu-id="32e6c-220">/IFD/XMP/ <xmpalt> DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="32e6c-221">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-221">unicode</span></span>        |
| <span data-ttu-id="32e6c-222">8</span><span class="sxs-lookup"><span data-stu-id="32e6c-222">8</span></span>     | <span data-ttu-id="32e6c-223">/IFD/XMP/DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="32e6c-224">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-224">unicode</span></span>        |
| <span data-ttu-id="32e6c-225">9</span><span class="sxs-lookup"><span data-stu-id="32e6c-225">9</span></span>     | <span data-ttu-id="32e6c-226">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="32e6c-227">10</span><span class="sxs-lookup"><span data-stu-id="32e6c-227">10</span></span>    | <span data-ttu-id="32e6c-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="32e6c-229">11</span><span class="sxs-lookup"><span data-stu-id="32e6c-229">11</span></span>    | <span data-ttu-id="32e6c-230">/IFD/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="32e6c-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="32e6c-231">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="32e6c-232">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="32e6c-232">Write Paths</span></span>



| <span data-ttu-id="32e6c-233">Pedido</span><span class="sxs-lookup"><span data-stu-id="32e6c-233">Order</span></span> | <span data-ttu-id="32e6c-234">Ruta</span><span class="sxs-lookup"><span data-stu-id="32e6c-234">Path</span></span>                                    | <span data-ttu-id="32e6c-235">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="32e6c-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="32e6c-236">1</span><span class="sxs-lookup"><span data-stu-id="32e6c-236">1</span></span>     | <span data-ttu-id="32e6c-237">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="32e6c-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="32e6c-238">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-238">unicode\_bytes</span></span> |
| <span data-ttu-id="32e6c-239">2</span><span class="sxs-lookup"><span data-stu-id="32e6c-239">2</span></span>     | <span data-ttu-id="32e6c-240">/IFD/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="32e6c-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="32e6c-241">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-241">unicode</span></span>        |
| <span data-ttu-id="32e6c-242">3</span><span class="sxs-lookup"><span data-stu-id="32e6c-242">3</span></span>     | <span data-ttu-id="32e6c-243">/IFD/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="32e6c-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="32e6c-244">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-244">unicode</span></span>        |
| <span data-ttu-id="32e6c-245">4</span><span class="sxs-lookup"><span data-stu-id="32e6c-245">4</span></span>     | <span data-ttu-id="32e6c-246">/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="32e6c-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="32e6c-247">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-247">unicode</span></span>        |
| <span data-ttu-id="32e6c-248">5</span><span class="sxs-lookup"><span data-stu-id="32e6c-248">5</span></span>     | <span data-ttu-id="32e6c-249">/IFD/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="32e6c-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="32e6c-250">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-250">unicode</span></span>        |
| <span data-ttu-id="32e6c-251">6</span><span class="sxs-lookup"><span data-stu-id="32e6c-251">6</span></span>     | <span data-ttu-id="32e6c-252">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="32e6c-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="32e6c-253">ascii</span><span class="sxs-lookup"><span data-stu-id="32e6c-253">ascii</span></span>          |
| <span data-ttu-id="32e6c-254">7</span><span class="sxs-lookup"><span data-stu-id="32e6c-254">7</span></span>     | <span data-ttu-id="32e6c-255">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="32e6c-256">8</span><span class="sxs-lookup"><span data-stu-id="32e6c-256">8</span></span>     | <span data-ttu-id="32e6c-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="32e6c-258">9</span><span class="sxs-lookup"><span data-stu-id="32e6c-258">9</span></span>     | <span data-ttu-id="32e6c-259">/IFD/XMP/DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="32e6c-260">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-260">unicode</span></span>        |
| <span data-ttu-id="32e6c-261">10</span><span class="sxs-lookup"><span data-stu-id="32e6c-261">10</span></span>    | <span data-ttu-id="32e6c-262">/IFD/XMP/ <xmpalt> DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="32e6c-263">unicode</span><span class="sxs-lookup"><span data-stu-id="32e6c-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="32e6c-264">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="32e6c-264">Remove Paths</span></span>



| <span data-ttu-id="32e6c-265">Pedido</span><span class="sxs-lookup"><span data-stu-id="32e6c-265">Order</span></span> | <span data-ttu-id="32e6c-266">Ruta</span><span class="sxs-lookup"><span data-stu-id="32e6c-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="32e6c-267">1</span><span class="sxs-lookup"><span data-stu-id="32e6c-267">1</span></span>     | <span data-ttu-id="32e6c-268">/IFD/{ushort = 40091}</span><span class="sxs-lookup"><span data-stu-id="32e6c-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="32e6c-269">2</span><span class="sxs-lookup"><span data-stu-id="32e6c-269">2</span></span>     | <span data-ttu-id="32e6c-270">/IFD/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="32e6c-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="32e6c-271">3</span><span class="sxs-lookup"><span data-stu-id="32e6c-271">3</span></span>     | <span data-ttu-id="32e6c-272">/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="32e6c-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="32e6c-273">4</span><span class="sxs-lookup"><span data-stu-id="32e6c-273">4</span></span>     | <span data-ttu-id="32e6c-274">/IFD/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="32e6c-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="32e6c-275">5</span><span class="sxs-lookup"><span data-stu-id="32e6c-275">5</span></span>     | <span data-ttu-id="32e6c-276">/IFD/{ushort = 270}</span><span class="sxs-lookup"><span data-stu-id="32e6c-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="32e6c-277">6</span><span class="sxs-lookup"><span data-stu-id="32e6c-277">6</span></span>     | <span data-ttu-id="32e6c-278">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="32e6c-279">7</span><span class="sxs-lookup"><span data-stu-id="32e6c-279">7</span></span>     | <span data-ttu-id="32e6c-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="32e6c-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="32e6c-281">8</span><span class="sxs-lookup"><span data-stu-id="32e6c-281">8</span></span>     | <span data-ttu-id="32e6c-282">/IFD/XMP/DC: Descripción</span><span class="sxs-lookup"><span data-stu-id="32e6c-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="32e6c-283">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32e6c-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="32e6c-284">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32e6c-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32e6c-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="32e6c-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
