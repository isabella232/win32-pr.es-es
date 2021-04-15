---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Directiva de metadatos de fotografía de System. Photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547043"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="3ea60-103">Directiva de metadatos de fotografía de System. Photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="3ea60-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="3ea60-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. Contrast](../properties/props-system-photo-contrast.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea60-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3ea60-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3ea60-105">PKEY</span></span>

<span data-ttu-id="3ea60-106">PKEY \_ contraste de fotografía \_</span><span class="sxs-lookup"><span data-stu-id="3ea60-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="3ea60-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="3ea60-107">Containers</span></span>

<span data-ttu-id="3ea60-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3ea60-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3ea60-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ea60-109">Read-Only</span></span>

<span data-ttu-id="3ea60-110">No</span><span class="sxs-lookup"><span data-stu-id="3ea60-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3ea60-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="3ea60-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3ea60-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="3ea60-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="3ea60-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="3ea60-113">Input Type</span></span>

<span data-ttu-id="3ea60-114">UShort</span><span class="sxs-lookup"><span data-stu-id="3ea60-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3ea60-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="3ea60-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3ea60-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="3ea60-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3ea60-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="3ea60-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3ea60-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3ea60-118">Read Paths</span></span>



| <span data-ttu-id="3ea60-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="3ea60-119">Order</span></span> | <span data-ttu-id="3ea60-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ea60-120">Path</span></span>                          | <span data-ttu-id="3ea60-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3ea60-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3ea60-122">1</span><span class="sxs-lookup"><span data-stu-id="3ea60-122">1</span></span>     | <span data-ttu-id="3ea60-123">/app1/IFD/Exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="3ea60-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="3ea60-124">ushort</span><span class="sxs-lookup"><span data-stu-id="3ea60-124">ushort</span></span>      |
| <span data-ttu-id="3ea60-125">2</span><span class="sxs-lookup"><span data-stu-id="3ea60-125">2</span></span>     | <span data-ttu-id="3ea60-126">/XMP/Exif: contraste</span><span class="sxs-lookup"><span data-stu-id="3ea60-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="3ea60-127">unicode</span><span class="sxs-lookup"><span data-stu-id="3ea60-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3ea60-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3ea60-128">Write Paths</span></span>



| <span data-ttu-id="3ea60-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="3ea60-129">Order</span></span> | <span data-ttu-id="3ea60-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ea60-130">Path</span></span>                          | <span data-ttu-id="3ea60-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3ea60-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="3ea60-132">1</span><span class="sxs-lookup"><span data-stu-id="3ea60-132">1</span></span>     | <span data-ttu-id="3ea60-133">/app1/IFD/Exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="3ea60-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="3ea60-134">ushort</span><span class="sxs-lookup"><span data-stu-id="3ea60-134">ushort</span></span>      |
| <span data-ttu-id="3ea60-135">2</span><span class="sxs-lookup"><span data-stu-id="3ea60-135">2</span></span>     | <span data-ttu-id="3ea60-136">/XMP/Exif: contraste</span><span class="sxs-lookup"><span data-stu-id="3ea60-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="3ea60-137">unicode</span><span class="sxs-lookup"><span data-stu-id="3ea60-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3ea60-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3ea60-138">Remove Paths</span></span>



| <span data-ttu-id="3ea60-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="3ea60-139">Order</span></span> | <span data-ttu-id="3ea60-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ea60-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="3ea60-141">1</span><span class="sxs-lookup"><span data-stu-id="3ea60-141">1</span></span>     | <span data-ttu-id="3ea60-142">/app1/IFD/Exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="3ea60-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="3ea60-143">2</span><span class="sxs-lookup"><span data-stu-id="3ea60-143">2</span></span>     | <span data-ttu-id="3ea60-144">/XMP/Exif: contraste</span><span class="sxs-lookup"><span data-stu-id="3ea60-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="3ea60-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="3ea60-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3ea60-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3ea60-146">Read Paths</span></span>



| <span data-ttu-id="3ea60-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="3ea60-147">Order</span></span> | <span data-ttu-id="3ea60-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ea60-148">Path</span></span>                     | <span data-ttu-id="3ea60-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3ea60-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3ea60-150">1</span><span class="sxs-lookup"><span data-stu-id="3ea60-150">1</span></span>     | <span data-ttu-id="3ea60-151">/IFD/Exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="3ea60-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="3ea60-152">ushort</span><span class="sxs-lookup"><span data-stu-id="3ea60-152">ushort</span></span>      |
| <span data-ttu-id="3ea60-153">2</span><span class="sxs-lookup"><span data-stu-id="3ea60-153">2</span></span>     | <span data-ttu-id="3ea60-154">/IFD/XMP/Exif: contraste</span><span class="sxs-lookup"><span data-stu-id="3ea60-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="3ea60-155">unicode</span><span class="sxs-lookup"><span data-stu-id="3ea60-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3ea60-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3ea60-156">Write Paths</span></span>



| <span data-ttu-id="3ea60-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="3ea60-157">Order</span></span> | <span data-ttu-id="3ea60-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ea60-158">Path</span></span>                     | <span data-ttu-id="3ea60-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3ea60-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3ea60-160">1</span><span class="sxs-lookup"><span data-stu-id="3ea60-160">1</span></span>     | <span data-ttu-id="3ea60-161">/IFD/Exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="3ea60-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="3ea60-162">ushort</span><span class="sxs-lookup"><span data-stu-id="3ea60-162">ushort</span></span>      |
| <span data-ttu-id="3ea60-163">2</span><span class="sxs-lookup"><span data-stu-id="3ea60-163">2</span></span>     | <span data-ttu-id="3ea60-164">/IFD/XMP/Exif: contraste</span><span class="sxs-lookup"><span data-stu-id="3ea60-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="3ea60-165">unicode</span><span class="sxs-lookup"><span data-stu-id="3ea60-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3ea60-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3ea60-166">Remove Paths</span></span>



| <span data-ttu-id="3ea60-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="3ea60-167">Order</span></span> | <span data-ttu-id="3ea60-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ea60-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="3ea60-169">1</span><span class="sxs-lookup"><span data-stu-id="3ea60-169">1</span></span>     | <span data-ttu-id="3ea60-170">/IFD/Exif/{ushort = 41992}</span><span class="sxs-lookup"><span data-stu-id="3ea60-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="3ea60-171">2</span><span class="sxs-lookup"><span data-stu-id="3ea60-171">2</span></span>     | <span data-ttu-id="3ea60-172">/IFD/XMP/Exif: contraste</span><span class="sxs-lookup"><span data-stu-id="3ea60-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="3ea60-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ea60-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ea60-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3ea60-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ea60-175">System. Photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="3ea60-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
