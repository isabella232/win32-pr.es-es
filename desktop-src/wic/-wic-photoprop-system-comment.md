---
description: La Directiva de metadatos de la fotografía para la propiedad System. comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Directiva de metadatos de la foto System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361318"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="ebce3-103">Directiva de metadatos de la foto System. Comment</span><span class="sxs-lookup"><span data-stu-id="ebce3-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="ebce3-104">La Directiva de metadatos de la fotografía para la propiedad [System. Comment](../properties/props-system-comment.md) .</span><span class="sxs-lookup"><span data-stu-id="ebce3-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ebce3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ebce3-105">PKEY</span></span>

<span data-ttu-id="ebce3-106">\_Comentario PKEY</span><span class="sxs-lookup"><span data-stu-id="ebce3-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="ebce3-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="ebce3-107">Containers</span></span>

<span data-ttu-id="ebce3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ebce3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ebce3-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ebce3-109">Read-Only</span></span>

<span data-ttu-id="ebce3-110">No</span><span class="sxs-lookup"><span data-stu-id="ebce3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ebce3-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="ebce3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ebce3-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="ebce3-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="ebce3-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="ebce3-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="ebce3-114">VT \_ LPWStr o VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="ebce3-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ebce3-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="ebce3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ebce3-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="ebce3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="ebce3-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="ebce3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ebce3-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ebce3-118">Read Paths</span></span>



| <span data-ttu-id="ebce3-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="ebce3-119">Order</span></span> | <span data-ttu-id="ebce3-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="ebce3-120">Path</span></span>                                | <span data-ttu-id="ebce3-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ebce3-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="ebce3-122">1</span><span class="sxs-lookup"><span data-stu-id="ebce3-122">1</span></span>     | <span data-ttu-id="ebce3-123">/app1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="ebce3-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="ebce3-124">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-124">unicode\_bytes</span></span> |
| <span data-ttu-id="ebce3-125">2</span><span class="sxs-lookup"><span data-stu-id="ebce3-125">2</span></span>     | <span data-ttu-id="ebce3-126">/app1/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="ebce3-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="ebce3-127">unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-127">unicode</span></span>        |
| <span data-ttu-id="ebce3-128">3</span><span class="sxs-lookup"><span data-stu-id="ebce3-128">3</span></span>     | <span data-ttu-id="ebce3-129">/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="ebce3-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="ebce3-130">unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="ebce3-131">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ebce3-131">Write Paths</span></span>



| <span data-ttu-id="ebce3-132">Pedido</span><span class="sxs-lookup"><span data-stu-id="ebce3-132">Order</span></span> | <span data-ttu-id="ebce3-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="ebce3-133">Path</span></span>                     | <span data-ttu-id="ebce3-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ebce3-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="ebce3-135">1</span><span class="sxs-lookup"><span data-stu-id="ebce3-135">1</span></span>     | <span data-ttu-id="ebce3-136">/app1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="ebce3-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="ebce3-137">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="ebce3-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ebce3-138">Remove Paths</span></span>



| <span data-ttu-id="ebce3-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="ebce3-139">Order</span></span> | <span data-ttu-id="ebce3-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="ebce3-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="ebce3-141">1</span><span class="sxs-lookup"><span data-stu-id="ebce3-141">1</span></span>     | <span data-ttu-id="ebce3-142">/app1/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="ebce3-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="ebce3-143">2</span><span class="sxs-lookup"><span data-stu-id="ebce3-143">2</span></span>     | <span data-ttu-id="ebce3-144">/app1/IFD/Exif/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="ebce3-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="ebce3-145">3</span><span class="sxs-lookup"><span data-stu-id="ebce3-145">3</span></span>     | <span data-ttu-id="ebce3-146">/xmp/exif:UserComment</span><span class="sxs-lookup"><span data-stu-id="ebce3-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="ebce3-147">Directiva TIFF</span><span class="sxs-lookup"><span data-stu-id="ebce3-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="ebce3-148">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ebce3-148">Read Paths</span></span>



| <span data-ttu-id="ebce3-149">Pedido</span><span class="sxs-lookup"><span data-stu-id="ebce3-149">Order</span></span> | <span data-ttu-id="ebce3-150">Ruta</span><span class="sxs-lookup"><span data-stu-id="ebce3-150">Path</span></span>                                    | <span data-ttu-id="ebce3-151">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ebce3-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="ebce3-152">1</span><span class="sxs-lookup"><span data-stu-id="ebce3-152">1</span></span>     | <span data-ttu-id="ebce3-153">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="ebce3-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="ebce3-154">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-154">unicode\_bytes</span></span> |
| <span data-ttu-id="ebce3-155">2</span><span class="sxs-lookup"><span data-stu-id="ebce3-155">2</span></span>     | <span data-ttu-id="ebce3-156">/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="ebce3-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="ebce3-157">unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-157">unicode</span></span>        |
| <span data-ttu-id="ebce3-158">3</span><span class="sxs-lookup"><span data-stu-id="ebce3-158">3</span></span>     | <span data-ttu-id="ebce3-159">/IFD/XMP/ <xmpalt> Exif: UserComment</span><span class="sxs-lookup"><span data-stu-id="ebce3-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="ebce3-160">unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="ebce3-161">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ebce3-161">Write Paths</span></span>



| <span data-ttu-id="ebce3-162">Pedido</span><span class="sxs-lookup"><span data-stu-id="ebce3-162">Order</span></span> | <span data-ttu-id="ebce3-163">Ruta</span><span class="sxs-lookup"><span data-stu-id="ebce3-163">Path</span></span>                | <span data-ttu-id="ebce3-164">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ebce3-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="ebce3-165">1</span><span class="sxs-lookup"><span data-stu-id="ebce3-165">1</span></span>     | <span data-ttu-id="ebce3-166">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="ebce3-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="ebce3-167">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="ebce3-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="ebce3-168">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ebce3-168">Remove Paths</span></span>



| <span data-ttu-id="ebce3-169">Pedido</span><span class="sxs-lookup"><span data-stu-id="ebce3-169">Order</span></span> | <span data-ttu-id="ebce3-170">Ruta</span><span class="sxs-lookup"><span data-stu-id="ebce3-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="ebce3-171">1</span><span class="sxs-lookup"><span data-stu-id="ebce3-171">1</span></span>     | <span data-ttu-id="ebce3-172">/IFD/{ushort = 40092}</span><span class="sxs-lookup"><span data-stu-id="ebce3-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="ebce3-173">2</span><span class="sxs-lookup"><span data-stu-id="ebce3-173">2</span></span>     | <span data-ttu-id="ebce3-174">/IFD/{ushort = 37510}</span><span class="sxs-lookup"><span data-stu-id="ebce3-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="ebce3-175">3</span><span class="sxs-lookup"><span data-stu-id="ebce3-175">3</span></span>     | <span data-ttu-id="ebce3-176">/ifd/xmp/exif:UserComment</span><span class="sxs-lookup"><span data-stu-id="ebce3-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ebce3-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebce3-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebce3-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebce3-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebce3-179">System. Comment</span><span class="sxs-lookup"><span data-stu-id="ebce3-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
