---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Directiva de metadatos de la foto de System. Photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678226"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a><span data-ttu-id="5c927-103">Directiva de metadatos de la foto de System. Photo. MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-103">System.Photo.MeteringMode Photo Metadata Policy</span></span>

<span data-ttu-id="5c927-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="5c927-104">The photo metadata policy for the [System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5c927-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5c927-105">PKEY</span></span>

<span data-ttu-id="5c927-106">PKEY \_ Photo \_ MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-106">PKEY\_Photo\_MeteringMode</span></span>

### <a name="containers"></a><span data-ttu-id="5c927-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="5c927-107">Containers</span></span>

<span data-ttu-id="5c927-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5c927-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5c927-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c927-109">Read-Only</span></span>

<span data-ttu-id="5c927-110">No</span><span class="sxs-lookup"><span data-stu-id="5c927-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5c927-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="5c927-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5c927-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="5c927-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="5c927-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="5c927-113">Input Type</span></span>

<span data-ttu-id="5c927-114">UShort</span><span class="sxs-lookup"><span data-stu-id="5c927-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5c927-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="5c927-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5c927-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="5c927-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5c927-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="5c927-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5c927-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5c927-118">Read Paths</span></span>



| <span data-ttu-id="5c927-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="5c927-119">Order</span></span> | <span data-ttu-id="5c927-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="5c927-120">Path</span></span>                          | <span data-ttu-id="5c927-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5c927-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5c927-122">1</span><span class="sxs-lookup"><span data-stu-id="5c927-122">1</span></span>     | <span data-ttu-id="5c927-123">/app1/IFD/Exif/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="5c927-123">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="5c927-124">ushort</span><span class="sxs-lookup"><span data-stu-id="5c927-124">ushort</span></span>      |
| <span data-ttu-id="5c927-125">2</span><span class="sxs-lookup"><span data-stu-id="5c927-125">2</span></span>     | <span data-ttu-id="5c927-126">/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-126">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="5c927-127">unicode</span><span class="sxs-lookup"><span data-stu-id="5c927-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5c927-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5c927-128">Write Paths</span></span>



| <span data-ttu-id="5c927-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="5c927-129">Order</span></span> | <span data-ttu-id="5c927-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="5c927-130">Path</span></span>                          | <span data-ttu-id="5c927-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5c927-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5c927-132">1</span><span class="sxs-lookup"><span data-stu-id="5c927-132">1</span></span>     | <span data-ttu-id="5c927-133">/app1/IFD/Exif/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="5c927-133">/app1/ifd/exif/{ushort=37383}</span></span> | <span data-ttu-id="5c927-134">ushort</span><span class="sxs-lookup"><span data-stu-id="5c927-134">ushort</span></span>      |
| <span data-ttu-id="5c927-135">2</span><span class="sxs-lookup"><span data-stu-id="5c927-135">2</span></span>     | <span data-ttu-id="5c927-136">/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-136">/xmp/exif:MeteringMode</span></span>        | <span data-ttu-id="5c927-137">unicode</span><span class="sxs-lookup"><span data-stu-id="5c927-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5c927-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5c927-138">Remove Paths</span></span>



| <span data-ttu-id="5c927-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="5c927-139">Order</span></span> | <span data-ttu-id="5c927-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="5c927-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5c927-141">1</span><span class="sxs-lookup"><span data-stu-id="5c927-141">1</span></span>     | <span data-ttu-id="5c927-142">/app1/IFD/Exif/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="5c927-142">/app1/ifd/exif/{ushort=37383}</span></span> |
| <span data-ttu-id="5c927-143">2</span><span class="sxs-lookup"><span data-stu-id="5c927-143">2</span></span>     | <span data-ttu-id="5c927-144">/xmp/exif:meteringmode</span><span class="sxs-lookup"><span data-stu-id="5c927-144">/xmp/exif:meteringmode</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="5c927-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="5c927-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5c927-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5c927-146">Read Paths</span></span>



| <span data-ttu-id="5c927-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="5c927-147">Order</span></span> | <span data-ttu-id="5c927-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="5c927-148">Path</span></span>                       | <span data-ttu-id="5c927-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5c927-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="5c927-150">1</span><span class="sxs-lookup"><span data-stu-id="5c927-150">1</span></span>     | <span data-ttu-id="5c927-151">/IFD/Exif/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="5c927-151">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="5c927-152">ushort</span><span class="sxs-lookup"><span data-stu-id="5c927-152">ushort</span></span>      |
| <span data-ttu-id="5c927-153">2</span><span class="sxs-lookup"><span data-stu-id="5c927-153">2</span></span>     | <span data-ttu-id="5c927-154">/ifd/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-154">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="5c927-155">unicode</span><span class="sxs-lookup"><span data-stu-id="5c927-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5c927-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5c927-156">Write Paths</span></span>



| <span data-ttu-id="5c927-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="5c927-157">Order</span></span> | <span data-ttu-id="5c927-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="5c927-158">Path</span></span>                       | <span data-ttu-id="5c927-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5c927-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="5c927-160">1</span><span class="sxs-lookup"><span data-stu-id="5c927-160">1</span></span>     | <span data-ttu-id="5c927-161">/IFD/Exif/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="5c927-161">/ifd/exif/{ushort=37383}</span></span>   | <span data-ttu-id="5c927-162">ushort</span><span class="sxs-lookup"><span data-stu-id="5c927-162">ushort</span></span>      |
| <span data-ttu-id="5c927-163">2</span><span class="sxs-lookup"><span data-stu-id="5c927-163">2</span></span>     | <span data-ttu-id="5c927-164">/ifd/xmp/exif:MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-164">/ifd/xmp/exif:MeteringMode</span></span> | <span data-ttu-id="5c927-165">unicode</span><span class="sxs-lookup"><span data-stu-id="5c927-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5c927-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="5c927-166">Remove Paths</span></span>



| <span data-ttu-id="5c927-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="5c927-167">Order</span></span> | <span data-ttu-id="5c927-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="5c927-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="5c927-169">1</span><span class="sxs-lookup"><span data-stu-id="5c927-169">1</span></span>     | <span data-ttu-id="5c927-170">/IFD/Exif/{ushort = 37383}</span><span class="sxs-lookup"><span data-stu-id="5c927-170">/ifd/exif/{ushort=37383}</span></span>   |
| <span data-ttu-id="5c927-171">2</span><span class="sxs-lookup"><span data-stu-id="5c927-171">2</span></span>     | <span data-ttu-id="5c927-172">/ifd/xmp/exif:meteringmode</span><span class="sxs-lookup"><span data-stu-id="5c927-172">/ifd/xmp/exif:meteringmode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5c927-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c927-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c927-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c927-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c927-175">System. Photo. MeteringMode</span><span class="sxs-lookup"><span data-stu-id="5c927-175">System.Photo.MeteringMode</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
