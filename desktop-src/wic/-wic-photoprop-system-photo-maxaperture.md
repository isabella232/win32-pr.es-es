---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Directiva de metadatos de la foto de System. Photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678095"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="7c8af-103">Directiva de metadatos de la foto de System. Photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="7c8af-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="7c8af-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8af-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7c8af-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7c8af-105">PKEY</span></span>

<span data-ttu-id="7c8af-106">PKEY \_ Photo \_ MaxAperture</span><span class="sxs-lookup"><span data-stu-id="7c8af-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="7c8af-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="7c8af-107">Containers</span></span>

<span data-ttu-id="7c8af-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7c8af-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7c8af-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c8af-109">Read-Only</span></span>

<span data-ttu-id="7c8af-110">Sí</span><span class="sxs-lookup"><span data-stu-id="7c8af-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7c8af-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="7c8af-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7c8af-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="7c8af-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="7c8af-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="7c8af-113">Input Type</span></span>

<span data-ttu-id="7c8af-114">Doble</span><span class="sxs-lookup"><span data-stu-id="7c8af-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7c8af-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="7c8af-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7c8af-116">Este valor se genera a partir de System. Photo. MaxApertureNumerator y System. Photo. MaxApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="7c8af-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="7c8af-117">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="7c8af-117">It cannot be written directly.</span></span> <span data-ttu-id="7c8af-118">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="7c8af-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7c8af-119">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="7c8af-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7c8af-120">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7c8af-120">Read Paths</span></span>



| <span data-ttu-id="7c8af-121">Pedido</span><span class="sxs-lookup"><span data-stu-id="7c8af-121">Order</span></span> | <span data-ttu-id="7c8af-122">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c8af-122">Path</span></span>                          | <span data-ttu-id="7c8af-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c8af-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="7c8af-124">1</span><span class="sxs-lookup"><span data-stu-id="7c8af-124">1</span></span>     | <span data-ttu-id="7c8af-125">/app1/IFD/Exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="7c8af-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="7c8af-126">2</span><span class="sxs-lookup"><span data-stu-id="7c8af-126">2</span></span>     | <span data-ttu-id="7c8af-127">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="7c8af-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="7c8af-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7c8af-128">Write Paths</span></span>



| <span data-ttu-id="7c8af-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="7c8af-129">Order</span></span> | <span data-ttu-id="7c8af-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c8af-130">Path</span></span>                          | <span data-ttu-id="7c8af-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c8af-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="7c8af-132">1</span><span class="sxs-lookup"><span data-stu-id="7c8af-132">1</span></span>     | <span data-ttu-id="7c8af-133">/app1/IFD/Exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="7c8af-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="7c8af-134">2</span><span class="sxs-lookup"><span data-stu-id="7c8af-134">2</span></span>     | <span data-ttu-id="7c8af-135">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="7c8af-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="7c8af-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7c8af-136">Remove Paths</span></span>



| <span data-ttu-id="7c8af-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="7c8af-137">Order</span></span> | <span data-ttu-id="7c8af-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c8af-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="7c8af-139">1</span><span class="sxs-lookup"><span data-stu-id="7c8af-139">1</span></span>     | <span data-ttu-id="7c8af-140">/app1/IFD/Exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="7c8af-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="7c8af-141">2</span><span class="sxs-lookup"><span data-stu-id="7c8af-141">2</span></span>     | <span data-ttu-id="7c8af-142">/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="7c8af-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="7c8af-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="7c8af-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7c8af-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7c8af-144">Read Paths</span></span>



| <span data-ttu-id="7c8af-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="7c8af-145">Order</span></span> | <span data-ttu-id="7c8af-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c8af-146">Path</span></span>                           | <span data-ttu-id="7c8af-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c8af-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="7c8af-148">1</span><span class="sxs-lookup"><span data-stu-id="7c8af-148">1</span></span>     | <span data-ttu-id="7c8af-149">/IFD/Exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="7c8af-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="7c8af-150">2</span><span class="sxs-lookup"><span data-stu-id="7c8af-150">2</span></span>     | <span data-ttu-id="7c8af-151">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="7c8af-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="7c8af-152">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7c8af-152">Write Paths</span></span>



| <span data-ttu-id="7c8af-153">Pedido</span><span class="sxs-lookup"><span data-stu-id="7c8af-153">Order</span></span> | <span data-ttu-id="7c8af-154">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c8af-154">Path</span></span>                           | <span data-ttu-id="7c8af-155">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c8af-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="7c8af-156">1</span><span class="sxs-lookup"><span data-stu-id="7c8af-156">1</span></span>     | <span data-ttu-id="7c8af-157">/IFD/Exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="7c8af-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="7c8af-158">2</span><span class="sxs-lookup"><span data-stu-id="7c8af-158">2</span></span>     | <span data-ttu-id="7c8af-159">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="7c8af-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="7c8af-160">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7c8af-160">Remove Paths</span></span>



| <span data-ttu-id="7c8af-161">Pedido</span><span class="sxs-lookup"><span data-stu-id="7c8af-161">Order</span></span> | <span data-ttu-id="7c8af-162">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c8af-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="7c8af-163">1</span><span class="sxs-lookup"><span data-stu-id="7c8af-163">1</span></span>     | <span data-ttu-id="7c8af-164">/IFD/Exif/{ushort = 37381}</span><span class="sxs-lookup"><span data-stu-id="7c8af-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="7c8af-165">2</span><span class="sxs-lookup"><span data-stu-id="7c8af-165">2</span></span>     | <span data-ttu-id="7c8af-166">/ifd/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="7c8af-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7c8af-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c8af-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c8af-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c8af-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c8af-169">System. Photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="7c8af-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
