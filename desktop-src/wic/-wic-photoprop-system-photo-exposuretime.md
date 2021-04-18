---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Directiva de metadatos de la foto de System. Photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678098"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="06369-103">Directiva de metadatos de la foto de System. Photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="06369-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="06369-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="06369-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="06369-105">PKEY</span></span>

<span data-ttu-id="06369-106">PKEY \_ Photo \_ ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="06369-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="06369-107">Containers</span></span>

<span data-ttu-id="06369-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="06369-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="06369-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="06369-109">Read-Only</span></span>

<span data-ttu-id="06369-110">Sí</span><span class="sxs-lookup"><span data-stu-id="06369-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="06369-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="06369-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="06369-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="06369-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="06369-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="06369-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="06369-114">Este valor se genera a partir de System. Photo. ExposureTimeNumerator y System. Photo. ExposureTimeDenominator.</span><span class="sxs-lookup"><span data-stu-id="06369-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="06369-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="06369-115">It cannot be written directly.</span></span> <span data-ttu-id="06369-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="06369-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="06369-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="06369-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="06369-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="06369-118">Read Paths</span></span>



| <span data-ttu-id="06369-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="06369-119">Order</span></span> | <span data-ttu-id="06369-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="06369-120">Path</span></span>                          | <span data-ttu-id="06369-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="06369-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="06369-122">1</span><span class="sxs-lookup"><span data-stu-id="06369-122">1</span></span>     | <span data-ttu-id="06369-123">/app1/IFD/Exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06369-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="06369-124">2</span><span class="sxs-lookup"><span data-stu-id="06369-124">2</span></span>     | <span data-ttu-id="06369-125">/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="06369-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="06369-126">Write Paths</span></span>



| <span data-ttu-id="06369-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="06369-127">Order</span></span> | <span data-ttu-id="06369-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="06369-128">Path</span></span>                          | <span data-ttu-id="06369-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="06369-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="06369-130">1</span><span class="sxs-lookup"><span data-stu-id="06369-130">1</span></span>     | <span data-ttu-id="06369-131">/app1/IFD/Exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06369-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="06369-132">2</span><span class="sxs-lookup"><span data-stu-id="06369-132">2</span></span>     | <span data-ttu-id="06369-133">/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="06369-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="06369-134">Remove Paths</span></span>



| <span data-ttu-id="06369-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="06369-135">Order</span></span> | <span data-ttu-id="06369-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="06369-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="06369-137">1</span><span class="sxs-lookup"><span data-stu-id="06369-137">1</span></span>     | <span data-ttu-id="06369-138">/app1/IFD/Exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06369-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="06369-139">2</span><span class="sxs-lookup"><span data-stu-id="06369-139">2</span></span>     | <span data-ttu-id="06369-140">/xmp/exif:exposuretime</span><span class="sxs-lookup"><span data-stu-id="06369-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="06369-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="06369-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="06369-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="06369-142">Read Paths</span></span>



| <span data-ttu-id="06369-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="06369-143">Order</span></span> | <span data-ttu-id="06369-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="06369-144">Path</span></span>                       | <span data-ttu-id="06369-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="06369-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="06369-146">1</span><span class="sxs-lookup"><span data-stu-id="06369-146">1</span></span>     | <span data-ttu-id="06369-147">/IFD/Exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06369-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="06369-148">2</span><span class="sxs-lookup"><span data-stu-id="06369-148">2</span></span>     | <span data-ttu-id="06369-149">/ifd/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="06369-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="06369-150">Write Paths</span></span>



| <span data-ttu-id="06369-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="06369-151">Order</span></span> | <span data-ttu-id="06369-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="06369-152">Path</span></span>                       | <span data-ttu-id="06369-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="06369-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="06369-154">1</span><span class="sxs-lookup"><span data-stu-id="06369-154">1</span></span>     | <span data-ttu-id="06369-155">/IFD/Exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06369-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="06369-156">2</span><span class="sxs-lookup"><span data-stu-id="06369-156">2</span></span>     | <span data-ttu-id="06369-157">/ifd/xmp/exif:ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="06369-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="06369-158">Remove Paths</span></span>



| <span data-ttu-id="06369-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="06369-159">Order</span></span> | <span data-ttu-id="06369-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="06369-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="06369-161">1</span><span class="sxs-lookup"><span data-stu-id="06369-161">1</span></span>     | <span data-ttu-id="06369-162">/IFD/Exif/{ushort = 33434}</span><span class="sxs-lookup"><span data-stu-id="06369-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="06369-163">2</span><span class="sxs-lookup"><span data-stu-id="06369-163">2</span></span>     | <span data-ttu-id="06369-164">/ifd/xmp/exif:exposuretime</span><span class="sxs-lookup"><span data-stu-id="06369-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="06369-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06369-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="06369-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06369-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06369-167">System. Photo. ExposureTime</span><span class="sxs-lookup"><span data-stu-id="06369-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
