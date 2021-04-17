---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Directiva de metadatos de la foto de System. Photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678221"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="eb531-103">Directiva de metadatos de la foto de System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="eb531-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="eb531-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .</span><span class="sxs-lookup"><span data-stu-id="eb531-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="eb531-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="eb531-105">PKEY</span></span>

<span data-ttu-id="eb531-106">PKEY \_ Photo \_ ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="eb531-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="eb531-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="eb531-107">Containers</span></span>

<span data-ttu-id="eb531-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="eb531-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="eb531-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb531-109">Read-Only</span></span>

<span data-ttu-id="eb531-110">Sí</span><span class="sxs-lookup"><span data-stu-id="eb531-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="eb531-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="eb531-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="eb531-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="eb531-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="eb531-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="eb531-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="eb531-114">Este valor se genera a partir de System. Photo. ShutterSpeedNumerator y System. Photo. ShutterSpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="eb531-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="eb531-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="eb531-115">It cannot be written directly.</span></span> <span data-ttu-id="eb531-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="eb531-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="eb531-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="eb531-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="eb531-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="eb531-118">Read Paths</span></span>



| <span data-ttu-id="eb531-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="eb531-119">Order</span></span> | <span data-ttu-id="eb531-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="eb531-120">Path</span></span>                          | <span data-ttu-id="eb531-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb531-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="eb531-122">1</span><span class="sxs-lookup"><span data-stu-id="eb531-122">1</span></span>     | <span data-ttu-id="eb531-123">/app1/IFD/Exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="eb531-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="eb531-124">2</span><span class="sxs-lookup"><span data-stu-id="eb531-124">2</span></span>     | <span data-ttu-id="eb531-125">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="eb531-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="eb531-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="eb531-126">Write Paths</span></span>



| <span data-ttu-id="eb531-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="eb531-127">Order</span></span> | <span data-ttu-id="eb531-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="eb531-128">Path</span></span>                          | <span data-ttu-id="eb531-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb531-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="eb531-130">1</span><span class="sxs-lookup"><span data-stu-id="eb531-130">1</span></span>     | <span data-ttu-id="eb531-131">/app1/IFD/Exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="eb531-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="eb531-132">2</span><span class="sxs-lookup"><span data-stu-id="eb531-132">2</span></span>     | <span data-ttu-id="eb531-133">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="eb531-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="eb531-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="eb531-134">Remove Paths</span></span>



| <span data-ttu-id="eb531-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="eb531-135">Order</span></span> | <span data-ttu-id="eb531-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="eb531-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="eb531-137">1</span><span class="sxs-lookup"><span data-stu-id="eb531-137">1</span></span>     | <span data-ttu-id="eb531-138">/app1/IFD/Exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="eb531-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="eb531-139">2</span><span class="sxs-lookup"><span data-stu-id="eb531-139">2</span></span>     | <span data-ttu-id="eb531-140">/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="eb531-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="eb531-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="eb531-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="eb531-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="eb531-142">Read Paths</span></span>



| <span data-ttu-id="eb531-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="eb531-143">Order</span></span> | <span data-ttu-id="eb531-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="eb531-144">Path</span></span>                            | <span data-ttu-id="eb531-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb531-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="eb531-146">1</span><span class="sxs-lookup"><span data-stu-id="eb531-146">1</span></span>     | <span data-ttu-id="eb531-147">/IFD/Exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="eb531-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="eb531-148">2</span><span class="sxs-lookup"><span data-stu-id="eb531-148">2</span></span>     | <span data-ttu-id="eb531-149">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="eb531-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="eb531-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="eb531-150">Write Paths</span></span>



| <span data-ttu-id="eb531-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="eb531-151">Order</span></span> | <span data-ttu-id="eb531-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="eb531-152">Path</span></span>                            | <span data-ttu-id="eb531-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb531-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="eb531-154">1</span><span class="sxs-lookup"><span data-stu-id="eb531-154">1</span></span>     | <span data-ttu-id="eb531-155">/IFD/Exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="eb531-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="eb531-156">2</span><span class="sxs-lookup"><span data-stu-id="eb531-156">2</span></span>     | <span data-ttu-id="eb531-157">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="eb531-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="eb531-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="eb531-158">Remove Paths</span></span>



| <span data-ttu-id="eb531-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="eb531-159">Order</span></span> | <span data-ttu-id="eb531-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="eb531-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="eb531-161">1</span><span class="sxs-lookup"><span data-stu-id="eb531-161">1</span></span>     | <span data-ttu-id="eb531-162">/IFD/Exif/{ushort = 37377}</span><span class="sxs-lookup"><span data-stu-id="eb531-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="eb531-163">2</span><span class="sxs-lookup"><span data-stu-id="eb531-163">2</span></span>     | <span data-ttu-id="eb531-164">/ifd/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="eb531-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eb531-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb531-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb531-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb531-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb531-167">System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="eb531-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
