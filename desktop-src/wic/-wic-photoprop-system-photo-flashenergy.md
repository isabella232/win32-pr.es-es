---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Directiva de metadatos de la foto de System. Photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083308"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="88a73-103">Directiva de metadatos de la foto de System. Photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="88a73-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .</span><span class="sxs-lookup"><span data-stu-id="88a73-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="88a73-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="88a73-105">PKEY</span></span>

<span data-ttu-id="88a73-106">PKEY \_ Photo \_ FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="88a73-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="88a73-107">Containers</span></span>

<span data-ttu-id="88a73-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="88a73-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="88a73-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88a73-109">Read-Only</span></span>

<span data-ttu-id="88a73-110">Sí</span><span class="sxs-lookup"><span data-stu-id="88a73-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="88a73-111">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="88a73-111">Input Type</span></span>

<span data-ttu-id="88a73-112">Doble</span><span class="sxs-lookup"><span data-stu-id="88a73-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="88a73-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="88a73-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="88a73-114">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="88a73-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="88a73-115">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="88a73-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="88a73-116">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88a73-116">Read Paths</span></span>



| <span data-ttu-id="88a73-117">Pedido</span><span class="sxs-lookup"><span data-stu-id="88a73-117">Order</span></span> | <span data-ttu-id="88a73-118">Ruta</span><span class="sxs-lookup"><span data-stu-id="88a73-118">Path</span></span>                          | <span data-ttu-id="88a73-119">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88a73-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="88a73-120">1</span><span class="sxs-lookup"><span data-stu-id="88a73-120">1</span></span>     | <span data-ttu-id="88a73-121">/app1/IFD/Exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88a73-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="88a73-122">2</span><span class="sxs-lookup"><span data-stu-id="88a73-122">2</span></span>     | <span data-ttu-id="88a73-123">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="88a73-124">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88a73-124">Write Paths</span></span>



| <span data-ttu-id="88a73-125">Pedido</span><span class="sxs-lookup"><span data-stu-id="88a73-125">Order</span></span> | <span data-ttu-id="88a73-126">Ruta</span><span class="sxs-lookup"><span data-stu-id="88a73-126">Path</span></span>                          | <span data-ttu-id="88a73-127">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88a73-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="88a73-128">1</span><span class="sxs-lookup"><span data-stu-id="88a73-128">1</span></span>     | <span data-ttu-id="88a73-129">/app1/IFD/Exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88a73-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="88a73-130">2</span><span class="sxs-lookup"><span data-stu-id="88a73-130">2</span></span>     | <span data-ttu-id="88a73-131">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="88a73-132">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88a73-132">Remove Paths</span></span>



| <span data-ttu-id="88a73-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="88a73-133">Order</span></span> | <span data-ttu-id="88a73-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="88a73-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="88a73-135">1</span><span class="sxs-lookup"><span data-stu-id="88a73-135">1</span></span>     | <span data-ttu-id="88a73-136">/app1/IFD/Exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88a73-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="88a73-137">2</span><span class="sxs-lookup"><span data-stu-id="88a73-137">2</span></span>     | <span data-ttu-id="88a73-138">/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="88a73-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="88a73-139">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="88a73-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="88a73-140">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88a73-140">Read Paths</span></span>



| <span data-ttu-id="88a73-141">Pedido</span><span class="sxs-lookup"><span data-stu-id="88a73-141">Order</span></span> | <span data-ttu-id="88a73-142">Ruta</span><span class="sxs-lookup"><span data-stu-id="88a73-142">Path</span></span>                      | <span data-ttu-id="88a73-143">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88a73-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="88a73-144">1</span><span class="sxs-lookup"><span data-stu-id="88a73-144">1</span></span>     | <span data-ttu-id="88a73-145">/IFD/Exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88a73-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="88a73-146">2</span><span class="sxs-lookup"><span data-stu-id="88a73-146">2</span></span>     | <span data-ttu-id="88a73-147">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="88a73-148">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88a73-148">Write Paths</span></span>



| <span data-ttu-id="88a73-149">Pedido</span><span class="sxs-lookup"><span data-stu-id="88a73-149">Order</span></span> | <span data-ttu-id="88a73-150">Ruta</span><span class="sxs-lookup"><span data-stu-id="88a73-150">Path</span></span>                      | <span data-ttu-id="88a73-151">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88a73-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="88a73-152">1</span><span class="sxs-lookup"><span data-stu-id="88a73-152">1</span></span>     | <span data-ttu-id="88a73-153">/IFD/Exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88a73-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="88a73-154">2</span><span class="sxs-lookup"><span data-stu-id="88a73-154">2</span></span>     | <span data-ttu-id="88a73-155">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="88a73-156">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="88a73-156">Remove Paths</span></span>



| <span data-ttu-id="88a73-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="88a73-157">Order</span></span> | <span data-ttu-id="88a73-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="88a73-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="88a73-159">1</span><span class="sxs-lookup"><span data-stu-id="88a73-159">1</span></span>     | <span data-ttu-id="88a73-160">/IFD/Exif/{ushort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88a73-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="88a73-161">2</span><span class="sxs-lookup"><span data-stu-id="88a73-161">2</span></span>     | <span data-ttu-id="88a73-162">/ifd/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="88a73-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="88a73-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88a73-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="88a73-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88a73-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88a73-165">System. Photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88a73-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
