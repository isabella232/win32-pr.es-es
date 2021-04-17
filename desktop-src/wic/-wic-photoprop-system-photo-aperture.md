---
description: La Directiva de metadatos de la fotografía para la propiedad System. Photo. abertura.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Directiva de metadatos de fotografía de System. Photo. abertura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688386"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="88500-103">Directiva de metadatos de fotografía de System. Photo. abertura</span><span class="sxs-lookup"><span data-stu-id="88500-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="88500-104">La Directiva de metadatos de la fotografía para la propiedad [System. Photo. abertura](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="88500-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="88500-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="88500-105">PKEY</span></span>

<span data-ttu-id="88500-106">\_Abertura de fotografía de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="88500-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="88500-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="88500-107">Containers</span></span>

<span data-ttu-id="88500-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="88500-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="88500-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88500-109">Read-Only</span></span>

<span data-ttu-id="88500-110">Sí</span><span class="sxs-lookup"><span data-stu-id="88500-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="88500-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="88500-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="88500-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="88500-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="88500-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="88500-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="88500-114">Este valor se genera a partir de System. Photo. ApertureNumerator y System. Photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="88500-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="88500-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="88500-115">It cannot be written directly.</span></span> <span data-ttu-id="88500-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="88500-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="88500-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="88500-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="88500-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88500-118">Read Paths</span></span>



| <span data-ttu-id="88500-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="88500-119">Order</span></span> | <span data-ttu-id="88500-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="88500-120">Path</span></span>                          | <span data-ttu-id="88500-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88500-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="88500-122">1</span><span class="sxs-lookup"><span data-stu-id="88500-122">1</span></span>     | <span data-ttu-id="88500-123">/app1/IFD/Exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="88500-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="88500-124">2</span><span class="sxs-lookup"><span data-stu-id="88500-124">2</span></span>     | <span data-ttu-id="88500-125">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="88500-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="88500-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88500-126">Write Paths</span></span>



| <span data-ttu-id="88500-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="88500-127">Order</span></span> | <span data-ttu-id="88500-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="88500-128">Path</span></span>                          | <span data-ttu-id="88500-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88500-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="88500-130">1</span><span class="sxs-lookup"><span data-stu-id="88500-130">1</span></span>     | <span data-ttu-id="88500-131">/app1/IFD/Exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="88500-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="88500-132">2</span><span class="sxs-lookup"><span data-stu-id="88500-132">2</span></span>     | <span data-ttu-id="88500-133">/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="88500-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="88500-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88500-134">Remove Paths</span></span>



| <span data-ttu-id="88500-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="88500-135">Order</span></span> | <span data-ttu-id="88500-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="88500-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="88500-137">1</span><span class="sxs-lookup"><span data-stu-id="88500-137">1</span></span>     | <span data-ttu-id="88500-138">/app1/IFD/Exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="88500-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="88500-139">2</span><span class="sxs-lookup"><span data-stu-id="88500-139">2</span></span>     | <span data-ttu-id="88500-140">/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="88500-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="88500-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="88500-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="88500-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88500-142">Read Paths</span></span>



| <span data-ttu-id="88500-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="88500-143">Order</span></span> | <span data-ttu-id="88500-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="88500-144">Path</span></span>                        | <span data-ttu-id="88500-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88500-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="88500-146">1</span><span class="sxs-lookup"><span data-stu-id="88500-146">1</span></span>     | <span data-ttu-id="88500-147">/IFD/Exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="88500-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="88500-148">2</span><span class="sxs-lookup"><span data-stu-id="88500-148">2</span></span>     | <span data-ttu-id="88500-149">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="88500-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="88500-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88500-150">Write Paths</span></span>



| <span data-ttu-id="88500-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="88500-151">Order</span></span> | <span data-ttu-id="88500-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="88500-152">Path</span></span>                        | <span data-ttu-id="88500-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88500-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="88500-154">1</span><span class="sxs-lookup"><span data-stu-id="88500-154">1</span></span>     | <span data-ttu-id="88500-155">/IFD/Exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="88500-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="88500-156">2</span><span class="sxs-lookup"><span data-stu-id="88500-156">2</span></span>     | <span data-ttu-id="88500-157">/ifd/xmp/exif:ApertureValue</span><span class="sxs-lookup"><span data-stu-id="88500-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="88500-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88500-158">Remove Paths</span></span>



| <span data-ttu-id="88500-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="88500-159">Order</span></span> | <span data-ttu-id="88500-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="88500-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="88500-161">1</span><span class="sxs-lookup"><span data-stu-id="88500-161">1</span></span>     | <span data-ttu-id="88500-162">/IFD/Exif/{ushort = 37378}</span><span class="sxs-lookup"><span data-stu-id="88500-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="88500-163">2</span><span class="sxs-lookup"><span data-stu-id="88500-163">2</span></span>     | <span data-ttu-id="88500-164">/ifd/xmp/exif:aperturevalue</span><span class="sxs-lookup"><span data-stu-id="88500-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="88500-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88500-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="88500-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88500-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88500-167">System. Photo. abertura</span><span class="sxs-lookup"><span data-stu-id="88500-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
