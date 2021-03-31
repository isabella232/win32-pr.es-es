---
description: La Directiva de metadatos de la fotografía para la propiedad System. keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Directiva de metadatos de la foto System. keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278636"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="9b67b-103">Directiva de metadatos de la foto System. keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="9b67b-104">La Directiva de metadatos de la fotografía para la propiedad [System. keywords](../properties/props-system-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="9b67b-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9b67b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9b67b-105">PKEY</span></span>

<span data-ttu-id="9b67b-106">\_Palabras clave de PKEY</span><span class="sxs-lookup"><span data-stu-id="9b67b-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="9b67b-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="9b67b-107">Containers</span></span>

<span data-ttu-id="9b67b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9b67b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9b67b-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b67b-109">Read-Only</span></span>

<span data-ttu-id="9b67b-110">No</span><span class="sxs-lookup"><span data-stu-id="9b67b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9b67b-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="9b67b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9b67b-112">VT \_ Vector \| VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="9b67b-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9b67b-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="9b67b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9b67b-114">\_ \| Se prefiere VT vector VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="9b67b-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="9b67b-115">\_También se acepta un VT LPWStr que contenga una cadena delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="9b67b-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9b67b-116">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="9b67b-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="9b67b-117">Se combinan los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="9b67b-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9b67b-118">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="9b67b-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9b67b-119">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9b67b-119">Read Paths</span></span>



| <span data-ttu-id="9b67b-120">Pedido</span><span class="sxs-lookup"><span data-stu-id="9b67b-120">Order</span></span> | <span data-ttu-id="9b67b-121">Ruta</span><span class="sxs-lookup"><span data-stu-id="9b67b-121">Path</span></span>                              | <span data-ttu-id="9b67b-122">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9b67b-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="9b67b-123">1</span><span class="sxs-lookup"><span data-stu-id="9b67b-123">1</span></span>     | <span data-ttu-id="9b67b-124">/XMP/ <xmpbag> DC: asunto</span><span class="sxs-lookup"><span data-stu-id="9b67b-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="9b67b-125">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-125">unicode</span></span>        |
| <span data-ttu-id="9b67b-126">2</span><span class="sxs-lookup"><span data-stu-id="9b67b-126">2</span></span>     | <span data-ttu-id="9b67b-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="9b67b-128">3</span><span class="sxs-lookup"><span data-stu-id="9b67b-128">3</span></span>     | <span data-ttu-id="9b67b-129">/app1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="9b67b-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="9b67b-130">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-130">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-131">4</span><span class="sxs-lookup"><span data-stu-id="9b67b-131">4</span></span>     | <span data-ttu-id="9b67b-132">/app1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="9b67b-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="9b67b-133">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="9b67b-134">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9b67b-134">Write Paths</span></span>



| <span data-ttu-id="9b67b-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="9b67b-135">Order</span></span> | <span data-ttu-id="9b67b-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="9b67b-136">Path</span></span>                                              | <span data-ttu-id="9b67b-137">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9b67b-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="9b67b-138">1</span><span class="sxs-lookup"><span data-stu-id="9b67b-138">1</span></span>     | <span data-ttu-id="9b67b-139">/XMP/ <xmpbag> DC: asunto</span><span class="sxs-lookup"><span data-stu-id="9b67b-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="9b67b-140">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-140">unicode</span></span>        |
| <span data-ttu-id="9b67b-141">2</span><span class="sxs-lookup"><span data-stu-id="9b67b-141">2</span></span>     | <span data-ttu-id="9b67b-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="9b67b-143">3</span><span class="sxs-lookup"><span data-stu-id="9b67b-143">3</span></span>     | <span data-ttu-id="9b67b-144">/app1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="9b67b-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="9b67b-145">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-145">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-146">4</span><span class="sxs-lookup"><span data-stu-id="9b67b-146">4</span></span>     | <span data-ttu-id="9b67b-147">/app1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="9b67b-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="9b67b-148">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-148">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-149">5</span><span class="sxs-lookup"><span data-stu-id="9b67b-149">5</span></span>     | <span data-ttu-id="9b67b-150">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="9b67b-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="9b67b-151">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-151">unicode</span></span>        |
| <span data-ttu-id="9b67b-152">6</span><span class="sxs-lookup"><span data-stu-id="9b67b-152">6</span></span>     | <span data-ttu-id="9b67b-153">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="9b67b-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="9b67b-154">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="9b67b-155">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9b67b-155">Remove Paths</span></span>



| <span data-ttu-id="9b67b-156">Pedido</span><span class="sxs-lookup"><span data-stu-id="9b67b-156">Order</span></span> | <span data-ttu-id="9b67b-157">Ruta</span><span class="sxs-lookup"><span data-stu-id="9b67b-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="9b67b-158">1</span><span class="sxs-lookup"><span data-stu-id="9b67b-158">1</span></span>     | <span data-ttu-id="9b67b-159">/XMP/DC: asunto</span><span class="sxs-lookup"><span data-stu-id="9b67b-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="9b67b-160">2</span><span class="sxs-lookup"><span data-stu-id="9b67b-160">2</span></span>     | <span data-ttu-id="9b67b-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="9b67b-162">3</span><span class="sxs-lookup"><span data-stu-id="9b67b-162">3</span></span>     | <span data-ttu-id="9b67b-163">/app1/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="9b67b-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="9b67b-164">4</span><span class="sxs-lookup"><span data-stu-id="9b67b-164">4</span></span>     | <span data-ttu-id="9b67b-165">/app1/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="9b67b-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="9b67b-166">5</span><span class="sxs-lookup"><span data-stu-id="9b67b-166">5</span></span>     | <span data-ttu-id="9b67b-167">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="9b67b-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="9b67b-168">6</span><span class="sxs-lookup"><span data-stu-id="9b67b-168">6</span></span>     | <span data-ttu-id="9b67b-169">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="9b67b-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="9b67b-170">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="9b67b-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9b67b-171">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9b67b-171">Read Paths</span></span>



| <span data-ttu-id="9b67b-172">Pedido</span><span class="sxs-lookup"><span data-stu-id="9b67b-172">Order</span></span> | <span data-ttu-id="9b67b-173">Ruta</span><span class="sxs-lookup"><span data-stu-id="9b67b-173">Path</span></span>                              | <span data-ttu-id="9b67b-174">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9b67b-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="9b67b-175">1</span><span class="sxs-lookup"><span data-stu-id="9b67b-175">1</span></span>     | <span data-ttu-id="9b67b-176">/IFD/XMP/ <xmpbag> DC: asunto</span><span class="sxs-lookup"><span data-stu-id="9b67b-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="9b67b-177">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-177">unicode</span></span>        |
| <span data-ttu-id="9b67b-178">2</span><span class="sxs-lookup"><span data-stu-id="9b67b-178">2</span></span>     | <span data-ttu-id="9b67b-179">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="9b67b-180">3</span><span class="sxs-lookup"><span data-stu-id="9b67b-180">3</span></span>     | <span data-ttu-id="9b67b-181">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="9b67b-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="9b67b-182">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-182">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-183">4</span><span class="sxs-lookup"><span data-stu-id="9b67b-183">4</span></span>     | <span data-ttu-id="9b67b-184">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="9b67b-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="9b67b-185">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-185">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-186">5</span><span class="sxs-lookup"><span data-stu-id="9b67b-186">5</span></span>     | <span data-ttu-id="9b67b-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="9b67b-188">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9b67b-188">Write Paths</span></span>



| <span data-ttu-id="9b67b-189">Pedido</span><span class="sxs-lookup"><span data-stu-id="9b67b-189">Order</span></span> | <span data-ttu-id="9b67b-190">Ruta</span><span class="sxs-lookup"><span data-stu-id="9b67b-190">Path</span></span>                                                             | <span data-ttu-id="9b67b-191">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9b67b-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="9b67b-192">1</span><span class="sxs-lookup"><span data-stu-id="9b67b-192">1</span></span>     | <span data-ttu-id="9b67b-193">/IFD/XMP/ <xmpbag> DC: asunto</span><span class="sxs-lookup"><span data-stu-id="9b67b-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="9b67b-194">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-194">unicode</span></span>        |
| <span data-ttu-id="9b67b-195">2</span><span class="sxs-lookup"><span data-stu-id="9b67b-195">2</span></span>     | <span data-ttu-id="9b67b-196">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="9b67b-197">3</span><span class="sxs-lookup"><span data-stu-id="9b67b-197">3</span></span>     | <span data-ttu-id="9b67b-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="9b67b-199">4</span><span class="sxs-lookup"><span data-stu-id="9b67b-199">4</span></span>     | <span data-ttu-id="9b67b-200">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="9b67b-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="9b67b-201">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-201">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-202">5</span><span class="sxs-lookup"><span data-stu-id="9b67b-202">5</span></span>     | <span data-ttu-id="9b67b-203">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="9b67b-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="9b67b-204">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-204">unicode\_bytes</span></span> |
| <span data-ttu-id="9b67b-205">6</span><span class="sxs-lookup"><span data-stu-id="9b67b-205">6</span></span>     | <span data-ttu-id="9b67b-206">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="9b67b-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="9b67b-207">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-207">unicode</span></span>        |
| <span data-ttu-id="9b67b-208">7</span><span class="sxs-lookup"><span data-stu-id="9b67b-208">7</span></span>     | <span data-ttu-id="9b67b-209">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="9b67b-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="9b67b-210">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-210">unicode</span></span>        |
| <span data-ttu-id="9b67b-211">8</span><span class="sxs-lookup"><span data-stu-id="9b67b-211">8</span></span>     | <span data-ttu-id="9b67b-212">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="9b67b-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="9b67b-213">unicode</span><span class="sxs-lookup"><span data-stu-id="9b67b-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="9b67b-214">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9b67b-214">Remove Paths</span></span>



| <span data-ttu-id="9b67b-215">Pedido</span><span class="sxs-lookup"><span data-stu-id="9b67b-215">Order</span></span> | <span data-ttu-id="9b67b-216">Ruta</span><span class="sxs-lookup"><span data-stu-id="9b67b-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="9b67b-217">1</span><span class="sxs-lookup"><span data-stu-id="9b67b-217">1</span></span>     | <span data-ttu-id="9b67b-218">/IFD/XMP/DC: asunto</span><span class="sxs-lookup"><span data-stu-id="9b67b-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="9b67b-219">2</span><span class="sxs-lookup"><span data-stu-id="9b67b-219">2</span></span>     | <span data-ttu-id="9b67b-220">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="9b67b-221">3</span><span class="sxs-lookup"><span data-stu-id="9b67b-221">3</span></span>     | <span data-ttu-id="9b67b-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="9b67b-223">4</span><span class="sxs-lookup"><span data-stu-id="9b67b-223">4</span></span>     | <span data-ttu-id="9b67b-224">/IFD/{ushort = 18247}</span><span class="sxs-lookup"><span data-stu-id="9b67b-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="9b67b-225">5</span><span class="sxs-lookup"><span data-stu-id="9b67b-225">5</span></span>     | <span data-ttu-id="9b67b-226">/IFD/{ushort = 40094}</span><span class="sxs-lookup"><span data-stu-id="9b67b-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="9b67b-227">6</span><span class="sxs-lookup"><span data-stu-id="9b67b-227">6</span></span>     | <span data-ttu-id="9b67b-228">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="9b67b-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="9b67b-229">7</span><span class="sxs-lookup"><span data-stu-id="9b67b-229">7</span></span>     | <span data-ttu-id="9b67b-230">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="9b67b-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="9b67b-231">8</span><span class="sxs-lookup"><span data-stu-id="9b67b-231">8</span></span>     | <span data-ttu-id="9b67b-232">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="9b67b-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="9b67b-233">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b67b-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b67b-234">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b67b-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b67b-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="9b67b-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
