---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Directiva de metadatos de la foto de System. Photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277616"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="4ebcc-103">Directiva de metadatos de la foto de System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="4ebcc-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. FNumber](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="4ebcc-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4ebcc-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4ebcc-105">PKEY</span></span>

<span data-ttu-id="4ebcc-106">PKEY \_ Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="4ebcc-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4ebcc-107">Containers</span></span>

<span data-ttu-id="4ebcc-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4ebcc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4ebcc-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4ebcc-109">Read-Only</span></span>

<span data-ttu-id="4ebcc-110">Sí</span><span class="sxs-lookup"><span data-stu-id="4ebcc-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4ebcc-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="4ebcc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4ebcc-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4ebcc-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4ebcc-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="4ebcc-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="4ebcc-114">Este valor se genera a partir de System. Photo. FNumberNumerator y System. Photo. FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="4ebcc-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-115">It cannot be written directly.</span></span> <span data-ttu-id="4ebcc-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="4ebcc-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4ebcc-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="4ebcc-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4ebcc-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4ebcc-118">Read Paths</span></span>



| <span data-ttu-id="4ebcc-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="4ebcc-119">Order</span></span> | <span data-ttu-id="4ebcc-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="4ebcc-120">Path</span></span>                          | <span data-ttu-id="4ebcc-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4ebcc-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="4ebcc-122">1</span><span class="sxs-lookup"><span data-stu-id="4ebcc-122">1</span></span>     | <span data-ttu-id="4ebcc-123">/app1/IFD/Exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="4ebcc-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="4ebcc-124">2</span><span class="sxs-lookup"><span data-stu-id="4ebcc-124">2</span></span>     | <span data-ttu-id="4ebcc-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="4ebcc-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4ebcc-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="4ebcc-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="4ebcc-127">Order</span></span> | <span data-ttu-id="4ebcc-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="4ebcc-128">Path</span></span>                          | <span data-ttu-id="4ebcc-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4ebcc-129">Disk Format</span></span> |     |
| <span data-ttu-id="4ebcc-130">1</span><span class="sxs-lookup"><span data-stu-id="4ebcc-130">1</span></span>     | <span data-ttu-id="4ebcc-131">/app1/IFD/Exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="4ebcc-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="4ebcc-132">2</span><span class="sxs-lookup"><span data-stu-id="4ebcc-132">2</span></span>     | <span data-ttu-id="4ebcc-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="4ebcc-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4ebcc-134">Remove Paths</span></span>



| <span data-ttu-id="4ebcc-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="4ebcc-135">Order</span></span> | <span data-ttu-id="4ebcc-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="4ebcc-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="4ebcc-137">1</span><span class="sxs-lookup"><span data-stu-id="4ebcc-137">1</span></span>     | <span data-ttu-id="4ebcc-138">/app1/IFD/Exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="4ebcc-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="4ebcc-139">2</span><span class="sxs-lookup"><span data-stu-id="4ebcc-139">2</span></span>     | <span data-ttu-id="4ebcc-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="4ebcc-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="4ebcc-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4ebcc-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4ebcc-142">Read Paths</span></span>



| <span data-ttu-id="4ebcc-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="4ebcc-143">Order</span></span> | <span data-ttu-id="4ebcc-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="4ebcc-144">Path</span></span>                     | <span data-ttu-id="4ebcc-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4ebcc-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4ebcc-146">1</span><span class="sxs-lookup"><span data-stu-id="4ebcc-146">1</span></span>     | <span data-ttu-id="4ebcc-147">/IFD/Exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="4ebcc-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="4ebcc-148">2</span><span class="sxs-lookup"><span data-stu-id="4ebcc-148">2</span></span>     | <span data-ttu-id="4ebcc-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="4ebcc-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4ebcc-150">Write Paths</span></span>



| <span data-ttu-id="4ebcc-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="4ebcc-151">Order</span></span> | <span data-ttu-id="4ebcc-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="4ebcc-152">Path</span></span>                     | <span data-ttu-id="4ebcc-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4ebcc-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4ebcc-154">1</span><span class="sxs-lookup"><span data-stu-id="4ebcc-154">1</span></span>     | <span data-ttu-id="4ebcc-155">/IFD/Exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="4ebcc-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="4ebcc-156">2</span><span class="sxs-lookup"><span data-stu-id="4ebcc-156">2</span></span>     | <span data-ttu-id="4ebcc-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4ebcc-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4ebcc-158">Remove Paths</span></span>



| <span data-ttu-id="4ebcc-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="4ebcc-159">Order</span></span> | <span data-ttu-id="4ebcc-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="4ebcc-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4ebcc-161">1</span><span class="sxs-lookup"><span data-stu-id="4ebcc-161">1</span></span>     | <span data-ttu-id="4ebcc-162">/IFD/Exif/{ushort = 33437}</span><span class="sxs-lookup"><span data-stu-id="4ebcc-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="4ebcc-163">2</span><span class="sxs-lookup"><span data-stu-id="4ebcc-163">2</span></span>     | <span data-ttu-id="4ebcc-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="4ebcc-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ebcc-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ebcc-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ebcc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ebcc-167">System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="4ebcc-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
