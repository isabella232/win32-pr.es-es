---
description: La Directiva de metadatos de la foto de la propiedad System. Photo. Sharpity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Directiva de metadatos de foto de System. Photo. nitidez
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678223"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="5b607-103">Directiva de metadatos de foto de System. Photo. nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="5b607-104">La Directiva de metadatos de la foto de la propiedad [System. Photo. sharpity](../properties/props-system-photo-sharpness.md) .</span><span class="sxs-lookup"><span data-stu-id="5b607-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5b607-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5b607-105">PKEY</span></span>

<span data-ttu-id="5b607-106">PKEY \_ foto \_</span><span class="sxs-lookup"><span data-stu-id="5b607-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="5b607-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="5b607-107">Containers</span></span>

<span data-ttu-id="5b607-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5b607-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5b607-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5b607-109">Read-Only</span></span>

<span data-ttu-id="5b607-110">No</span><span class="sxs-lookup"><span data-stu-id="5b607-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5b607-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="5b607-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5b607-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="5b607-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="5b607-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="5b607-113">Input Type</span></span>

<span data-ttu-id="5b607-114">UShort</span><span class="sxs-lookup"><span data-stu-id="5b607-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5b607-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="5b607-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5b607-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="5b607-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5b607-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="5b607-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5b607-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5b607-118">Read Paths</span></span>



| <span data-ttu-id="5b607-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="5b607-119">Order</span></span> | <span data-ttu-id="5b607-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="5b607-120">Path</span></span>                          | <span data-ttu-id="5b607-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5b607-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5b607-122">1</span><span class="sxs-lookup"><span data-stu-id="5b607-122">1</span></span>     | <span data-ttu-id="5b607-123">/app1/IFD/Exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="5b607-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="5b607-124">ushort</span><span class="sxs-lookup"><span data-stu-id="5b607-124">ushort</span></span>      |
| <span data-ttu-id="5b607-125">2</span><span class="sxs-lookup"><span data-stu-id="5b607-125">2</span></span>     | <span data-ttu-id="5b607-126">/XMP/Exif: nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="5b607-127">unicode</span><span class="sxs-lookup"><span data-stu-id="5b607-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5b607-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5b607-128">Write Paths</span></span>



| <span data-ttu-id="5b607-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="5b607-129">Order</span></span> | <span data-ttu-id="5b607-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="5b607-130">Path</span></span>                          | <span data-ttu-id="5b607-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5b607-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5b607-132">1</span><span class="sxs-lookup"><span data-stu-id="5b607-132">1</span></span>     | <span data-ttu-id="5b607-133">/app1/IFD/Exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="5b607-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="5b607-134">ushort</span><span class="sxs-lookup"><span data-stu-id="5b607-134">ushort</span></span>      |
| <span data-ttu-id="5b607-135">2</span><span class="sxs-lookup"><span data-stu-id="5b607-135">2</span></span>     | <span data-ttu-id="5b607-136">/XMP/Exif: nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="5b607-137">unicode</span><span class="sxs-lookup"><span data-stu-id="5b607-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5b607-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5b607-138">Remove Paths</span></span>



| <span data-ttu-id="5b607-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="5b607-139">Order</span></span> | <span data-ttu-id="5b607-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="5b607-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5b607-141">1</span><span class="sxs-lookup"><span data-stu-id="5b607-141">1</span></span>     | <span data-ttu-id="5b607-142">/app1/IFD/Exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="5b607-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="5b607-143">2</span><span class="sxs-lookup"><span data-stu-id="5b607-143">2</span></span>     | <span data-ttu-id="5b607-144">/XMP/Exif: nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="5b607-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="5b607-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5b607-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5b607-146">Read Paths</span></span>



| <span data-ttu-id="5b607-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="5b607-147">Order</span></span> | <span data-ttu-id="5b607-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="5b607-148">Path</span></span>                     | <span data-ttu-id="5b607-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5b607-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5b607-150">1</span><span class="sxs-lookup"><span data-stu-id="5b607-150">1</span></span>     | <span data-ttu-id="5b607-151">/IFD/Exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="5b607-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="5b607-152">ushort</span><span class="sxs-lookup"><span data-stu-id="5b607-152">ushort</span></span>      |
| <span data-ttu-id="5b607-153">2</span><span class="sxs-lookup"><span data-stu-id="5b607-153">2</span></span>     | <span data-ttu-id="5b607-154">/IFD/XMP/Exif: nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="5b607-155">unicode</span><span class="sxs-lookup"><span data-stu-id="5b607-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5b607-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5b607-156">Write Paths</span></span>



| <span data-ttu-id="5b607-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="5b607-157">Order</span></span> | <span data-ttu-id="5b607-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="5b607-158">Path</span></span>                     | <span data-ttu-id="5b607-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5b607-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5b607-160">1</span><span class="sxs-lookup"><span data-stu-id="5b607-160">1</span></span>     | <span data-ttu-id="5b607-161">/IFD/Exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="5b607-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="5b607-162">ushort</span><span class="sxs-lookup"><span data-stu-id="5b607-162">ushort</span></span>      |
| <span data-ttu-id="5b607-163">2</span><span class="sxs-lookup"><span data-stu-id="5b607-163">2</span></span>     | <span data-ttu-id="5b607-164">/IFD/XMP/Exif: nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="5b607-165">unicode</span><span class="sxs-lookup"><span data-stu-id="5b607-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5b607-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5b607-166">Remove Paths</span></span>



| <span data-ttu-id="5b607-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="5b607-167">Order</span></span> | <span data-ttu-id="5b607-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="5b607-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="5b607-169">1</span><span class="sxs-lookup"><span data-stu-id="5b607-169">1</span></span>     | <span data-ttu-id="5b607-170">/IFD/Exif/{ushort = 41994}</span><span class="sxs-lookup"><span data-stu-id="5b607-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="5b607-171">2</span><span class="sxs-lookup"><span data-stu-id="5b607-171">2</span></span>     | <span data-ttu-id="5b607-172">/IFD/XMP/Exif: nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="5b607-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b607-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b607-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b607-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b607-175">System. Photo. nitidez</span><span class="sxs-lookup"><span data-stu-id="5b607-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
