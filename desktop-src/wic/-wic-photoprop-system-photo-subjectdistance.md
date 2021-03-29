---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Directiva de metadatos de la foto de System. Photo. SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911946"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="966c9-103">Directiva de metadatos de la foto de System. Photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="966c9-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. SubjectDistance](../properties/props-system-photo-subjectdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="966c9-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="966c9-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="966c9-105">PKEY</span></span>

<span data-ttu-id="966c9-106">PKEY \_ Photo \_ SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="966c9-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="966c9-107">Containers</span></span>

<span data-ttu-id="966c9-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="966c9-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="966c9-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="966c9-109">Read-Only</span></span>

<span data-ttu-id="966c9-110">Sí</span><span class="sxs-lookup"><span data-stu-id="966c9-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="966c9-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="966c9-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="966c9-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="966c9-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="966c9-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="966c9-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="966c9-114">Este valor se genera a partir de System. Photo. SubjectDistanceNumerator y System. Photo. SubjectDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="966c9-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="966c9-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="966c9-115">It cannot be written directly.</span></span> <span data-ttu-id="966c9-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="966c9-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="966c9-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="966c9-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="966c9-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="966c9-118">Read Paths</span></span>



| <span data-ttu-id="966c9-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="966c9-119">Order</span></span> | <span data-ttu-id="966c9-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="966c9-120">Path</span></span>                          | <span data-ttu-id="966c9-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="966c9-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="966c9-122">1</span><span class="sxs-lookup"><span data-stu-id="966c9-122">1</span></span>     | <span data-ttu-id="966c9-123">/app1/IFD/Exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="966c9-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="966c9-124">2</span><span class="sxs-lookup"><span data-stu-id="966c9-124">2</span></span>     | <span data-ttu-id="966c9-125">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="966c9-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="966c9-126">Write Paths</span></span>



| <span data-ttu-id="966c9-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="966c9-127">Order</span></span> | <span data-ttu-id="966c9-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="966c9-128">Path</span></span>                          | <span data-ttu-id="966c9-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="966c9-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="966c9-130">1</span><span class="sxs-lookup"><span data-stu-id="966c9-130">1</span></span>     | <span data-ttu-id="966c9-131">/app1/IFD/Exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="966c9-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="966c9-132">2</span><span class="sxs-lookup"><span data-stu-id="966c9-132">2</span></span>     | <span data-ttu-id="966c9-133">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="966c9-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="966c9-134">Remove Paths</span></span>



| <span data-ttu-id="966c9-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="966c9-135">Order</span></span> | <span data-ttu-id="966c9-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="966c9-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="966c9-137">1</span><span class="sxs-lookup"><span data-stu-id="966c9-137">1</span></span>     | <span data-ttu-id="966c9-138">/app1/IFD/Exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="966c9-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="966c9-139">2</span><span class="sxs-lookup"><span data-stu-id="966c9-139">2</span></span>     | <span data-ttu-id="966c9-140">/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="966c9-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="966c9-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="966c9-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="966c9-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="966c9-142">Read Paths</span></span>



| <span data-ttu-id="966c9-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="966c9-143">Order</span></span> | <span data-ttu-id="966c9-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="966c9-144">Path</span></span>                          | <span data-ttu-id="966c9-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="966c9-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="966c9-146">1</span><span class="sxs-lookup"><span data-stu-id="966c9-146">1</span></span>     | <span data-ttu-id="966c9-147">/IFD/Exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="966c9-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="966c9-148">2</span><span class="sxs-lookup"><span data-stu-id="966c9-148">2</span></span>     | <span data-ttu-id="966c9-149">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="966c9-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="966c9-150">Write Paths</span></span>



| <span data-ttu-id="966c9-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="966c9-151">Order</span></span> | <span data-ttu-id="966c9-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="966c9-152">Path</span></span>                          | <span data-ttu-id="966c9-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="966c9-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="966c9-154">1</span><span class="sxs-lookup"><span data-stu-id="966c9-154">1</span></span>     | <span data-ttu-id="966c9-155">/IFD/Exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="966c9-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="966c9-156">2</span><span class="sxs-lookup"><span data-stu-id="966c9-156">2</span></span>     | <span data-ttu-id="966c9-157">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="966c9-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="966c9-158">Remove Paths</span></span>



| <span data-ttu-id="966c9-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="966c9-159">Order</span></span> | <span data-ttu-id="966c9-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="966c9-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="966c9-161">1</span><span class="sxs-lookup"><span data-stu-id="966c9-161">1</span></span>     | <span data-ttu-id="966c9-162">/IFD/Exif/{ushort = 37382}</span><span class="sxs-lookup"><span data-stu-id="966c9-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="966c9-163">2</span><span class="sxs-lookup"><span data-stu-id="966c9-163">2</span></span>     | <span data-ttu-id="966c9-164">/ifd/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="966c9-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="966c9-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="966c9-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="966c9-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="966c9-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="966c9-167">System. Photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="966c9-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
