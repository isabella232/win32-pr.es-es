---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Directiva de metadatos de la foto de System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706405"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="4e64e-103">Directiva de metadatos de la foto de System. Image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="4e64e-104">La Directiva de metadatos de la fotografía para la propiedad [System. Image. ColorSpace](../properties/props-system-image-colorspace.md) .</span><span class="sxs-lookup"><span data-stu-id="4e64e-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4e64e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4e64e-105">PKEY</span></span>

<span data-ttu-id="4e64e-106">PKEY \_ Image \_ ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="4e64e-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4e64e-107">Containers</span></span>

<span data-ttu-id="4e64e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4e64e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4e64e-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e64e-109">Read-Only</span></span>

<span data-ttu-id="4e64e-110">Sí</span><span class="sxs-lookup"><span data-stu-id="4e64e-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4e64e-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="4e64e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4e64e-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="4e64e-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="4e64e-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="4e64e-113">Input Type</span></span>

<span data-ttu-id="4e64e-114">UShort</span><span class="sxs-lookup"><span data-stu-id="4e64e-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4e64e-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="4e64e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4e64e-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="4e64e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4e64e-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="4e64e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4e64e-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4e64e-118">Read Paths</span></span>



| <span data-ttu-id="4e64e-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="4e64e-119">Order</span></span> | <span data-ttu-id="4e64e-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="4e64e-120">Path</span></span>                          | <span data-ttu-id="4e64e-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4e64e-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4e64e-122">1</span><span class="sxs-lookup"><span data-stu-id="4e64e-122">1</span></span>     | <span data-ttu-id="4e64e-123">/app1/IFD/Exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="4e64e-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="4e64e-124">ushort</span><span class="sxs-lookup"><span data-stu-id="4e64e-124">ushort</span></span>      |
| <span data-ttu-id="4e64e-125">2</span><span class="sxs-lookup"><span data-stu-id="4e64e-125">2</span></span>     | <span data-ttu-id="4e64e-126">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="4e64e-127">unicode</span><span class="sxs-lookup"><span data-stu-id="4e64e-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4e64e-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4e64e-128">Write Paths</span></span>



| <span data-ttu-id="4e64e-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="4e64e-129">Order</span></span> | <span data-ttu-id="4e64e-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="4e64e-130">Path</span></span>                          | <span data-ttu-id="4e64e-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4e64e-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4e64e-132">1</span><span class="sxs-lookup"><span data-stu-id="4e64e-132">1</span></span>     | <span data-ttu-id="4e64e-133">/app1/IFD/Exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="4e64e-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="4e64e-134">ushort</span><span class="sxs-lookup"><span data-stu-id="4e64e-134">ushort</span></span>      |
| <span data-ttu-id="4e64e-135">2</span><span class="sxs-lookup"><span data-stu-id="4e64e-135">2</span></span>     | <span data-ttu-id="4e64e-136">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="4e64e-137">unicode</span><span class="sxs-lookup"><span data-stu-id="4e64e-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4e64e-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4e64e-138">Remove Paths</span></span>



| <span data-ttu-id="4e64e-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="4e64e-139">Order</span></span> | <span data-ttu-id="4e64e-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="4e64e-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="4e64e-141">1</span><span class="sxs-lookup"><span data-stu-id="4e64e-141">1</span></span>     | <span data-ttu-id="4e64e-142">/app1/IFD/Exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="4e64e-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="4e64e-143">2</span><span class="sxs-lookup"><span data-stu-id="4e64e-143">2</span></span>     | <span data-ttu-id="4e64e-144">/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="4e64e-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="4e64e-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="4e64e-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4e64e-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4e64e-146">Read Paths</span></span>



| <span data-ttu-id="4e64e-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="4e64e-147">Order</span></span> | <span data-ttu-id="4e64e-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="4e64e-148">Path</span></span>                     | <span data-ttu-id="4e64e-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4e64e-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4e64e-150">1</span><span class="sxs-lookup"><span data-stu-id="4e64e-150">1</span></span>     | <span data-ttu-id="4e64e-151">/IFD/Exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="4e64e-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="4e64e-152">ushort</span><span class="sxs-lookup"><span data-stu-id="4e64e-152">ushort</span></span>      |
| <span data-ttu-id="4e64e-153">2</span><span class="sxs-lookup"><span data-stu-id="4e64e-153">2</span></span>     | <span data-ttu-id="4e64e-154">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="4e64e-155">unicode</span><span class="sxs-lookup"><span data-stu-id="4e64e-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4e64e-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4e64e-156">Write Paths</span></span>



| <span data-ttu-id="4e64e-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="4e64e-157">Order</span></span> | <span data-ttu-id="4e64e-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="4e64e-158">Path</span></span>                     | <span data-ttu-id="4e64e-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4e64e-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4e64e-160">1</span><span class="sxs-lookup"><span data-stu-id="4e64e-160">1</span></span>     | <span data-ttu-id="4e64e-161">/IFD/Exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="4e64e-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="4e64e-162">ushort</span><span class="sxs-lookup"><span data-stu-id="4e64e-162">ushort</span></span>      |
| <span data-ttu-id="4e64e-163">2</span><span class="sxs-lookup"><span data-stu-id="4e64e-163">2</span></span>     | <span data-ttu-id="4e64e-164">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="4e64e-165">unicode</span><span class="sxs-lookup"><span data-stu-id="4e64e-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4e64e-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4e64e-166">Remove Paths</span></span>



| <span data-ttu-id="4e64e-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="4e64e-167">Order</span></span> | <span data-ttu-id="4e64e-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="4e64e-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4e64e-169">1</span><span class="sxs-lookup"><span data-stu-id="4e64e-169">1</span></span>     | <span data-ttu-id="4e64e-170">/IFD/Exif/{ushort = 40961}</span><span class="sxs-lookup"><span data-stu-id="4e64e-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="4e64e-171">2</span><span class="sxs-lookup"><span data-stu-id="4e64e-171">2</span></span>     | <span data-ttu-id="4e64e-172">/ifd/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="4e64e-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4e64e-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e64e-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e64e-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e64e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e64e-175">System. Image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="4e64e-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
