---
description: La Directiva de metadatos de la fotografía para la propiedad System. Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Directiva de metadatos de fotos de System. Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716897"
---
# <a name="systemcopyright-photo-metadata-policy"></a><span data-ttu-id="6a8ff-103">Directiva de metadatos de fotos de System. Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-103">System.Copyright Photo Metadata Policy</span></span>

<span data-ttu-id="6a8ff-104">La Directiva de metadatos de la fotografía para la propiedad [System. Copyright](../properties/props-system-copyright.md) .</span><span class="sxs-lookup"><span data-stu-id="6a8ff-104">The photo metadata policy for the [System.Copyright](../properties/props-system-copyright.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6a8ff-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6a8ff-105">PKEY</span></span>

<span data-ttu-id="6a8ff-106">Copyright de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="6a8ff-106">PKEY\_Copyright</span></span>

### <a name="containers"></a><span data-ttu-id="6a8ff-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="6a8ff-107">Containers</span></span>

<span data-ttu-id="6a8ff-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6a8ff-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6a8ff-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a8ff-109">Read-Only</span></span>

<span data-ttu-id="6a8ff-110">No</span><span class="sxs-lookup"><span data-stu-id="6a8ff-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6a8ff-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="6a8ff-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6a8ff-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="6a8ff-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="6a8ff-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="6a8ff-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="6a8ff-114">String</span><span class="sxs-lookup"><span data-stu-id="6a8ff-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6a8ff-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6a8ff-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="6a8ff-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6a8ff-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="6a8ff-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a8ff-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6a8ff-118">Read Paths</span></span>



| <span data-ttu-id="6a8ff-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="6a8ff-119">Order</span></span> | <span data-ttu-id="6a8ff-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a8ff-120">Path</span></span>                                      | <span data-ttu-id="6a8ff-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a8ff-121">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="6a8ff-122">/app1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="6a8ff-122">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="6a8ff-123">ascii</span><span class="sxs-lookup"><span data-stu-id="6a8ff-123">ascii</span></span>       |
|       | <span data-ttu-id="6a8ff-124">Aviso de/app13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-124">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="6a8ff-125">/XMP/ <xmpalt> DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-125">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="6a8ff-126">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-126">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-127">/XMP/DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-127">/xmp/dc:rights</span></span>                            | <span data-ttu-id="6a8ff-128">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-128">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-129">Aviso de/app13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-129">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6a8ff-130">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6a8ff-130">Write Paths</span></span>



| <span data-ttu-id="6a8ff-131">Pedido</span><span class="sxs-lookup"><span data-stu-id="6a8ff-131">Order</span></span> | <span data-ttu-id="6a8ff-132">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a8ff-132">Path</span></span>                                      | <span data-ttu-id="6a8ff-133">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a8ff-133">Disk Format</span></span> |
|-------|-------------------------------------------|-------------|
|       | <span data-ttu-id="6a8ff-134">/XMP/DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-134">/xmp/dc:rights</span></span>                            | <span data-ttu-id="6a8ff-135">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-135">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-136">/XMP/ <xmpalt> DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-136">/xmp/<xmpalt>dc:rights</span></span>              | <span data-ttu-id="6a8ff-137">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-137">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-138">Aviso de/app13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-138">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="6a8ff-139">/app1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="6a8ff-139">/app1/ifd/{ushort=33432}</span></span>                  | <span data-ttu-id="6a8ff-140">ascii</span><span class="sxs-lookup"><span data-stu-id="6a8ff-140">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="6a8ff-141">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6a8ff-141">Remove Paths</span></span>



| <span data-ttu-id="6a8ff-142">Pedido</span><span class="sxs-lookup"><span data-stu-id="6a8ff-142">Order</span></span> | <span data-ttu-id="6a8ff-143">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a8ff-143">Path</span></span>                                      |
|-------|-------------------------------------------|
|       | <span data-ttu-id="6a8ff-144">/XMP/DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-144">/xmp/dc:rights</span></span>                            |
|       | <span data-ttu-id="6a8ff-145">Aviso de/app13/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-145">/app13/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="6a8ff-146">/app1/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="6a8ff-146">/app1/ifd/{ushort=33432}</span></span>                  |



 

### <a name="tiff-policy"></a><span data-ttu-id="6a8ff-147">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="6a8ff-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a8ff-148">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6a8ff-148">Read Paths</span></span>



| <span data-ttu-id="6a8ff-149">Pedido</span><span class="sxs-lookup"><span data-stu-id="6a8ff-149">Order</span></span> | <span data-ttu-id="6a8ff-150">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a8ff-150">Path</span></span>                                    | <span data-ttu-id="6a8ff-151">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a8ff-151">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="6a8ff-152">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="6a8ff-152">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="6a8ff-153">ascii</span><span class="sxs-lookup"><span data-stu-id="6a8ff-153">ascii</span></span>       |
|       | <span data-ttu-id="6a8ff-154">Aviso de/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-154">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="6a8ff-155">/IFD/XMP/ <xmpalt> DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-155">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="6a8ff-156">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-156">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-157">/IFD/XMP/DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-157">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="6a8ff-158">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-158">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-159">Aviso de/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-159">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="6a8ff-160">Aviso de/IFD/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-160">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6a8ff-161">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6a8ff-161">Write Paths</span></span>



| <span data-ttu-id="6a8ff-162">Pedido</span><span class="sxs-lookup"><span data-stu-id="6a8ff-162">Order</span></span> | <span data-ttu-id="6a8ff-163">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a8ff-163">Path</span></span>                                    | <span data-ttu-id="6a8ff-164">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a8ff-164">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
|       | <span data-ttu-id="6a8ff-165">/IFD/XMP/DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-165">/ifd/xmp/dc:rights</span></span>                      | <span data-ttu-id="6a8ff-166">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-166">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-167">/IFD/XMP/ <xmpalt> DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-167">/ifd/xmp/<xmpalt>dc:rights</span></span>        | <span data-ttu-id="6a8ff-168">unicode</span><span class="sxs-lookup"><span data-stu-id="6a8ff-168">unicode</span></span>     |
|       | <span data-ttu-id="6a8ff-169">Aviso de/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-169">/ifd/iptc/copyright notice</span></span>              |             |
|       | <span data-ttu-id="6a8ff-170">Aviso de/IFD/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-170">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |             |
|       | <span data-ttu-id="6a8ff-171">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="6a8ff-171">/ifd/{ushort=33432}</span></span>                     | <span data-ttu-id="6a8ff-172">ascii</span><span class="sxs-lookup"><span data-stu-id="6a8ff-172">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="6a8ff-173">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6a8ff-173">Remove Paths</span></span>



| <span data-ttu-id="6a8ff-174">Pedido</span><span class="sxs-lookup"><span data-stu-id="6a8ff-174">Order</span></span> | <span data-ttu-id="6a8ff-175">Ruta</span><span class="sxs-lookup"><span data-stu-id="6a8ff-175">Path</span></span>                                    |
|-------|-----------------------------------------|
|       | <span data-ttu-id="6a8ff-176">/IFD/XMP/DC: derechos</span><span class="sxs-lookup"><span data-stu-id="6a8ff-176">/ifd/xmp/dc:rights</span></span>                      |
|       | <span data-ttu-id="6a8ff-177">Aviso de/IFD/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-177">/ifd/iptc/copyright notice</span></span>              |
|       | <span data-ttu-id="6a8ff-178">Aviso de/IFD/IRB/8bimiptc/IPTC/Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-178">/ifd/irb/8bimiptc/iptc/copyright notice</span></span> |
|       | <span data-ttu-id="6a8ff-179">/IFD/{ushort = 33432}</span><span class="sxs-lookup"><span data-stu-id="6a8ff-179">/ifd/{ushort=33432}</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="6a8ff-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a8ff-180">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a8ff-181">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a8ff-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a8ff-182">System. Copyright</span><span class="sxs-lookup"><span data-stu-id="6a8ff-182">System.Copyright</span></span>](../properties/props-system-copyright.md)
</dt> </dl>

 

 
