---
description: La Directiva de metadatos de la fotografía para la propiedad System. Photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Directiva de metadatos de fotografía de System. Photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546606"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a><span data-ttu-id="e133c-103">Directiva de metadatos de fotografía de System. Photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="e133c-103">System.Photo.LightSource Photo Metadata Policy</span></span>

<span data-ttu-id="e133c-104">La Directiva de metadatos de la fotografía para la propiedad [System. Photo. lightsource](../properties/props-system-photo-lightsource.md) .</span><span class="sxs-lookup"><span data-stu-id="e133c-104">The photo metadata policy for the [System.Photo.LightSource](../properties/props-system-photo-lightsource.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e133c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e133c-105">PKEY</span></span>

<span data-ttu-id="e133c-106">PKEY \_ Photo \_ lightsource</span><span class="sxs-lookup"><span data-stu-id="e133c-106">PKEY\_Photo\_LightSource</span></span>

### <a name="containers"></a><span data-ttu-id="e133c-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="e133c-107">Containers</span></span>

<span data-ttu-id="e133c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e133c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e133c-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e133c-109">Read-Only</span></span>

<span data-ttu-id="e133c-110">No</span><span class="sxs-lookup"><span data-stu-id="e133c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e133c-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="e133c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e133c-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e133c-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="e133c-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="e133c-113">Input Type</span></span>

<span data-ttu-id="e133c-114">UShort</span><span class="sxs-lookup"><span data-stu-id="e133c-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e133c-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="e133c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e133c-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="e133c-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e133c-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="e133c-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e133c-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e133c-118">Read Paths</span></span>



| <span data-ttu-id="e133c-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="e133c-119">Order</span></span> | <span data-ttu-id="e133c-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="e133c-120">Path</span></span>                          | <span data-ttu-id="e133c-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e133c-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e133c-122">1</span><span class="sxs-lookup"><span data-stu-id="e133c-122">1</span></span>     | <span data-ttu-id="e133c-123">/app1/IFD/Exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="e133c-123">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="e133c-124">ushort</span><span class="sxs-lookup"><span data-stu-id="e133c-124">ushort</span></span>      |
| <span data-ttu-id="e133c-125">2</span><span class="sxs-lookup"><span data-stu-id="e133c-125">2</span></span>     | <span data-ttu-id="e133c-126">/XMP/Exif: LightSource</span><span class="sxs-lookup"><span data-stu-id="e133c-126">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="e133c-127">unicode</span><span class="sxs-lookup"><span data-stu-id="e133c-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e133c-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e133c-128">Write Paths</span></span>



| <span data-ttu-id="e133c-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="e133c-129">Order</span></span> | <span data-ttu-id="e133c-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="e133c-130">Path</span></span>                          | <span data-ttu-id="e133c-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e133c-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e133c-132">1</span><span class="sxs-lookup"><span data-stu-id="e133c-132">1</span></span>     | <span data-ttu-id="e133c-133">/app1/IFD/Exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="e133c-133">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="e133c-134">ushort</span><span class="sxs-lookup"><span data-stu-id="e133c-134">ushort</span></span>      |
| <span data-ttu-id="e133c-135">2</span><span class="sxs-lookup"><span data-stu-id="e133c-135">2</span></span>     | <span data-ttu-id="e133c-136">/XMP/Exif: LightSource</span><span class="sxs-lookup"><span data-stu-id="e133c-136">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="e133c-137">unicode</span><span class="sxs-lookup"><span data-stu-id="e133c-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e133c-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e133c-138">Remove Paths</span></span>



| <span data-ttu-id="e133c-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="e133c-139">Order</span></span> | <span data-ttu-id="e133c-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="e133c-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="e133c-141">1</span><span class="sxs-lookup"><span data-stu-id="e133c-141">1</span></span>     | <span data-ttu-id="e133c-142">/app1/IFD/Exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="e133c-142">/app1/ifd/exif/{ushort=37384}</span></span> |
| <span data-ttu-id="e133c-143">2</span><span class="sxs-lookup"><span data-stu-id="e133c-143">2</span></span>     | <span data-ttu-id="e133c-144">/XMP/Exif: lightsource</span><span class="sxs-lookup"><span data-stu-id="e133c-144">/xmp/exif:lightsource</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="e133c-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="e133c-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e133c-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e133c-146">Read Paths</span></span>



| <span data-ttu-id="e133c-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="e133c-147">Order</span></span> | <span data-ttu-id="e133c-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="e133c-148">Path</span></span>                      | <span data-ttu-id="e133c-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e133c-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e133c-150">1</span><span class="sxs-lookup"><span data-stu-id="e133c-150">1</span></span>     | <span data-ttu-id="e133c-151">/IFD/Exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="e133c-151">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="e133c-152">ushort</span><span class="sxs-lookup"><span data-stu-id="e133c-152">ushort</span></span>      |
| <span data-ttu-id="e133c-153">2</span><span class="sxs-lookup"><span data-stu-id="e133c-153">2</span></span>     | <span data-ttu-id="e133c-154">/IFD/XMP/Exif: LightSource</span><span class="sxs-lookup"><span data-stu-id="e133c-154">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="e133c-155">unicode</span><span class="sxs-lookup"><span data-stu-id="e133c-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="e133c-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e133c-156">Write Paths</span></span>



| <span data-ttu-id="e133c-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="e133c-157">Order</span></span> | <span data-ttu-id="e133c-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="e133c-158">Path</span></span>                      | <span data-ttu-id="e133c-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e133c-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e133c-160">1</span><span class="sxs-lookup"><span data-stu-id="e133c-160">1</span></span>     | <span data-ttu-id="e133c-161">/IFD/Exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="e133c-161">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="e133c-162">ushort</span><span class="sxs-lookup"><span data-stu-id="e133c-162">ushort</span></span>      |
| <span data-ttu-id="e133c-163">2</span><span class="sxs-lookup"><span data-stu-id="e133c-163">2</span></span>     | <span data-ttu-id="e133c-164">/IFD/XMP/Exif: LightSource</span><span class="sxs-lookup"><span data-stu-id="e133c-164">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="e133c-165">unicode</span><span class="sxs-lookup"><span data-stu-id="e133c-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="e133c-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e133c-166">Remove Paths</span></span>



| <span data-ttu-id="e133c-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="e133c-167">Order</span></span> | <span data-ttu-id="e133c-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="e133c-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="e133c-169">1</span><span class="sxs-lookup"><span data-stu-id="e133c-169">1</span></span>     | <span data-ttu-id="e133c-170">/IFD/Exif/{ushort = 37384}</span><span class="sxs-lookup"><span data-stu-id="e133c-170">/ifd/exif/{ushort=37384}</span></span>  |
| <span data-ttu-id="e133c-171">2</span><span class="sxs-lookup"><span data-stu-id="e133c-171">2</span></span>     | <span data-ttu-id="e133c-172">/IFD/XMP/Exif: lightsource</span><span class="sxs-lookup"><span data-stu-id="e133c-172">/ifd/xmp/exif:lightsource</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e133c-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e133c-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e133c-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e133c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e133c-175">System. Photo. LightSource</span><span class="sxs-lookup"><span data-stu-id="e133c-175">System.Photo.LightSource</span></span>](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
