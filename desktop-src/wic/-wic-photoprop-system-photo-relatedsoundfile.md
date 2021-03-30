---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Directiva de metadatos de la foto de System. Photo. RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002577"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a><span data-ttu-id="d7ddf-103">Directiva de metadatos de la foto de System. Photo. RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-103">System.Photo.RelatedSoundFile Photo Metadata Policy</span></span>

<span data-ttu-id="d7ddf-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ddf-104">The photo metadata policy for the [System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d7ddf-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d7ddf-105">PKEY</span></span>

<span data-ttu-id="d7ddf-106">PKEY \_ Photo \_ RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-106">PKEY\_Photo\_RelatedSoundFile</span></span>

### <a name="containers"></a><span data-ttu-id="d7ddf-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="d7ddf-107">Containers</span></span>

<span data-ttu-id="d7ddf-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d7ddf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d7ddf-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d7ddf-109">Read-Only</span></span>

<span data-ttu-id="d7ddf-110">No</span><span class="sxs-lookup"><span data-stu-id="d7ddf-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d7ddf-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="d7ddf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d7ddf-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="d7ddf-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="d7ddf-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="d7ddf-113">Input Type</span></span>

<span data-ttu-id="d7ddf-114">String.</span><span class="sxs-lookup"><span data-stu-id="d7ddf-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d7ddf-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="d7ddf-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d7ddf-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="d7ddf-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d7ddf-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="d7ddf-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d7ddf-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d7ddf-118">Read Paths</span></span>



| <span data-ttu-id="d7ddf-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="d7ddf-119">Order</span></span> | <span data-ttu-id="d7ddf-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="d7ddf-120">Path</span></span>                          | <span data-ttu-id="d7ddf-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7ddf-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d7ddf-122">1</span><span class="sxs-lookup"><span data-stu-id="d7ddf-122">1</span></span>     | <span data-ttu-id="d7ddf-123">/app1/IFD/Exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="d7ddf-123">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="d7ddf-124">ascii</span><span class="sxs-lookup"><span data-stu-id="d7ddf-124">ascii</span></span>       |
| <span data-ttu-id="d7ddf-125">2</span><span class="sxs-lookup"><span data-stu-id="d7ddf-125">2</span></span>     | <span data-ttu-id="d7ddf-126">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-126">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="d7ddf-127">unicode</span><span class="sxs-lookup"><span data-stu-id="d7ddf-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d7ddf-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d7ddf-128">Write Paths</span></span>



| <span data-ttu-id="d7ddf-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="d7ddf-129">Order</span></span> | <span data-ttu-id="d7ddf-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="d7ddf-130">Path</span></span>                          | <span data-ttu-id="d7ddf-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7ddf-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d7ddf-132">1</span><span class="sxs-lookup"><span data-stu-id="d7ddf-132">1</span></span>     | <span data-ttu-id="d7ddf-133">/app1/IFD/Exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="d7ddf-133">/app1/ifd/exif/{ushort=40964}</span></span> | <span data-ttu-id="d7ddf-134">ascii</span><span class="sxs-lookup"><span data-stu-id="d7ddf-134">ascii</span></span>       |
| <span data-ttu-id="d7ddf-135">2</span><span class="sxs-lookup"><span data-stu-id="d7ddf-135">2</span></span>     | <span data-ttu-id="d7ddf-136">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-136">/xmp/exif:RelatedSoundFile</span></span>    | <span data-ttu-id="d7ddf-137">unicode</span><span class="sxs-lookup"><span data-stu-id="d7ddf-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d7ddf-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d7ddf-138">Remove Paths</span></span>



| <span data-ttu-id="d7ddf-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="d7ddf-139">Order</span></span> | <span data-ttu-id="d7ddf-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="d7ddf-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d7ddf-141">1</span><span class="sxs-lookup"><span data-stu-id="d7ddf-141">1</span></span>     | <span data-ttu-id="d7ddf-142">/app1/IFD/Exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="d7ddf-142">/app1/ifd/exif/{ushort=40964}</span></span> |
| <span data-ttu-id="d7ddf-143">2</span><span class="sxs-lookup"><span data-stu-id="d7ddf-143">2</span></span>     | <span data-ttu-id="d7ddf-144">/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-144">/xmp/exif:RelatedSoundFile</span></span>    |



 

### <a name="tiff-policy"></a><span data-ttu-id="d7ddf-145">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="d7ddf-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d7ddf-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d7ddf-146">Read Paths</span></span>



| <span data-ttu-id="d7ddf-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="d7ddf-147">Order</span></span> | <span data-ttu-id="d7ddf-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="d7ddf-148">Path</span></span>                           | <span data-ttu-id="d7ddf-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7ddf-149">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="d7ddf-150">1</span><span class="sxs-lookup"><span data-stu-id="d7ddf-150">1</span></span>     | <span data-ttu-id="d7ddf-151">/IFD/Exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="d7ddf-151">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="d7ddf-152">ascii</span><span class="sxs-lookup"><span data-stu-id="d7ddf-152">ascii</span></span>       |
| <span data-ttu-id="d7ddf-153">2</span><span class="sxs-lookup"><span data-stu-id="d7ddf-153">2</span></span>     | <span data-ttu-id="d7ddf-154">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-154">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="d7ddf-155">unicode</span><span class="sxs-lookup"><span data-stu-id="d7ddf-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d7ddf-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d7ddf-156">Write Paths</span></span>



| <span data-ttu-id="d7ddf-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="d7ddf-157">Order</span></span> | <span data-ttu-id="d7ddf-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="d7ddf-158">Path</span></span>                           | <span data-ttu-id="d7ddf-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7ddf-159">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="d7ddf-160">1</span><span class="sxs-lookup"><span data-stu-id="d7ddf-160">1</span></span>     | <span data-ttu-id="d7ddf-161">/IFD/Exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="d7ddf-161">/ifd/exif/{ushort=40964}</span></span>       | <span data-ttu-id="d7ddf-162">ascii</span><span class="sxs-lookup"><span data-stu-id="d7ddf-162">ascii</span></span>       |
| <span data-ttu-id="d7ddf-163">2</span><span class="sxs-lookup"><span data-stu-id="d7ddf-163">2</span></span>     | <span data-ttu-id="d7ddf-164">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-164">/ifd/xmp/exif:RelatedSoundFile</span></span> | <span data-ttu-id="d7ddf-165">unicode</span><span class="sxs-lookup"><span data-stu-id="d7ddf-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d7ddf-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d7ddf-166">Remove Paths</span></span>



| <span data-ttu-id="d7ddf-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="d7ddf-167">Order</span></span> | <span data-ttu-id="d7ddf-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="d7ddf-168">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="d7ddf-169">1</span><span class="sxs-lookup"><span data-stu-id="d7ddf-169">1</span></span>     | <span data-ttu-id="d7ddf-170">/IFD/Exif/{ushort = 40964}</span><span class="sxs-lookup"><span data-stu-id="d7ddf-170">/ifd/exif/{ushort=40964}</span></span>       |
| <span data-ttu-id="d7ddf-171">2</span><span class="sxs-lookup"><span data-stu-id="d7ddf-171">2</span></span>     | <span data-ttu-id="d7ddf-172">/ifd/xmp/exif:RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-172">/ifd/xmp/exif:RelatedSoundFile</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d7ddf-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7ddf-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7ddf-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7ddf-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ddf-175">System. Photo. RelatedSoundFile</span><span class="sxs-lookup"><span data-stu-id="d7ddf-175">System.Photo.RelatedSoundFile</span></span>](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
