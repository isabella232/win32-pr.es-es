---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Directiva de metadatos de la foto de System. Photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716445"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="45ab5-103">Directiva de metadatos de la foto de System. Photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="45ab5-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. FocalLength](../properties/props-system-photo-focallength.md) .</span><span class="sxs-lookup"><span data-stu-id="45ab5-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="45ab5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="45ab5-105">PKEY</span></span>

<span data-ttu-id="45ab5-106">PKEY \_ Photo \_ FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="45ab5-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="45ab5-107">Containers</span></span>

<span data-ttu-id="45ab5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="45ab5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="45ab5-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="45ab5-109">Read-Only</span></span>

<span data-ttu-id="45ab5-110">Sí</span><span class="sxs-lookup"><span data-stu-id="45ab5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="45ab5-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="45ab5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="45ab5-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="45ab5-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="45ab5-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="45ab5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="45ab5-114">Este valor se genera a partir de System. Photo. FocalLengthNumerator y System. Photo. FocalLengthDenominator.</span><span class="sxs-lookup"><span data-stu-id="45ab5-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="45ab5-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="45ab5-115">It cannot be written directly.</span></span> <span data-ttu-id="45ab5-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="45ab5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="45ab5-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="45ab5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="45ab5-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="45ab5-118">Read Paths</span></span>



| <span data-ttu-id="45ab5-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="45ab5-119">Order</span></span> | <span data-ttu-id="45ab5-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="45ab5-120">Path</span></span>                          | <span data-ttu-id="45ab5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45ab5-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="45ab5-122">1</span><span class="sxs-lookup"><span data-stu-id="45ab5-122">1</span></span>     | <span data-ttu-id="45ab5-123">/app1/IFD/Exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="45ab5-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="45ab5-124">2</span><span class="sxs-lookup"><span data-stu-id="45ab5-124">2</span></span>     | <span data-ttu-id="45ab5-125">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="45ab5-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="45ab5-126">Write Paths</span></span>



| <span data-ttu-id="45ab5-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="45ab5-127">Order</span></span> | <span data-ttu-id="45ab5-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="45ab5-128">Path</span></span>                          | <span data-ttu-id="45ab5-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45ab5-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="45ab5-130">1</span><span class="sxs-lookup"><span data-stu-id="45ab5-130">1</span></span>     | <span data-ttu-id="45ab5-131">/app1/IFD/Exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="45ab5-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="45ab5-132">2</span><span class="sxs-lookup"><span data-stu-id="45ab5-132">2</span></span>     | <span data-ttu-id="45ab5-133">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="45ab5-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="45ab5-134">Remove Paths</span></span>



| <span data-ttu-id="45ab5-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="45ab5-135">Order</span></span> | <span data-ttu-id="45ab5-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="45ab5-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="45ab5-137">1</span><span class="sxs-lookup"><span data-stu-id="45ab5-137">1</span></span>     | <span data-ttu-id="45ab5-138">/app1/IFD/Exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="45ab5-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="45ab5-139">2</span><span class="sxs-lookup"><span data-stu-id="45ab5-139">2</span></span>     | <span data-ttu-id="45ab5-140">/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="45ab5-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="45ab5-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="45ab5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="45ab5-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="45ab5-142">Read Paths</span></span>



| <span data-ttu-id="45ab5-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="45ab5-143">Order</span></span> | <span data-ttu-id="45ab5-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="45ab5-144">Path</span></span>                      | <span data-ttu-id="45ab5-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45ab5-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="45ab5-146">1</span><span class="sxs-lookup"><span data-stu-id="45ab5-146">1</span></span>     | <span data-ttu-id="45ab5-147">/IFD/Exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="45ab5-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="45ab5-148">2</span><span class="sxs-lookup"><span data-stu-id="45ab5-148">2</span></span>     | <span data-ttu-id="45ab5-149">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="45ab5-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="45ab5-150">Write Paths</span></span>



| <span data-ttu-id="45ab5-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="45ab5-151">Order</span></span> | <span data-ttu-id="45ab5-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="45ab5-152">Path</span></span>                      | <span data-ttu-id="45ab5-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45ab5-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="45ab5-154">1</span><span class="sxs-lookup"><span data-stu-id="45ab5-154">1</span></span>     | <span data-ttu-id="45ab5-155">/IFD/Exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="45ab5-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="45ab5-156">2</span><span class="sxs-lookup"><span data-stu-id="45ab5-156">2</span></span>     | <span data-ttu-id="45ab5-157">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="45ab5-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="45ab5-158">Remove Paths</span></span>



| <span data-ttu-id="45ab5-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="45ab5-159">Order</span></span> | <span data-ttu-id="45ab5-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="45ab5-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="45ab5-161">1</span><span class="sxs-lookup"><span data-stu-id="45ab5-161">1</span></span>     | <span data-ttu-id="45ab5-162">/IFD/Exif/{ushort = 37386}</span><span class="sxs-lookup"><span data-stu-id="45ab5-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="45ab5-163">2</span><span class="sxs-lookup"><span data-stu-id="45ab5-163">2</span></span>     | <span data-ttu-id="45ab5-164">/ifd/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="45ab5-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="45ab5-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45ab5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="45ab5-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45ab5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45ab5-167">System. Photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="45ab5-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
