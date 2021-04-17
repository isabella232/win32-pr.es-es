---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Directiva de metadatos de la foto de System. Photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706835"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="edabf-103">Directiva de metadatos de la foto de System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="edabf-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="edabf-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. Whitebalance](../properties/props-system-photo-whitebalance.md) .</span><span class="sxs-lookup"><span data-stu-id="edabf-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="edabf-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="edabf-105">PKEY</span></span>

<span data-ttu-id="edabf-106">PKEY \_ Photo \_ Whitebalance</span><span class="sxs-lookup"><span data-stu-id="edabf-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="edabf-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="edabf-107">Containers</span></span>

<span data-ttu-id="edabf-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="edabf-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="edabf-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="edabf-109">Read-Only</span></span>

<span data-ttu-id="edabf-110">No</span><span class="sxs-lookup"><span data-stu-id="edabf-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="edabf-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="edabf-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="edabf-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="edabf-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="edabf-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="edabf-113">Input Type</span></span>

<span data-ttu-id="edabf-114">UShort</span><span class="sxs-lookup"><span data-stu-id="edabf-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="edabf-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="edabf-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="edabf-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="edabf-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="edabf-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="edabf-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="edabf-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="edabf-118">Read Paths</span></span>



| <span data-ttu-id="edabf-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="edabf-119">Order</span></span> | <span data-ttu-id="edabf-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="edabf-120">Path</span></span>                          | <span data-ttu-id="edabf-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="edabf-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="edabf-122">1</span><span class="sxs-lookup"><span data-stu-id="edabf-122">1</span></span>     | <span data-ttu-id="edabf-123">/app1/IFD/Exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="edabf-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="edabf-124">ushort</span><span class="sxs-lookup"><span data-stu-id="edabf-124">ushort</span></span>      |
| <span data-ttu-id="edabf-125">2</span><span class="sxs-lookup"><span data-stu-id="edabf-125">2</span></span>     | <span data-ttu-id="edabf-126">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="edabf-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="edabf-127">unicode</span><span class="sxs-lookup"><span data-stu-id="edabf-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="edabf-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="edabf-128">Write Paths</span></span>



| <span data-ttu-id="edabf-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="edabf-129">Order</span></span> | <span data-ttu-id="edabf-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="edabf-130">Path</span></span>                          | <span data-ttu-id="edabf-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="edabf-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="edabf-132">1</span><span class="sxs-lookup"><span data-stu-id="edabf-132">1</span></span>     | <span data-ttu-id="edabf-133">/app1/IFD/Exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="edabf-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="edabf-134">ushort</span><span class="sxs-lookup"><span data-stu-id="edabf-134">ushort</span></span>      |
| <span data-ttu-id="edabf-135">2</span><span class="sxs-lookup"><span data-stu-id="edabf-135">2</span></span>     | <span data-ttu-id="edabf-136">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="edabf-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="edabf-137">unicode</span><span class="sxs-lookup"><span data-stu-id="edabf-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="edabf-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="edabf-138">Remove Paths</span></span>



| <span data-ttu-id="edabf-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="edabf-139">Order</span></span> | <span data-ttu-id="edabf-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="edabf-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="edabf-141">1</span><span class="sxs-lookup"><span data-stu-id="edabf-141">1</span></span>     | <span data-ttu-id="edabf-142">/app1/IFD/Exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="edabf-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="edabf-143">2</span><span class="sxs-lookup"><span data-stu-id="edabf-143">2</span></span>     | <span data-ttu-id="edabf-144">/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="edabf-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="edabf-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="edabf-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="edabf-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="edabf-146">Read Paths</span></span>



| <span data-ttu-id="edabf-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="edabf-147">Order</span></span> | <span data-ttu-id="edabf-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="edabf-148">Path</span></span>                       | <span data-ttu-id="edabf-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="edabf-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="edabf-150">1</span><span class="sxs-lookup"><span data-stu-id="edabf-150">1</span></span>     | <span data-ttu-id="edabf-151">/IFD/Exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="edabf-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="edabf-152">ushort</span><span class="sxs-lookup"><span data-stu-id="edabf-152">ushort</span></span>      |
| <span data-ttu-id="edabf-153">2</span><span class="sxs-lookup"><span data-stu-id="edabf-153">2</span></span>     | <span data-ttu-id="edabf-154">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="edabf-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="edabf-155">unicode</span><span class="sxs-lookup"><span data-stu-id="edabf-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="edabf-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="edabf-156">Write Paths</span></span>



| <span data-ttu-id="edabf-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="edabf-157">Order</span></span> | <span data-ttu-id="edabf-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="edabf-158">Path</span></span>                       | <span data-ttu-id="edabf-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="edabf-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="edabf-160">1</span><span class="sxs-lookup"><span data-stu-id="edabf-160">1</span></span>     | <span data-ttu-id="edabf-161">/IFD/Exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="edabf-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="edabf-162">ushort</span><span class="sxs-lookup"><span data-stu-id="edabf-162">ushort</span></span>      |
| <span data-ttu-id="edabf-163">2</span><span class="sxs-lookup"><span data-stu-id="edabf-163">2</span></span>     | <span data-ttu-id="edabf-164">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="edabf-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="edabf-165">unicode</span><span class="sxs-lookup"><span data-stu-id="edabf-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="edabf-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="edabf-166">Remove Paths</span></span>



| <span data-ttu-id="edabf-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="edabf-167">Order</span></span> | <span data-ttu-id="edabf-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="edabf-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="edabf-169">1</span><span class="sxs-lookup"><span data-stu-id="edabf-169">1</span></span>     | <span data-ttu-id="edabf-170">/IFD/Exif/{ushort = 41987}</span><span class="sxs-lookup"><span data-stu-id="edabf-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="edabf-171">2</span><span class="sxs-lookup"><span data-stu-id="edabf-171">2</span></span>     | <span data-ttu-id="edabf-172">/ifd/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="edabf-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="edabf-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edabf-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="edabf-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edabf-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edabf-175">System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="edabf-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
