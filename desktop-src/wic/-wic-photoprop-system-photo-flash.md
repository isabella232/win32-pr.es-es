---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Directiva de metadatos de foto de System. Photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678097"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="07882-103">Directiva de metadatos de foto de System. Photo. Flash</span><span class="sxs-lookup"><span data-stu-id="07882-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="07882-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. Flash](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="07882-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="07882-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="07882-105">PKEY</span></span>

<span data-ttu-id="07882-106">PKEY \_ Photo \_ Flash</span><span class="sxs-lookup"><span data-stu-id="07882-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="07882-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="07882-107">Containers</span></span>

<span data-ttu-id="07882-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="07882-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="07882-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="07882-109">Read-Only</span></span>

<span data-ttu-id="07882-110">No</span><span class="sxs-lookup"><span data-stu-id="07882-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="07882-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="07882-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="07882-112">VT \_ UI1 (si el esquema de origen era XMP) o VT \_ UI2 (si el esquema de origen es EXIF)</span><span class="sxs-lookup"><span data-stu-id="07882-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="07882-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="07882-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="07882-114">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="07882-114">Input Type</span></span>

<span data-ttu-id="07882-115">VT \_ UI1, VTUI2, VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="07882-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="07882-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="07882-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="07882-117">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="07882-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="07882-118">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="07882-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="07882-119">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="07882-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="07882-120">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="07882-120">Read Paths</span></span>



| <span data-ttu-id="07882-121">Pedido</span><span class="sxs-lookup"><span data-stu-id="07882-121">Order</span></span> | <span data-ttu-id="07882-122">Ruta</span><span class="sxs-lookup"><span data-stu-id="07882-122">Path</span></span>                             | <span data-ttu-id="07882-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07882-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="07882-124">1</span><span class="sxs-lookup"><span data-stu-id="07882-124">1</span></span>     | <span data-ttu-id="07882-125">/app1/IFD/Exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="07882-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="07882-126">ushort</span><span class="sxs-lookup"><span data-stu-id="07882-126">ushort</span></span>      |
| <span data-ttu-id="07882-127">2</span><span class="sxs-lookup"><span data-stu-id="07882-127">2</span></span>     | <span data-ttu-id="07882-128">/XMP/ <xmpstruct> Exif: Flash</span><span class="sxs-lookup"><span data-stu-id="07882-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="07882-129">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="07882-129">Write Paths</span></span>



| <span data-ttu-id="07882-130">Pedido</span><span class="sxs-lookup"><span data-stu-id="07882-130">Order</span></span> | <span data-ttu-id="07882-131">Ruta</span><span class="sxs-lookup"><span data-stu-id="07882-131">Path</span></span>                             | <span data-ttu-id="07882-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07882-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="07882-133">1</span><span class="sxs-lookup"><span data-stu-id="07882-133">1</span></span>     | <span data-ttu-id="07882-134">/app1/IFD/Exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="07882-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="07882-135">ushort</span><span class="sxs-lookup"><span data-stu-id="07882-135">ushort</span></span>      |
| <span data-ttu-id="07882-136">2</span><span class="sxs-lookup"><span data-stu-id="07882-136">2</span></span>     | <span data-ttu-id="07882-137">/XMP/ <xmpstruct> Exif: Flash</span><span class="sxs-lookup"><span data-stu-id="07882-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="07882-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="07882-138">Remove Paths</span></span>



| <span data-ttu-id="07882-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="07882-139">Order</span></span> | <span data-ttu-id="07882-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="07882-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="07882-141">1</span><span class="sxs-lookup"><span data-stu-id="07882-141">1</span></span>     | <span data-ttu-id="07882-142">/app1/IFD/Exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="07882-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="07882-143">2</span><span class="sxs-lookup"><span data-stu-id="07882-143">2</span></span>     | <span data-ttu-id="07882-144">/XMP/ <xmpstruct> Exif: Flash</span><span class="sxs-lookup"><span data-stu-id="07882-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="07882-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="07882-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="07882-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="07882-146">Read Paths</span></span>



| <span data-ttu-id="07882-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="07882-147">Order</span></span> | <span data-ttu-id="07882-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="07882-148">Path</span></span>                                 | <span data-ttu-id="07882-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07882-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="07882-150">1</span><span class="sxs-lookup"><span data-stu-id="07882-150">1</span></span>     | <span data-ttu-id="07882-151">/IFD/Exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="07882-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="07882-152">ushort</span><span class="sxs-lookup"><span data-stu-id="07882-152">ushort</span></span>      |
| <span data-ttu-id="07882-153">2</span><span class="sxs-lookup"><span data-stu-id="07882-153">2</span></span>     | <span data-ttu-id="07882-154">/IFD/XMP/ <xmpstruct> Exif: Flash</span><span class="sxs-lookup"><span data-stu-id="07882-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="07882-155">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="07882-155">Write Paths</span></span>



| <span data-ttu-id="07882-156">Pedido</span><span class="sxs-lookup"><span data-stu-id="07882-156">Order</span></span> | <span data-ttu-id="07882-157">Ruta</span><span class="sxs-lookup"><span data-stu-id="07882-157">Path</span></span>                                 | <span data-ttu-id="07882-158">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07882-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="07882-159">1</span><span class="sxs-lookup"><span data-stu-id="07882-159">1</span></span>     | <span data-ttu-id="07882-160">/IFD/Exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="07882-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="07882-161">ushort</span><span class="sxs-lookup"><span data-stu-id="07882-161">ushort</span></span>      |
| <span data-ttu-id="07882-162">2</span><span class="sxs-lookup"><span data-stu-id="07882-162">2</span></span>     | <span data-ttu-id="07882-163">/IFD/XMP/ <xmpstruct> Exif: Flash</span><span class="sxs-lookup"><span data-stu-id="07882-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="07882-164">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="07882-164">Remove Paths</span></span>



| <span data-ttu-id="07882-165">Pedido</span><span class="sxs-lookup"><span data-stu-id="07882-165">Order</span></span> | <span data-ttu-id="07882-166">Ruta</span><span class="sxs-lookup"><span data-stu-id="07882-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="07882-167">1</span><span class="sxs-lookup"><span data-stu-id="07882-167">1</span></span>     | <span data-ttu-id="07882-168">/IFD/Exif/{ushort = 37385}</span><span class="sxs-lookup"><span data-stu-id="07882-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="07882-169">2</span><span class="sxs-lookup"><span data-stu-id="07882-169">2</span></span>     | <span data-ttu-id="07882-170">/IFD/XMP/ <xmpstruct> Exif: Flash</span><span class="sxs-lookup"><span data-stu-id="07882-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="07882-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07882-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="07882-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07882-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07882-173">System. Photo. Flash</span><span class="sxs-lookup"><span data-stu-id="07882-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
