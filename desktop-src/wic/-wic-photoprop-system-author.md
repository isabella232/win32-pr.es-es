---
description: La Directiva de metadatos de la fotografía para la propiedad System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Directiva de metadatos de fotografía de System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720716"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="5f5d5-103">Directiva de metadatos de fotografía de System. Author</span><span class="sxs-lookup"><span data-stu-id="5f5d5-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="5f5d5-104">La Directiva de metadatos de la fotografía para la propiedad [System. Author](../properties/props-system-author.md) .</span><span class="sxs-lookup"><span data-stu-id="5f5d5-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5f5d5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5f5d5-105">PKEY</span></span>

<span data-ttu-id="5f5d5-106">Autor de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="5f5d5-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="5f5d5-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="5f5d5-107">Containers</span></span>

<span data-ttu-id="5f5d5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5f5d5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5f5d5-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f5d5-109">Read-Only</span></span>

<span data-ttu-id="5f5d5-110">No</span><span class="sxs-lookup"><span data-stu-id="5f5d5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5f5d5-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="5f5d5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5f5d5-112">VT \_ Vector \| VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="5f5d5-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="5f5d5-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="5f5d5-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="5f5d5-114">\_ \| Se prefiere VT vector VT \_ LPWStr, pero \_ también se acepta VT LPWStr.</span><span class="sxs-lookup"><span data-stu-id="5f5d5-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5f5d5-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="5f5d5-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5f5d5-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="5f5d5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5f5d5-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="5f5d5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5f5d5-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5f5d5-118">Read Paths</span></span>



| <span data-ttu-id="5f5d5-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="5f5d5-119">Order</span></span> | <span data-ttu-id="5f5d5-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="5f5d5-120">Path</span></span>                             | <span data-ttu-id="5f5d5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5f5d5-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="5f5d5-122">1</span><span class="sxs-lookup"><span data-stu-id="5f5d5-122">1</span></span>     | <span data-ttu-id="5f5d5-123">/app1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="5f5d5-124">ascii</span><span class="sxs-lookup"><span data-stu-id="5f5d5-124">ascii</span></span>          |
| <span data-ttu-id="5f5d5-125">2</span><span class="sxs-lookup"><span data-stu-id="5f5d5-125">2</span></span>     | <span data-ttu-id="5f5d5-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="5f5d5-127">3</span><span class="sxs-lookup"><span data-stu-id="5f5d5-127">3</span></span>     | <span data-ttu-id="5f5d5-128">/XMP/ <xmpseq> DC: creador</span><span class="sxs-lookup"><span data-stu-id="5f5d5-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="5f5d5-129">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-129">unicode</span></span>        |
| <span data-ttu-id="5f5d5-130">4</span><span class="sxs-lookup"><span data-stu-id="5f5d5-130">4</span></span>     | <span data-ttu-id="5f5d5-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="5f5d5-132">5</span><span class="sxs-lookup"><span data-stu-id="5f5d5-132">5</span></span>     | <span data-ttu-id="5f5d5-133">/app1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="5f5d5-134">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-134">unicode\_bytes</span></span> |
| <span data-ttu-id="5f5d5-135">6</span><span class="sxs-lookup"><span data-stu-id="5f5d5-135">6</span></span>     | <span data-ttu-id="5f5d5-136">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="5f5d5-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="5f5d5-137">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="5f5d5-138">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5f5d5-138">Write Paths</span></span>



| <span data-ttu-id="5f5d5-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="5f5d5-139">Order</span></span> | <span data-ttu-id="5f5d5-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="5f5d5-140">Path</span></span>                             | <span data-ttu-id="5f5d5-141">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5f5d5-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="5f5d5-142">1</span><span class="sxs-lookup"><span data-stu-id="5f5d5-142">1</span></span>     | <span data-ttu-id="5f5d5-143">/XMP/ <xmpseq> DC: creador</span><span class="sxs-lookup"><span data-stu-id="5f5d5-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="5f5d5-144">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-144">unicode</span></span>        |
| <span data-ttu-id="5f5d5-145">2</span><span class="sxs-lookup"><span data-stu-id="5f5d5-145">2</span></span>     | <span data-ttu-id="5f5d5-146">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="5f5d5-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="5f5d5-147">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-147">unicode</span></span>        |
| <span data-ttu-id="5f5d5-148">3</span><span class="sxs-lookup"><span data-stu-id="5f5d5-148">3</span></span>     | <span data-ttu-id="5f5d5-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="5f5d5-150">4</span><span class="sxs-lookup"><span data-stu-id="5f5d5-150">4</span></span>     | <span data-ttu-id="5f5d5-151">/app1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="5f5d5-152">ascii</span><span class="sxs-lookup"><span data-stu-id="5f5d5-152">ascii</span></span>          |
| <span data-ttu-id="5f5d5-153">5</span><span class="sxs-lookup"><span data-stu-id="5f5d5-153">5</span></span>     | <span data-ttu-id="5f5d5-154">/app1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="5f5d5-155">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="5f5d5-156">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5f5d5-156">Remove Paths</span></span>



| <span data-ttu-id="5f5d5-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="5f5d5-157">Order</span></span> | <span data-ttu-id="5f5d5-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="5f5d5-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="5f5d5-159">1</span><span class="sxs-lookup"><span data-stu-id="5f5d5-159">1</span></span>     | <span data-ttu-id="5f5d5-160">/XMP/DC: creador</span><span class="sxs-lookup"><span data-stu-id="5f5d5-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="5f5d5-161">2</span><span class="sxs-lookup"><span data-stu-id="5f5d5-161">2</span></span>     | <span data-ttu-id="5f5d5-162">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="5f5d5-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="5f5d5-163">3</span><span class="sxs-lookup"><span data-stu-id="5f5d5-163">3</span></span>     | <span data-ttu-id="5f5d5-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="5f5d5-165">4</span><span class="sxs-lookup"><span data-stu-id="5f5d5-165">4</span></span>     | <span data-ttu-id="5f5d5-166">/app1/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="5f5d5-167">5</span><span class="sxs-lookup"><span data-stu-id="5f5d5-167">5</span></span>     | <span data-ttu-id="5f5d5-168">/app1/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="5f5d5-169">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="5f5d5-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5f5d5-170">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5f5d5-170">Read Paths</span></span>



| <span data-ttu-id="5f5d5-171">Pedido</span><span class="sxs-lookup"><span data-stu-id="5f5d5-171">Order</span></span> | <span data-ttu-id="5f5d5-172">Ruta</span><span class="sxs-lookup"><span data-stu-id="5f5d5-172">Path</span></span>                              | <span data-ttu-id="5f5d5-173">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5f5d5-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="5f5d5-174">1</span><span class="sxs-lookup"><span data-stu-id="5f5d5-174">1</span></span>     | <span data-ttu-id="5f5d5-175">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="5f5d5-176">ascii</span><span class="sxs-lookup"><span data-stu-id="5f5d5-176">ascii</span></span>          |
| <span data-ttu-id="5f5d5-177">2</span><span class="sxs-lookup"><span data-stu-id="5f5d5-177">2</span></span>     | <span data-ttu-id="5f5d5-178">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="5f5d5-179">3</span><span class="sxs-lookup"><span data-stu-id="5f5d5-179">3</span></span>     | <span data-ttu-id="5f5d5-180">/IFD/XMP/ <xmpseq> DC: creador</span><span class="sxs-lookup"><span data-stu-id="5f5d5-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="5f5d5-181">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-181">unicode</span></span>        |
| <span data-ttu-id="5f5d5-182">4</span><span class="sxs-lookup"><span data-stu-id="5f5d5-182">4</span></span>     | <span data-ttu-id="5f5d5-183">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="5f5d5-184">5</span><span class="sxs-lookup"><span data-stu-id="5f5d5-184">5</span></span>     | <span data-ttu-id="5f5d5-185">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="5f5d5-186">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-186">unicode\_bytes</span></span> |
| <span data-ttu-id="5f5d5-187">6</span><span class="sxs-lookup"><span data-stu-id="5f5d5-187">6</span></span>     | <span data-ttu-id="5f5d5-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="5f5d5-189">7</span><span class="sxs-lookup"><span data-stu-id="5f5d5-189">7</span></span>     | <span data-ttu-id="5f5d5-190">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="5f5d5-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="5f5d5-191">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="5f5d5-192">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5f5d5-192">Write Paths</span></span>



| <span data-ttu-id="5f5d5-193">Pedido</span><span class="sxs-lookup"><span data-stu-id="5f5d5-193">Order</span></span> | <span data-ttu-id="5f5d5-194">Ruta</span><span class="sxs-lookup"><span data-stu-id="5f5d5-194">Path</span></span>                              | <span data-ttu-id="5f5d5-195">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5f5d5-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="5f5d5-196">1</span><span class="sxs-lookup"><span data-stu-id="5f5d5-196">1</span></span>     | <span data-ttu-id="5f5d5-197">/IFD/XMP/ <xmpseq> DC: creador</span><span class="sxs-lookup"><span data-stu-id="5f5d5-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="5f5d5-198">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-198">unicode</span></span>        |
| <span data-ttu-id="5f5d5-199">2</span><span class="sxs-lookup"><span data-stu-id="5f5d5-199">2</span></span>     | <span data-ttu-id="5f5d5-200">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="5f5d5-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="5f5d5-201">unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-201">unicode</span></span>        |
| <span data-ttu-id="5f5d5-202">3</span><span class="sxs-lookup"><span data-stu-id="5f5d5-202">3</span></span>     | <span data-ttu-id="5f5d5-203">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="5f5d5-204">4</span><span class="sxs-lookup"><span data-stu-id="5f5d5-204">4</span></span>     | <span data-ttu-id="5f5d5-205">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="5f5d5-206">\_Vector ASCII</span><span class="sxs-lookup"><span data-stu-id="5f5d5-206">ascii\_vector</span></span>  |
| <span data-ttu-id="5f5d5-207">5</span><span class="sxs-lookup"><span data-stu-id="5f5d5-207">5</span></span>     | <span data-ttu-id="5f5d5-208">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="5f5d5-209">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="5f5d5-209">unicode\_bytes</span></span> |
| <span data-ttu-id="5f5d5-210">6</span><span class="sxs-lookup"><span data-stu-id="5f5d5-210">6</span></span>     | <span data-ttu-id="5f5d5-211">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="5f5d5-212">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5f5d5-212">Remove Paths</span></span>



| <span data-ttu-id="5f5d5-213">Pedido</span><span class="sxs-lookup"><span data-stu-id="5f5d5-213">Order</span></span> | <span data-ttu-id="5f5d5-214">Ruta</span><span class="sxs-lookup"><span data-stu-id="5f5d5-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="5f5d5-215">1</span><span class="sxs-lookup"><span data-stu-id="5f5d5-215">1</span></span>     | <span data-ttu-id="5f5d5-216">/IFD/XMP/DC: creador</span><span class="sxs-lookup"><span data-stu-id="5f5d5-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="5f5d5-217">2</span><span class="sxs-lookup"><span data-stu-id="5f5d5-217">2</span></span>     | <span data-ttu-id="5f5d5-218">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="5f5d5-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="5f5d5-219">3</span><span class="sxs-lookup"><span data-stu-id="5f5d5-219">3</span></span>     | <span data-ttu-id="5f5d5-220">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="5f5d5-221">4</span><span class="sxs-lookup"><span data-stu-id="5f5d5-221">4</span></span>     | <span data-ttu-id="5f5d5-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="5f5d5-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="5f5d5-223">5</span><span class="sxs-lookup"><span data-stu-id="5f5d5-223">5</span></span>     | <span data-ttu-id="5f5d5-224">/IFD/{ushort = 315}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="5f5d5-225">6</span><span class="sxs-lookup"><span data-stu-id="5f5d5-225">6</span></span>     | <span data-ttu-id="5f5d5-226">/IFD/{ushort = 40093}</span><span class="sxs-lookup"><span data-stu-id="5f5d5-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="5f5d5-227">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f5d5-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f5d5-228">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f5d5-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f5d5-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="5f5d5-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
