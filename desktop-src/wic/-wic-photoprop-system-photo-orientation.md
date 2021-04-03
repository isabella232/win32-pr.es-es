---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Directiva de metadatos de foto de System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083167"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="a74c4-103">Directiva de metadatos de foto de System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="a74c4-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="a74c4-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a74c4-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a74c4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a74c4-105">PKEY</span></span>

<span data-ttu-id="a74c4-106">PKEY \_ orientación de la foto \_</span><span class="sxs-lookup"><span data-stu-id="a74c4-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="a74c4-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a74c4-107">Containers</span></span>

<span data-ttu-id="a74c4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a74c4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a74c4-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a74c4-109">Read-Only</span></span>

<span data-ttu-id="a74c4-110">No</span><span class="sxs-lookup"><span data-stu-id="a74c4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a74c4-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="a74c4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a74c4-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="a74c4-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="a74c4-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a74c4-113">Input Type</span></span>

<span data-ttu-id="a74c4-114">UShort</span><span class="sxs-lookup"><span data-stu-id="a74c4-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a74c4-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="a74c4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a74c4-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="a74c4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a74c4-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="a74c4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a74c4-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a74c4-118">Read Paths</span></span>



| <span data-ttu-id="a74c4-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="a74c4-119">Order</span></span> | <span data-ttu-id="a74c4-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="a74c4-120">Path</span></span>                   | <span data-ttu-id="a74c4-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a74c4-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="a74c4-122">1</span><span class="sxs-lookup"><span data-stu-id="a74c4-122">1</span></span>     | <span data-ttu-id="a74c4-123">/app1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="a74c4-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="a74c4-124">ushort</span><span class="sxs-lookup"><span data-stu-id="a74c4-124">ushort</span></span>      |
| <span data-ttu-id="a74c4-125">2</span><span class="sxs-lookup"><span data-stu-id="a74c4-125">2</span></span>     | <span data-ttu-id="a74c4-126">/XMP/TIFF: orientación</span><span class="sxs-lookup"><span data-stu-id="a74c4-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="a74c4-127">unicode</span><span class="sxs-lookup"><span data-stu-id="a74c4-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a74c4-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a74c4-128">Write Paths</span></span>



| <span data-ttu-id="a74c4-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="a74c4-129">Order</span></span> | <span data-ttu-id="a74c4-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="a74c4-130">Path</span></span>                   | <span data-ttu-id="a74c4-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a74c4-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="a74c4-132">1</span><span class="sxs-lookup"><span data-stu-id="a74c4-132">1</span></span>     | <span data-ttu-id="a74c4-133">/app1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="a74c4-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="a74c4-134">ushort</span><span class="sxs-lookup"><span data-stu-id="a74c4-134">ushort</span></span>      |
| <span data-ttu-id="a74c4-135">2</span><span class="sxs-lookup"><span data-stu-id="a74c4-135">2</span></span>     | <span data-ttu-id="a74c4-136">/XMP/TIFF: orientación</span><span class="sxs-lookup"><span data-stu-id="a74c4-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="a74c4-137">unicode</span><span class="sxs-lookup"><span data-stu-id="a74c4-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a74c4-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a74c4-138">Remove Paths</span></span>



| <span data-ttu-id="a74c4-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="a74c4-139">Order</span></span> | <span data-ttu-id="a74c4-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="a74c4-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="a74c4-141">1</span><span class="sxs-lookup"><span data-stu-id="a74c4-141">1</span></span>     | <span data-ttu-id="a74c4-142">/app1/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="a74c4-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="a74c4-143">2</span><span class="sxs-lookup"><span data-stu-id="a74c4-143">2</span></span>     | <span data-ttu-id="a74c4-144">/XMP/TIFF: orientación</span><span class="sxs-lookup"><span data-stu-id="a74c4-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="a74c4-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="a74c4-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a74c4-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a74c4-146">Read Paths</span></span>



| <span data-ttu-id="a74c4-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="a74c4-147">Order</span></span> | <span data-ttu-id="a74c4-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="a74c4-148">Path</span></span>                      | <span data-ttu-id="a74c4-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a74c4-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a74c4-150">1</span><span class="sxs-lookup"><span data-stu-id="a74c4-150">1</span></span>     | <span data-ttu-id="a74c4-151">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="a74c4-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="a74c4-152">ushort</span><span class="sxs-lookup"><span data-stu-id="a74c4-152">ushort</span></span>      |
| <span data-ttu-id="a74c4-153">2</span><span class="sxs-lookup"><span data-stu-id="a74c4-153">2</span></span>     | <span data-ttu-id="a74c4-154">/IFD/XMP/TIFF: orientación</span><span class="sxs-lookup"><span data-stu-id="a74c4-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="a74c4-155">unicode</span><span class="sxs-lookup"><span data-stu-id="a74c4-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a74c4-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a74c4-156">Write Paths</span></span>



| <span data-ttu-id="a74c4-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="a74c4-157">Order</span></span> | <span data-ttu-id="a74c4-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="a74c4-158">Path</span></span>                      | <span data-ttu-id="a74c4-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a74c4-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a74c4-160">1</span><span class="sxs-lookup"><span data-stu-id="a74c4-160">1</span></span>     | <span data-ttu-id="a74c4-161">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="a74c4-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="a74c4-162">ushort</span><span class="sxs-lookup"><span data-stu-id="a74c4-162">ushort</span></span>      |
| <span data-ttu-id="a74c4-163">2</span><span class="sxs-lookup"><span data-stu-id="a74c4-163">2</span></span>     | <span data-ttu-id="a74c4-164">/IFD/XMP/TIFF: orientación</span><span class="sxs-lookup"><span data-stu-id="a74c4-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="a74c4-165">unicode</span><span class="sxs-lookup"><span data-stu-id="a74c4-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a74c4-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a74c4-166">Remove Paths</span></span>



| <span data-ttu-id="a74c4-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="a74c4-167">Order</span></span> | <span data-ttu-id="a74c4-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="a74c4-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a74c4-169">1</span><span class="sxs-lookup"><span data-stu-id="a74c4-169">1</span></span>     | <span data-ttu-id="a74c4-170">/IFD/{ushort = 274}</span><span class="sxs-lookup"><span data-stu-id="a74c4-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="a74c4-171">2</span><span class="sxs-lookup"><span data-stu-id="a74c4-171">2</span></span>     | <span data-ttu-id="a74c4-172">/IFD/XMP/TIFF: orientación</span><span class="sxs-lookup"><span data-stu-id="a74c4-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a74c4-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a74c4-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a74c4-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a74c4-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a74c4-175">System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="a74c4-175">System.Photo.Orientation</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
