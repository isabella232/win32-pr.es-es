---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Directiva de metadatos de la foto de System. Photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278634"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="a952d-103">Directiva de metadatos de la foto de System. Photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="a952d-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .</span><span class="sxs-lookup"><span data-stu-id="a952d-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a952d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a952d-105">PKEY</span></span>

<span data-ttu-id="a952d-106">PKEY \_ Photo \_ EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="a952d-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a952d-107">Containers</span></span>

<span data-ttu-id="a952d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a952d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a952d-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a952d-109">Read-Only</span></span>

<span data-ttu-id="a952d-110">No</span><span class="sxs-lookup"><span data-stu-id="a952d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a952d-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="a952d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a952d-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="a952d-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a952d-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a952d-113">Input Type</span></span>

<span data-ttu-id="a952d-114">String.</span><span class="sxs-lookup"><span data-stu-id="a952d-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a952d-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="a952d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a952d-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="a952d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a952d-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="a952d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a952d-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a952d-118">Read Paths</span></span>



| <span data-ttu-id="a952d-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="a952d-119">Order</span></span> | <span data-ttu-id="a952d-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="a952d-120">Path</span></span>                          | <span data-ttu-id="a952d-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a952d-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="a952d-122">1</span><span class="sxs-lookup"><span data-stu-id="a952d-122">1</span></span>     | <span data-ttu-id="a952d-123">/app1/IFD/Exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="a952d-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="a952d-124">\_versión EXIF</span><span class="sxs-lookup"><span data-stu-id="a952d-124">exif\_version</span></span> |
| <span data-ttu-id="a952d-125">2</span><span class="sxs-lookup"><span data-stu-id="a952d-125">2</span></span>     | <span data-ttu-id="a952d-126">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="a952d-127">unicode</span><span class="sxs-lookup"><span data-stu-id="a952d-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="a952d-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a952d-128">Write Paths</span></span>



| <span data-ttu-id="a952d-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="a952d-129">Order</span></span> | <span data-ttu-id="a952d-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="a952d-130">Path</span></span>                          | <span data-ttu-id="a952d-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a952d-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="a952d-132">1</span><span class="sxs-lookup"><span data-stu-id="a952d-132">1</span></span>     | <span data-ttu-id="a952d-133">/app1/IFD/Exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="a952d-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="a952d-134">\_versión EXIF</span><span class="sxs-lookup"><span data-stu-id="a952d-134">exif\_version</span></span> |
| <span data-ttu-id="a952d-135">2</span><span class="sxs-lookup"><span data-stu-id="a952d-135">2</span></span>     | <span data-ttu-id="a952d-136">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="a952d-137">unicode</span><span class="sxs-lookup"><span data-stu-id="a952d-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="a952d-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a952d-138">Remove Paths</span></span>



| <span data-ttu-id="a952d-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="a952d-139">Order</span></span> | <span data-ttu-id="a952d-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="a952d-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a952d-141">1</span><span class="sxs-lookup"><span data-stu-id="a952d-141">1</span></span>     | <span data-ttu-id="a952d-142">/app1/IFD/Exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="a952d-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="a952d-143">2</span><span class="sxs-lookup"><span data-stu-id="a952d-143">2</span></span>     | <span data-ttu-id="a952d-144">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="a952d-145">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="a952d-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a952d-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a952d-146">Read Paths</span></span>



| <span data-ttu-id="a952d-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="a952d-147">Order</span></span> | <span data-ttu-id="a952d-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="a952d-148">Path</span></span>                      | <span data-ttu-id="a952d-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a952d-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="a952d-150">1</span><span class="sxs-lookup"><span data-stu-id="a952d-150">1</span></span>     | <span data-ttu-id="a952d-151">/IFD/Exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="a952d-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="a952d-152">\_versión EXIF</span><span class="sxs-lookup"><span data-stu-id="a952d-152">exif\_version</span></span> |
| <span data-ttu-id="a952d-153">2</span><span class="sxs-lookup"><span data-stu-id="a952d-153">2</span></span>     | <span data-ttu-id="a952d-154">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="a952d-155">unicode</span><span class="sxs-lookup"><span data-stu-id="a952d-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="a952d-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a952d-156">Write Paths</span></span>



| <span data-ttu-id="a952d-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="a952d-157">Order</span></span> | <span data-ttu-id="a952d-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="a952d-158">Path</span></span>                      | <span data-ttu-id="a952d-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a952d-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="a952d-160">1</span><span class="sxs-lookup"><span data-stu-id="a952d-160">1</span></span>     | <span data-ttu-id="a952d-161">/IFD/Exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="a952d-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="a952d-162">\_versión EXIF</span><span class="sxs-lookup"><span data-stu-id="a952d-162">exif\_version</span></span> |
| <span data-ttu-id="a952d-163">2</span><span class="sxs-lookup"><span data-stu-id="a952d-163">2</span></span>     | <span data-ttu-id="a952d-164">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="a952d-165">unicode</span><span class="sxs-lookup"><span data-stu-id="a952d-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="a952d-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a952d-166">Remove Paths</span></span>



| <span data-ttu-id="a952d-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="a952d-167">Order</span></span> | <span data-ttu-id="a952d-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="a952d-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a952d-169">1</span><span class="sxs-lookup"><span data-stu-id="a952d-169">1</span></span>     | <span data-ttu-id="a952d-170">/IFD/Exif/{ushort = 36864}</span><span class="sxs-lookup"><span data-stu-id="a952d-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="a952d-171">2</span><span class="sxs-lookup"><span data-stu-id="a952d-171">2</span></span>     | <span data-ttu-id="a952d-172">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a952d-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a952d-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a952d-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a952d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a952d-175">System. Photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="a952d-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
