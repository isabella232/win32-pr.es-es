---
description: Directiva de metadatos de fotos para la propiedad System.Photo.FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Directiva de metadatos de fotos System.Photo.FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443626"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="5eca4-103">Directiva de metadatos de fotos System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="5eca4-104">Directiva de metadatos de fotos para [la propiedad System.Photo.FNumber.](../properties/props-system-photo-fnumber.md)</span><span class="sxs-lookup"><span data-stu-id="5eca4-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5eca4-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="5eca4-105">PKEY</span></span>

<span data-ttu-id="5eca4-106">PKEY \_ Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="5eca4-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="5eca4-107">Containers</span></span>

<span data-ttu-id="5eca4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5eca4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5eca4-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5eca4-109">Read-Only</span></span>

<span data-ttu-id="5eca4-110">Sí</span><span class="sxs-lookup"><span data-stu-id="5eca4-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5eca4-111">Tipo PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="5eca4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5eca4-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="5eca4-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5eca4-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="5eca4-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="5eca4-114">Este valor se genera a partir de System.Photo.FNumberNumerator y System.Photo.FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="5eca4-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="5eca4-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="5eca4-115">It cannot be written directly.</span></span> <span data-ttu-id="5eca4-116">Los valores de esquemas diferentes se concilian.</span><span class="sxs-lookup"><span data-stu-id="5eca4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5eca4-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="5eca4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5eca4-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-118">Read Paths</span></span>



| <span data-ttu-id="5eca4-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="5eca4-119">Order</span></span> | <span data-ttu-id="5eca4-120">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-120">Path</span></span>                          | <span data-ttu-id="5eca4-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5eca4-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5eca4-122">1</span><span class="sxs-lookup"><span data-stu-id="5eca4-122">1</span></span>     | <span data-ttu-id="5eca4-123">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="5eca4-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="5eca4-124">2</span><span class="sxs-lookup"><span data-stu-id="5eca4-124">2</span></span>     | <span data-ttu-id="5eca4-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="5eca4-126">Rutas de acceso de escritura</span><span class="sxs-lookup"><span data-stu-id="5eca4-126">Write Paths</span></span>



| <span data-ttu-id="5eca4-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="5eca4-127">Order</span></span> | <span data-ttu-id="5eca4-128">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-128">Path</span></span>                          | <span data-ttu-id="5eca4-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5eca4-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5eca4-130">1</span><span class="sxs-lookup"><span data-stu-id="5eca4-130">1</span></span>     | <span data-ttu-id="5eca4-131">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="5eca4-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="5eca4-132">2</span><span class="sxs-lookup"><span data-stu-id="5eca4-132">2</span></span>     | <span data-ttu-id="5eca4-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="5eca4-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-134">Remove Paths</span></span>



| <span data-ttu-id="5eca4-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="5eca4-135">Order</span></span> | <span data-ttu-id="5eca4-136">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5eca4-137">1</span><span class="sxs-lookup"><span data-stu-id="5eca4-137">1</span></span>     | <span data-ttu-id="5eca4-138">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="5eca4-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="5eca4-139">2</span><span class="sxs-lookup"><span data-stu-id="5eca4-139">2</span></span>     | <span data-ttu-id="5eca4-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="5eca4-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="5eca4-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5eca4-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-142">Read Paths</span></span>



| <span data-ttu-id="5eca4-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="5eca4-143">Order</span></span> | <span data-ttu-id="5eca4-144">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-144">Path</span></span>                     | <span data-ttu-id="5eca4-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5eca4-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5eca4-146">1</span><span class="sxs-lookup"><span data-stu-id="5eca4-146">1</span></span>     | <span data-ttu-id="5eca4-147">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="5eca4-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="5eca4-148">2</span><span class="sxs-lookup"><span data-stu-id="5eca4-148">2</span></span>     | <span data-ttu-id="5eca4-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="5eca4-150">Rutas de acceso de escritura</span><span class="sxs-lookup"><span data-stu-id="5eca4-150">Write Paths</span></span>



| <span data-ttu-id="5eca4-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="5eca4-151">Order</span></span> | <span data-ttu-id="5eca4-152">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-152">Path</span></span>                     | <span data-ttu-id="5eca4-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5eca4-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5eca4-154">1</span><span class="sxs-lookup"><span data-stu-id="5eca4-154">1</span></span>     | <span data-ttu-id="5eca4-155">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="5eca4-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="5eca4-156">2</span><span class="sxs-lookup"><span data-stu-id="5eca4-156">2</span></span>     | <span data-ttu-id="5eca4-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="5eca4-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-158">Remove Paths</span></span>



| <span data-ttu-id="5eca4-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="5eca4-159">Order</span></span> | <span data-ttu-id="5eca4-160">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5eca4-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="5eca4-161">1</span><span class="sxs-lookup"><span data-stu-id="5eca4-161">1</span></span>     | <span data-ttu-id="5eca4-162">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="5eca4-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="5eca4-163">2</span><span class="sxs-lookup"><span data-stu-id="5eca4-163">2</span></span>     | <span data-ttu-id="5eca4-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="5eca4-165">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5eca4-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eca4-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5eca4-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eca4-167">System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="5eca4-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
