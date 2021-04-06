---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Brightness.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Directiva de metadatos de foto de System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002794"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="d2d70-103">Directiva de metadatos de foto de System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="d2d70-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="d2d70-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. Brightness](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="d2d70-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d2d70-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d2d70-105">PKEY</span></span>

<span data-ttu-id="d2d70-106">Brillo de la \_ foto PKEY \_</span><span class="sxs-lookup"><span data-stu-id="d2d70-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="d2d70-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="d2d70-107">Containers</span></span>

<span data-ttu-id="d2d70-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d2d70-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d2d70-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2d70-109">Read-Only</span></span>

<span data-ttu-id="d2d70-110">Sí</span><span class="sxs-lookup"><span data-stu-id="d2d70-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="d2d70-111">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="d2d70-111">Input Type</span></span>

<span data-ttu-id="d2d70-112">Doble</span><span class="sxs-lookup"><span data-stu-id="d2d70-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d2d70-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="d2d70-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="d2d70-114">Este valor se genera a partir de System. Photo. ApertureNumerator y System. Photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="d2d70-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="d2d70-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="d2d70-115">It cannot be written directly.</span></span> <span data-ttu-id="d2d70-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="d2d70-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d2d70-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="d2d70-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d2d70-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d70-118">Read Paths</span></span>



| <span data-ttu-id="d2d70-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="d2d70-119">Order</span></span> | <span data-ttu-id="d2d70-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="d2d70-120">Path</span></span>                          | <span data-ttu-id="d2d70-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2d70-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d2d70-122">1</span><span class="sxs-lookup"><span data-stu-id="d2d70-122">1</span></span>     | <span data-ttu-id="d2d70-123">/app1/IFD/Exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="d2d70-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="d2d70-124">2</span><span class="sxs-lookup"><span data-stu-id="d2d70-124">2</span></span>     | <span data-ttu-id="d2d70-125">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="d2d70-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="d2d70-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d70-126">Write Paths</span></span>



| <span data-ttu-id="d2d70-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="d2d70-127">Order</span></span> | <span data-ttu-id="d2d70-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="d2d70-128">Path</span></span>                          | <span data-ttu-id="d2d70-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2d70-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d2d70-130">1</span><span class="sxs-lookup"><span data-stu-id="d2d70-130">1</span></span>     | <span data-ttu-id="d2d70-131">/app1/IFD/Exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="d2d70-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="d2d70-132">2</span><span class="sxs-lookup"><span data-stu-id="d2d70-132">2</span></span>     | <span data-ttu-id="d2d70-133">/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="d2d70-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d2d70-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d70-134">Remove Paths</span></span>



| <span data-ttu-id="d2d70-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="d2d70-135">Order</span></span> | <span data-ttu-id="d2d70-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="d2d70-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d2d70-137">1</span><span class="sxs-lookup"><span data-stu-id="d2d70-137">1</span></span>     | <span data-ttu-id="d2d70-138">/app1/IFD/Exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="d2d70-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="d2d70-139">2</span><span class="sxs-lookup"><span data-stu-id="d2d70-139">2</span></span>     | <span data-ttu-id="d2d70-140">/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="d2d70-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="d2d70-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="d2d70-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d2d70-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d70-142">Read Paths</span></span>



| <span data-ttu-id="d2d70-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="d2d70-143">Order</span></span> | <span data-ttu-id="d2d70-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="d2d70-144">Path</span></span>                          | <span data-ttu-id="d2d70-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2d70-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d2d70-146">1</span><span class="sxs-lookup"><span data-stu-id="d2d70-146">1</span></span>     | <span data-ttu-id="d2d70-147">/IFD/Exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="d2d70-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="d2d70-148">2</span><span class="sxs-lookup"><span data-stu-id="d2d70-148">2</span></span>     | <span data-ttu-id="d2d70-149">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="d2d70-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="d2d70-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d70-150">Write Paths</span></span>



| <span data-ttu-id="d2d70-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="d2d70-151">Order</span></span> | <span data-ttu-id="d2d70-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="d2d70-152">Path</span></span>                          | <span data-ttu-id="d2d70-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2d70-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d2d70-154">1</span><span class="sxs-lookup"><span data-stu-id="d2d70-154">1</span></span>     | <span data-ttu-id="d2d70-155">/IFD/Exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="d2d70-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="d2d70-156">2</span><span class="sxs-lookup"><span data-stu-id="d2d70-156">2</span></span>     | <span data-ttu-id="d2d70-157">/ifd/xmp/exif:BrightnessValue</span><span class="sxs-lookup"><span data-stu-id="d2d70-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d2d70-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="d2d70-158">Remove Paths</span></span>



| <span data-ttu-id="d2d70-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="d2d70-159">Order</span></span> | <span data-ttu-id="d2d70-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="d2d70-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d2d70-161">1</span><span class="sxs-lookup"><span data-stu-id="d2d70-161">1</span></span>     | <span data-ttu-id="d2d70-162">/IFD/Exif/{ushort = 37379}</span><span class="sxs-lookup"><span data-stu-id="d2d70-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="d2d70-163">2</span><span class="sxs-lookup"><span data-stu-id="d2d70-163">2</span></span>     | <span data-ttu-id="d2d70-164">/ifd/xmp/exif:brightnessvalue</span><span class="sxs-lookup"><span data-stu-id="d2d70-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d2d70-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2d70-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2d70-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d2d70-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2d70-167">System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="d2d70-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
