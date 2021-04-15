---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Directiva de metadatos de la foto de System. Photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498029"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a><span data-ttu-id="fbf54-103">Directiva de metadatos de la foto de System. Photo. FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-103">System.Photo.FocalLengthInFilm Photo Metadata Policy</span></span>

<span data-ttu-id="fbf54-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf54-104">The photo metadata policy for the [System.Photo.FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="fbf54-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="fbf54-105">PKEY</span></span>

<span data-ttu-id="fbf54-106">PKEY \_ FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-106">PKEY\_FocalLengthInFilm</span></span>

### <a name="containers"></a><span data-ttu-id="fbf54-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="fbf54-107">Containers</span></span>

<span data-ttu-id="fbf54-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="fbf54-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="fbf54-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf54-109">Read-Only</span></span>

<span data-ttu-id="fbf54-110">No</span><span class="sxs-lookup"><span data-stu-id="fbf54-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="fbf54-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="fbf54-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="fbf54-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="fbf54-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="fbf54-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="fbf54-113">Input Type</span></span>

<span data-ttu-id="fbf54-114">UShort</span><span class="sxs-lookup"><span data-stu-id="fbf54-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="fbf54-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="fbf54-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="fbf54-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="fbf54-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="fbf54-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="fbf54-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="fbf54-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="fbf54-118">Read Paths</span></span>



| <span data-ttu-id="fbf54-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="fbf54-119">Order</span></span> | <span data-ttu-id="fbf54-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="fbf54-120">Path</span></span>                            | <span data-ttu-id="fbf54-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="fbf54-121">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="fbf54-122">1</span><span class="sxs-lookup"><span data-stu-id="fbf54-122">1</span></span>     | <span data-ttu-id="fbf54-123">/app1/IFD/Exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="fbf54-123">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="fbf54-124">ushort</span><span class="sxs-lookup"><span data-stu-id="fbf54-124">ushort</span></span>      |
| <span data-ttu-id="fbf54-125">2</span><span class="sxs-lookup"><span data-stu-id="fbf54-125">2</span></span>     | <span data-ttu-id="fbf54-126">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-126">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="fbf54-127">unicode</span><span class="sxs-lookup"><span data-stu-id="fbf54-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fbf54-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="fbf54-128">Write Paths</span></span>



| <span data-ttu-id="fbf54-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="fbf54-129">Order</span></span> | <span data-ttu-id="fbf54-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="fbf54-130">Path</span></span>                            | <span data-ttu-id="fbf54-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="fbf54-131">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="fbf54-132">1</span><span class="sxs-lookup"><span data-stu-id="fbf54-132">1</span></span>     | <span data-ttu-id="fbf54-133">/app1/IFD/Exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="fbf54-133">/app1/ifd/exif/{ushort=41989}</span></span>   | <span data-ttu-id="fbf54-134">ushort</span><span class="sxs-lookup"><span data-stu-id="fbf54-134">ushort</span></span>      |
| <span data-ttu-id="fbf54-135">2</span><span class="sxs-lookup"><span data-stu-id="fbf54-135">2</span></span>     | <span data-ttu-id="fbf54-136">/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-136">/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="fbf54-137">unicode</span><span class="sxs-lookup"><span data-stu-id="fbf54-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fbf54-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="fbf54-138">Remove Paths</span></span>



| <span data-ttu-id="fbf54-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="fbf54-139">Order</span></span> | <span data-ttu-id="fbf54-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="fbf54-140">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="fbf54-141">1</span><span class="sxs-lookup"><span data-stu-id="fbf54-141">1</span></span>     | <span data-ttu-id="fbf54-142">/app1/IFD/Exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="fbf54-142">/app1/ifd/exif/{ushort=41989}</span></span>   |
| <span data-ttu-id="fbf54-143">2</span><span class="sxs-lookup"><span data-stu-id="fbf54-143">2</span></span>     | <span data-ttu-id="fbf54-144">/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-144">/xmp/exif:focallengthin35mmfilm</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="fbf54-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="fbf54-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="fbf54-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="fbf54-146">Read Paths</span></span>



| <span data-ttu-id="fbf54-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="fbf54-147">Order</span></span> | <span data-ttu-id="fbf54-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="fbf54-148">Path</span></span>                                | <span data-ttu-id="fbf54-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="fbf54-149">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="fbf54-150">1</span><span class="sxs-lookup"><span data-stu-id="fbf54-150">1</span></span>     | <span data-ttu-id="fbf54-151">/IFD/Exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="fbf54-151">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="fbf54-152">ushort</span><span class="sxs-lookup"><span data-stu-id="fbf54-152">ushort</span></span>      |
| <span data-ttu-id="fbf54-153">2</span><span class="sxs-lookup"><span data-stu-id="fbf54-153">2</span></span>     | <span data-ttu-id="fbf54-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-154">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="fbf54-155">unicode</span><span class="sxs-lookup"><span data-stu-id="fbf54-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="fbf54-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="fbf54-156">Write Paths</span></span>



| <span data-ttu-id="fbf54-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="fbf54-157">Order</span></span> | <span data-ttu-id="fbf54-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="fbf54-158">Path</span></span>                                | <span data-ttu-id="fbf54-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="fbf54-159">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="fbf54-160">1</span><span class="sxs-lookup"><span data-stu-id="fbf54-160">1</span></span>     | <span data-ttu-id="fbf54-161">/IFD/Exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="fbf54-161">/ifd/exif/{ushort=41989}</span></span>            | <span data-ttu-id="fbf54-162">ushort</span><span class="sxs-lookup"><span data-stu-id="fbf54-162">ushort</span></span>      |
| <span data-ttu-id="fbf54-163">2</span><span class="sxs-lookup"><span data-stu-id="fbf54-163">2</span></span>     | <span data-ttu-id="fbf54-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-164">/ifd/xmp/exif:FocalLengthIn35mmFilm</span></span> | <span data-ttu-id="fbf54-165">unicode</span><span class="sxs-lookup"><span data-stu-id="fbf54-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="fbf54-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="fbf54-166">Remove Paths</span></span>



| <span data-ttu-id="fbf54-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="fbf54-167">Order</span></span> | <span data-ttu-id="fbf54-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="fbf54-168">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="fbf54-169">1</span><span class="sxs-lookup"><span data-stu-id="fbf54-169">1</span></span>     | <span data-ttu-id="fbf54-170">/IFD/Exif/{ushort = 41989}</span><span class="sxs-lookup"><span data-stu-id="fbf54-170">/ifd/exif/{ushort=41989}</span></span>            |
| <span data-ttu-id="fbf54-171">2</span><span class="sxs-lookup"><span data-stu-id="fbf54-171">2</span></span>     | <span data-ttu-id="fbf54-172">/ifd/xmp/exif:focallengthin35mmfilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-172">/ifd/xmp/exif:focallengthin35mmfilm</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fbf54-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbf54-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbf54-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbf54-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbf54-175">System. Photo. FocalLengthInFilm</span><span class="sxs-lookup"><span data-stu-id="fbf54-175">System.Photo.FocalLengthInFilm</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
