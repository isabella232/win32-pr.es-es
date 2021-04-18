---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Directiva de metadatos de foto de System. Image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687662"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="ce876-103">Directiva de metadatos de foto de System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="ce876-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="ce876-104">La Directiva de metadatos de la fotografía para la propiedad [System. Image. Compression](../properties/props-system-image-compression.md) .</span><span class="sxs-lookup"><span data-stu-id="ce876-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ce876-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ce876-105">PKEY</span></span>

<span data-ttu-id="ce876-106">\_Compresión de imagen PKEY \_</span><span class="sxs-lookup"><span data-stu-id="ce876-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="ce876-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="ce876-107">Containers</span></span>

<span data-ttu-id="ce876-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ce876-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ce876-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ce876-109">Read-Only</span></span>

<span data-ttu-id="ce876-110">Sí</span><span class="sxs-lookup"><span data-stu-id="ce876-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ce876-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="ce876-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ce876-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="ce876-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="ce876-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="ce876-113">Input Type</span></span>

<span data-ttu-id="ce876-114">UShort</span><span class="sxs-lookup"><span data-stu-id="ce876-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ce876-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="ce876-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ce876-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="ce876-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ce876-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="ce876-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ce876-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ce876-118">Read Paths</span></span>



| <span data-ttu-id="ce876-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="ce876-119">Order</span></span> | <span data-ttu-id="ce876-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="ce876-120">Path</span></span>                   | <span data-ttu-id="ce876-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ce876-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="ce876-122">1</span><span class="sxs-lookup"><span data-stu-id="ce876-122">1</span></span>     | <span data-ttu-id="ce876-123">/app1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="ce876-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="ce876-124">ushort</span><span class="sxs-lookup"><span data-stu-id="ce876-124">ushort</span></span>      |
| <span data-ttu-id="ce876-125">2</span><span class="sxs-lookup"><span data-stu-id="ce876-125">2</span></span>     | <span data-ttu-id="ce876-126">/XMP/TIFF: compresión</span><span class="sxs-lookup"><span data-stu-id="ce876-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="ce876-127">unicode</span><span class="sxs-lookup"><span data-stu-id="ce876-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ce876-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ce876-128">Write Paths</span></span>



| <span data-ttu-id="ce876-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="ce876-129">Order</span></span> | <span data-ttu-id="ce876-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="ce876-130">Path</span></span>                   | <span data-ttu-id="ce876-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ce876-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="ce876-132">1</span><span class="sxs-lookup"><span data-stu-id="ce876-132">1</span></span>     | <span data-ttu-id="ce876-133">/app1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="ce876-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="ce876-134">ushort</span><span class="sxs-lookup"><span data-stu-id="ce876-134">ushort</span></span>      |
| <span data-ttu-id="ce876-135">2</span><span class="sxs-lookup"><span data-stu-id="ce876-135">2</span></span>     | <span data-ttu-id="ce876-136">/XMP/TIFF: compresión</span><span class="sxs-lookup"><span data-stu-id="ce876-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="ce876-137">unicode</span><span class="sxs-lookup"><span data-stu-id="ce876-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ce876-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ce876-138">Remove Paths</span></span>



| <span data-ttu-id="ce876-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="ce876-139">Order</span></span> | <span data-ttu-id="ce876-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="ce876-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="ce876-141">1</span><span class="sxs-lookup"><span data-stu-id="ce876-141">1</span></span>     | <span data-ttu-id="ce876-142">/app1/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="ce876-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="ce876-143">2</span><span class="sxs-lookup"><span data-stu-id="ce876-143">2</span></span>     | <span data-ttu-id="ce876-144">/XMP/TIFF: compresión</span><span class="sxs-lookup"><span data-stu-id="ce876-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="ce876-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="ce876-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ce876-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ce876-146">Read Paths</span></span>



| <span data-ttu-id="ce876-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="ce876-147">Order</span></span> | <span data-ttu-id="ce876-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="ce876-148">Path</span></span>                      | <span data-ttu-id="ce876-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ce876-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ce876-150">1</span><span class="sxs-lookup"><span data-stu-id="ce876-150">1</span></span>     | <span data-ttu-id="ce876-151">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="ce876-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="ce876-152">ushort</span><span class="sxs-lookup"><span data-stu-id="ce876-152">ushort</span></span>      |
| <span data-ttu-id="ce876-153">2</span><span class="sxs-lookup"><span data-stu-id="ce876-153">2</span></span>     | <span data-ttu-id="ce876-154">/IFD/XMP/TIFF: compresión</span><span class="sxs-lookup"><span data-stu-id="ce876-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="ce876-155">unicode</span><span class="sxs-lookup"><span data-stu-id="ce876-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ce876-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ce876-156">Write Paths</span></span>



| <span data-ttu-id="ce876-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="ce876-157">Order</span></span> | <span data-ttu-id="ce876-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="ce876-158">Path</span></span>                      | <span data-ttu-id="ce876-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ce876-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="ce876-160">1</span><span class="sxs-lookup"><span data-stu-id="ce876-160">1</span></span>     | <span data-ttu-id="ce876-161">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="ce876-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="ce876-162">ushort</span><span class="sxs-lookup"><span data-stu-id="ce876-162">ushort</span></span>      |
| <span data-ttu-id="ce876-163">2</span><span class="sxs-lookup"><span data-stu-id="ce876-163">2</span></span>     | <span data-ttu-id="ce876-164">/IFD/XMP/TIFF: compresión</span><span class="sxs-lookup"><span data-stu-id="ce876-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="ce876-165">unicode</span><span class="sxs-lookup"><span data-stu-id="ce876-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ce876-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ce876-166">Remove Paths</span></span>



| <span data-ttu-id="ce876-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="ce876-167">Order</span></span> | <span data-ttu-id="ce876-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="ce876-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ce876-169">1</span><span class="sxs-lookup"><span data-stu-id="ce876-169">1</span></span>     | <span data-ttu-id="ce876-170">/IFD/{ushort = 259}</span><span class="sxs-lookup"><span data-stu-id="ce876-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="ce876-171">2</span><span class="sxs-lookup"><span data-stu-id="ce876-171">2</span></span>     | <span data-ttu-id="ce876-172">/IFD/XMP/TIFF: compresión</span><span class="sxs-lookup"><span data-stu-id="ce876-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ce876-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce876-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce876-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce876-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce876-175">System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="ce876-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
