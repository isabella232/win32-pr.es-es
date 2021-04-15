---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Directiva de metadatos de la foto de System. Image. ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545718"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="522e3-103">Directiva de metadatos de la foto de System. Image. ImageID</span><span class="sxs-lookup"><span data-stu-id="522e3-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="522e3-104">La Directiva de metadatos de la fotografía para la propiedad [System. Image. ImageID](../properties/props-system-image-imageid.md) .</span><span class="sxs-lookup"><span data-stu-id="522e3-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="522e3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="522e3-105">PKEY</span></span>

<span data-ttu-id="522e3-106">PKEY \_ Image \_ ImageID</span><span class="sxs-lookup"><span data-stu-id="522e3-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="522e3-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="522e3-107">Containers</span></span>

<span data-ttu-id="522e3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="522e3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="522e3-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="522e3-109">Read-Only</span></span>

<span data-ttu-id="522e3-110">No</span><span class="sxs-lookup"><span data-stu-id="522e3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="522e3-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="522e3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="522e3-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="522e3-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="522e3-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="522e3-113">Input Type</span></span>

<span data-ttu-id="522e3-114">String.</span><span class="sxs-lookup"><span data-stu-id="522e3-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="522e3-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="522e3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="522e3-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="522e3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="522e3-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="522e3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="522e3-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="522e3-118">Read Paths</span></span>



| <span data-ttu-id="522e3-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="522e3-119">Order</span></span> | <span data-ttu-id="522e3-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="522e3-120">Path</span></span>                          | <span data-ttu-id="522e3-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="522e3-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="522e3-122">1</span><span class="sxs-lookup"><span data-stu-id="522e3-122">1</span></span>     | <span data-ttu-id="522e3-123">/app1/IFD/Exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="522e3-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="522e3-124">ascii</span><span class="sxs-lookup"><span data-stu-id="522e3-124">ascii</span></span>       |
| <span data-ttu-id="522e3-125">2</span><span class="sxs-lookup"><span data-stu-id="522e3-125">2</span></span>     | <span data-ttu-id="522e3-126">/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="522e3-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="522e3-127">unicode</span><span class="sxs-lookup"><span data-stu-id="522e3-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="522e3-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="522e3-128">Write Paths</span></span>



| <span data-ttu-id="522e3-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="522e3-129">Order</span></span> | <span data-ttu-id="522e3-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="522e3-130">Path</span></span>                          | <span data-ttu-id="522e3-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="522e3-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="522e3-132">1</span><span class="sxs-lookup"><span data-stu-id="522e3-132">1</span></span>     | <span data-ttu-id="522e3-133">/app1/IFD/Exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="522e3-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="522e3-134">ascii</span><span class="sxs-lookup"><span data-stu-id="522e3-134">ascii</span></span>       |
| <span data-ttu-id="522e3-135">2</span><span class="sxs-lookup"><span data-stu-id="522e3-135">2</span></span>     | <span data-ttu-id="522e3-136">/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="522e3-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="522e3-137">unicode</span><span class="sxs-lookup"><span data-stu-id="522e3-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="522e3-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="522e3-138">Remove Paths</span></span>



| <span data-ttu-id="522e3-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="522e3-139">Order</span></span> | <span data-ttu-id="522e3-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="522e3-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="522e3-141">1</span><span class="sxs-lookup"><span data-stu-id="522e3-141">1</span></span>     | <span data-ttu-id="522e3-142">/app1/IFD/Exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="522e3-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="522e3-143">2</span><span class="sxs-lookup"><span data-stu-id="522e3-143">2</span></span>     | <span data-ttu-id="522e3-144">/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="522e3-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="522e3-145">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="522e3-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="522e3-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="522e3-146">Read Paths</span></span>



| <span data-ttu-id="522e3-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="522e3-147">Order</span></span> | <span data-ttu-id="522e3-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="522e3-148">Path</span></span>                        | <span data-ttu-id="522e3-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="522e3-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="522e3-150">/IFD/Exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="522e3-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="522e3-151">ascii</span><span class="sxs-lookup"><span data-stu-id="522e3-151">ascii</span></span>       |
|       | <span data-ttu-id="522e3-152">/ifd/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="522e3-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="522e3-153">unicode</span><span class="sxs-lookup"><span data-stu-id="522e3-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="522e3-154">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="522e3-154">Write Paths</span></span>



| <span data-ttu-id="522e3-155">Pedido</span><span class="sxs-lookup"><span data-stu-id="522e3-155">Order</span></span> | <span data-ttu-id="522e3-156">Ruta</span><span class="sxs-lookup"><span data-stu-id="522e3-156">Path</span></span>                        | <span data-ttu-id="522e3-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="522e3-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="522e3-158">/IFD/Exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="522e3-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="522e3-159">ascii</span><span class="sxs-lookup"><span data-stu-id="522e3-159">ascii</span></span>       |
|       | <span data-ttu-id="522e3-160">/ifd/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="522e3-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="522e3-161">unicode</span><span class="sxs-lookup"><span data-stu-id="522e3-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="522e3-162">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="522e3-162">Remove Paths</span></span>



| <span data-ttu-id="522e3-163">Pedido</span><span class="sxs-lookup"><span data-stu-id="522e3-163">Order</span></span> | <span data-ttu-id="522e3-164">Ruta</span><span class="sxs-lookup"><span data-stu-id="522e3-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="522e3-165">/IFD/Exif/{ushort = 42016}</span><span class="sxs-lookup"><span data-stu-id="522e3-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="522e3-166">/ifd/xmp/exif:ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="522e3-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="522e3-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="522e3-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="522e3-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="522e3-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="522e3-169">System. Image. ImageID</span><span class="sxs-lookup"><span data-stu-id="522e3-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
