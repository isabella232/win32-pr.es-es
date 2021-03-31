---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Directiva de metadatos de la foto de System. Photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361084"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="e2843-103">Directiva de metadatos de la foto de System. Photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="e2843-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="e2843-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="e2843-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e2843-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e2843-105">PKEY</span></span>

<span data-ttu-id="e2843-106">PKEY \_ Photo \_ DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="e2843-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="e2843-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="e2843-107">Containers</span></span>

<span data-ttu-id="e2843-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e2843-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e2843-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2843-109">Read-Only</span></span>

<span data-ttu-id="e2843-110">Sí</span><span class="sxs-lookup"><span data-stu-id="e2843-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e2843-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="e2843-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e2843-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="e2843-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e2843-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="e2843-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="e2843-114">Este valor se genera a partir de System. Photo. DigitalZoomNumerator y System. Photo. DigitalZoomDenominator.</span><span class="sxs-lookup"><span data-stu-id="e2843-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="e2843-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="e2843-115">It cannot be written directly.</span></span> <span data-ttu-id="e2843-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="e2843-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e2843-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="e2843-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e2843-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e2843-118">Read Paths</span></span>



| <span data-ttu-id="e2843-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="e2843-119">Order</span></span> | <span data-ttu-id="e2843-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="e2843-120">Path</span></span>                          | <span data-ttu-id="e2843-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e2843-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e2843-122">1</span><span class="sxs-lookup"><span data-stu-id="e2843-122">1</span></span>     | <span data-ttu-id="e2843-123">/app1/IFD/Exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="e2843-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="e2843-124">2</span><span class="sxs-lookup"><span data-stu-id="e2843-124">2</span></span>     | <span data-ttu-id="e2843-125">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="e2843-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="e2843-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e2843-126">Write Paths</span></span>



| <span data-ttu-id="e2843-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="e2843-127">Order</span></span> | <span data-ttu-id="e2843-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="e2843-128">Path</span></span>                          | <span data-ttu-id="e2843-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e2843-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e2843-130">1</span><span class="sxs-lookup"><span data-stu-id="e2843-130">1</span></span>     | <span data-ttu-id="e2843-131">/app1/IFD/Exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="e2843-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="e2843-132">2</span><span class="sxs-lookup"><span data-stu-id="e2843-132">2</span></span>     | <span data-ttu-id="e2843-133">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="e2843-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e2843-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e2843-134">Remove Paths</span></span>



| <span data-ttu-id="e2843-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="e2843-135">Order</span></span> | <span data-ttu-id="e2843-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="e2843-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="e2843-137">1</span><span class="sxs-lookup"><span data-stu-id="e2843-137">1</span></span>     | <span data-ttu-id="e2843-138">/app1/IFD/Exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="e2843-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="e2843-139">2</span><span class="sxs-lookup"><span data-stu-id="e2843-139">2</span></span>     | <span data-ttu-id="e2843-140">/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="e2843-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="e2843-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="e2843-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e2843-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e2843-142">Read Paths</span></span>



| <span data-ttu-id="e2843-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="e2843-143">Order</span></span> | <span data-ttu-id="e2843-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="e2843-144">Path</span></span>                           | <span data-ttu-id="e2843-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e2843-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="e2843-146">1</span><span class="sxs-lookup"><span data-stu-id="e2843-146">1</span></span>     | <span data-ttu-id="e2843-147">/IFD/Exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="e2843-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="e2843-148">2</span><span class="sxs-lookup"><span data-stu-id="e2843-148">2</span></span>     | <span data-ttu-id="e2843-149">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="e2843-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e2843-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e2843-150">Write Paths</span></span>



| <span data-ttu-id="e2843-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="e2843-151">Order</span></span> | <span data-ttu-id="e2843-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="e2843-152">Path</span></span>                           | <span data-ttu-id="e2843-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e2843-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="e2843-154">1</span><span class="sxs-lookup"><span data-stu-id="e2843-154">1</span></span>     | <span data-ttu-id="e2843-155">/IFD/Exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="e2843-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="e2843-156">2</span><span class="sxs-lookup"><span data-stu-id="e2843-156">2</span></span>     | <span data-ttu-id="e2843-157">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="e2843-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e2843-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e2843-158">Remove Paths</span></span>



| <span data-ttu-id="e2843-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="e2843-159">Order</span></span> | <span data-ttu-id="e2843-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="e2843-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="e2843-161">1</span><span class="sxs-lookup"><span data-stu-id="e2843-161">1</span></span>     | <span data-ttu-id="e2843-162">/IFD/Exif/{ushort = 41988}</span><span class="sxs-lookup"><span data-stu-id="e2843-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="e2843-163">2</span><span class="sxs-lookup"><span data-stu-id="e2843-163">2</span></span>     | <span data-ttu-id="e2843-164">/ifd/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="e2843-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e2843-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2843-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2843-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2843-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2843-167">System. Photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="e2843-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
