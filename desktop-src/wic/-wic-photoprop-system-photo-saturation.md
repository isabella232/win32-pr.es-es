---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. saturación.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Directiva de metadatos de la foto System. Photo. saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083166"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="b1423-103">Directiva de metadatos de la foto System. Photo. saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="b1423-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. saturación](../properties/props-system-photo-saturation.md) .</span><span class="sxs-lookup"><span data-stu-id="b1423-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b1423-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b1423-105">PKEY</span></span>

<span data-ttu-id="b1423-106">Saturación de la fotografía de PKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1423-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="b1423-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="b1423-107">Containers</span></span>

<span data-ttu-id="b1423-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b1423-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b1423-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1423-109">Read-Only</span></span>

<span data-ttu-id="b1423-110">No</span><span class="sxs-lookup"><span data-stu-id="b1423-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b1423-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="b1423-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b1423-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b1423-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="b1423-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="b1423-113">Input Type</span></span>

<span data-ttu-id="b1423-114">UShort</span><span class="sxs-lookup"><span data-stu-id="b1423-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b1423-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="b1423-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b1423-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="b1423-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b1423-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="b1423-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b1423-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="b1423-118">Read Paths</span></span>



| <span data-ttu-id="b1423-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="b1423-119">Order</span></span> | <span data-ttu-id="b1423-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="b1423-120">Path</span></span>                          | <span data-ttu-id="b1423-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1423-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b1423-122">1</span><span class="sxs-lookup"><span data-stu-id="b1423-122">1</span></span>     | <span data-ttu-id="b1423-123">/app1/IFD/Exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b1423-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b1423-124">ushort</span><span class="sxs-lookup"><span data-stu-id="b1423-124">ushort</span></span>      |
| <span data-ttu-id="b1423-125">2</span><span class="sxs-lookup"><span data-stu-id="b1423-125">2</span></span>     | <span data-ttu-id="b1423-126">/XMP/Exif: saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="b1423-127">unicode</span><span class="sxs-lookup"><span data-stu-id="b1423-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b1423-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="b1423-128">Write Paths</span></span>



| <span data-ttu-id="b1423-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="b1423-129">Order</span></span> | <span data-ttu-id="b1423-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="b1423-130">Path</span></span>                          | <span data-ttu-id="b1423-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1423-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="b1423-132">1</span><span class="sxs-lookup"><span data-stu-id="b1423-132">1</span></span>     | <span data-ttu-id="b1423-133">/app1/IFD/Exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b1423-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b1423-134">ushort</span><span class="sxs-lookup"><span data-stu-id="b1423-134">ushort</span></span>      |
| <span data-ttu-id="b1423-135">2</span><span class="sxs-lookup"><span data-stu-id="b1423-135">2</span></span>     | <span data-ttu-id="b1423-136">/XMP/Exif: saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="b1423-137">unicode</span><span class="sxs-lookup"><span data-stu-id="b1423-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b1423-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="b1423-138">Remove Paths</span></span>



| <span data-ttu-id="b1423-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="b1423-139">Order</span></span> | <span data-ttu-id="b1423-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="b1423-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="b1423-141">1</span><span class="sxs-lookup"><span data-stu-id="b1423-141">1</span></span>     | <span data-ttu-id="b1423-142">/app1/IFD/Exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b1423-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="b1423-143">2</span><span class="sxs-lookup"><span data-stu-id="b1423-143">2</span></span>     | <span data-ttu-id="b1423-144">/XMP/Exif: saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="b1423-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="b1423-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b1423-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="b1423-146">Read Paths</span></span>



| <span data-ttu-id="b1423-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="b1423-147">Order</span></span> | <span data-ttu-id="b1423-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="b1423-148">Path</span></span>                     | <span data-ttu-id="b1423-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1423-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b1423-150">1</span><span class="sxs-lookup"><span data-stu-id="b1423-150">1</span></span>     | <span data-ttu-id="b1423-151">/IFD/Exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b1423-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b1423-152">ushort</span><span class="sxs-lookup"><span data-stu-id="b1423-152">ushort</span></span>      |
| <span data-ttu-id="b1423-153">2</span><span class="sxs-lookup"><span data-stu-id="b1423-153">2</span></span>     | <span data-ttu-id="b1423-154">/IFD/XMP/Exif: saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="b1423-155">unicode</span><span class="sxs-lookup"><span data-stu-id="b1423-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b1423-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="b1423-156">Write Paths</span></span>



| <span data-ttu-id="b1423-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="b1423-157">Order</span></span> | <span data-ttu-id="b1423-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="b1423-158">Path</span></span>                     | <span data-ttu-id="b1423-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1423-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b1423-160">1</span><span class="sxs-lookup"><span data-stu-id="b1423-160">1</span></span>     | <span data-ttu-id="b1423-161">/IFD/Exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b1423-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="b1423-162">ushort</span><span class="sxs-lookup"><span data-stu-id="b1423-162">ushort</span></span>      |
| <span data-ttu-id="b1423-163">2</span><span class="sxs-lookup"><span data-stu-id="b1423-163">2</span></span>     | <span data-ttu-id="b1423-164">/IFD/XMP/Exif: saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="b1423-165">unicode</span><span class="sxs-lookup"><span data-stu-id="b1423-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b1423-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="b1423-166">Remove Paths</span></span>



| <span data-ttu-id="b1423-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="b1423-167">Order</span></span> | <span data-ttu-id="b1423-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="b1423-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="b1423-169">1</span><span class="sxs-lookup"><span data-stu-id="b1423-169">1</span></span>     | <span data-ttu-id="b1423-170">/IFD/Exif/{ushort = 41993}</span><span class="sxs-lookup"><span data-stu-id="b1423-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="b1423-171">2</span><span class="sxs-lookup"><span data-stu-id="b1423-171">2</span></span>     | <span data-ttu-id="b1423-172">/IFD/XMP/Exif: saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b1423-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1423-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1423-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1423-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1423-175">System. Photo. saturación</span><span class="sxs-lookup"><span data-stu-id="b1423-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
