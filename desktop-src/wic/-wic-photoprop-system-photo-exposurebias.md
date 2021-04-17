---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Directiva de metadatos de la foto de System. Photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678100"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a><span data-ttu-id="2110d-103">Directiva de metadatos de la foto de System. Photo. ExposureBias</span><span class="sxs-lookup"><span data-stu-id="2110d-103">System.Photo.ExposureBias Photo Metadata Policy</span></span>

<span data-ttu-id="2110d-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .</span><span class="sxs-lookup"><span data-stu-id="2110d-104">The photo metadata policy for the [System.Photo.ExposureBias](../properties/props-system-photo-exposurebias.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2110d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2110d-105">PKEY</span></span>

<span data-ttu-id="2110d-106">PKEY \_ Photo \_ ExposureBias</span><span class="sxs-lookup"><span data-stu-id="2110d-106">PKEY\_Photo\_ExposureBias</span></span>

### <a name="containers"></a><span data-ttu-id="2110d-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="2110d-107">Containers</span></span>

<span data-ttu-id="2110d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2110d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2110d-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2110d-109">Read-Only</span></span>

<span data-ttu-id="2110d-110">Sí</span><span class="sxs-lookup"><span data-stu-id="2110d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2110d-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="2110d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2110d-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="2110d-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2110d-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="2110d-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="2110d-114">Este valor se genera a partir de System. Photo. ExposureBiasNumerator y System. Photo. ExposureBiasDenominator.</span><span class="sxs-lookup"><span data-stu-id="2110d-114">This value is generated from System.Photo.ExposureBiasNumerator and System.Photo.ExposureBiasDenominator.</span></span> <span data-ttu-id="2110d-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="2110d-115">It cannot be written directly.</span></span> <span data-ttu-id="2110d-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="2110d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2110d-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="2110d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2110d-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2110d-118">Read Paths</span></span>



| <span data-ttu-id="2110d-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="2110d-119">Order</span></span> | <span data-ttu-id="2110d-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="2110d-120">Path</span></span>                          | <span data-ttu-id="2110d-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2110d-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="2110d-122">1</span><span class="sxs-lookup"><span data-stu-id="2110d-122">1</span></span>     | <span data-ttu-id="2110d-123">/app1/IFD/Exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="2110d-123">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="2110d-124">2</span><span class="sxs-lookup"><span data-stu-id="2110d-124">2</span></span>     | <span data-ttu-id="2110d-125">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="2110d-125">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="2110d-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2110d-126">Write Paths</span></span>



| <span data-ttu-id="2110d-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="2110d-127">Order</span></span> | <span data-ttu-id="2110d-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="2110d-128">Path</span></span>                          | <span data-ttu-id="2110d-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2110d-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="2110d-130">1</span><span class="sxs-lookup"><span data-stu-id="2110d-130">1</span></span>     | <span data-ttu-id="2110d-131">/app1/IFD/Exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="2110d-131">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="2110d-132">2</span><span class="sxs-lookup"><span data-stu-id="2110d-132">2</span></span>     | <span data-ttu-id="2110d-133">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="2110d-133">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="2110d-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2110d-134">Remove Paths</span></span>



| <span data-ttu-id="2110d-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="2110d-135">Order</span></span> | <span data-ttu-id="2110d-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="2110d-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="2110d-137">1</span><span class="sxs-lookup"><span data-stu-id="2110d-137">1</span></span>     | <span data-ttu-id="2110d-138">/app1/IFD/Exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="2110d-138">/app1/ifd/exif/{ushort=37380}</span></span> |
| <span data-ttu-id="2110d-139">2</span><span class="sxs-lookup"><span data-stu-id="2110d-139">2</span></span>     | <span data-ttu-id="2110d-140">/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="2110d-140">/xmp/exif:exposurebiasvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="2110d-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="2110d-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2110d-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2110d-142">Read Paths</span></span>



| <span data-ttu-id="2110d-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="2110d-143">Order</span></span> | <span data-ttu-id="2110d-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="2110d-144">Path</span></span>                            | <span data-ttu-id="2110d-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2110d-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="2110d-146">1</span><span class="sxs-lookup"><span data-stu-id="2110d-146">1</span></span>     | <span data-ttu-id="2110d-147">/IFD/Exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="2110d-147">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="2110d-148">2</span><span class="sxs-lookup"><span data-stu-id="2110d-148">2</span></span>     | <span data-ttu-id="2110d-149">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="2110d-149">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="2110d-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2110d-150">Write Paths</span></span>



| <span data-ttu-id="2110d-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="2110d-151">Order</span></span> | <span data-ttu-id="2110d-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="2110d-152">Path</span></span>                            | <span data-ttu-id="2110d-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2110d-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="2110d-154">1</span><span class="sxs-lookup"><span data-stu-id="2110d-154">1</span></span>     | <span data-ttu-id="2110d-155">/IFD/Exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="2110d-155">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="2110d-156">2</span><span class="sxs-lookup"><span data-stu-id="2110d-156">2</span></span>     | <span data-ttu-id="2110d-157">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="2110d-157">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="2110d-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2110d-158">Remove Paths</span></span>



| <span data-ttu-id="2110d-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="2110d-159">Order</span></span> | <span data-ttu-id="2110d-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="2110d-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="2110d-161">1</span><span class="sxs-lookup"><span data-stu-id="2110d-161">1</span></span>     | <span data-ttu-id="2110d-162">/IFD/Exif/{ushort = 37380}</span><span class="sxs-lookup"><span data-stu-id="2110d-162">/ifd/exif/{ushort=37380}</span></span>        |
| <span data-ttu-id="2110d-163">2</span><span class="sxs-lookup"><span data-stu-id="2110d-163">2</span></span>     | <span data-ttu-id="2110d-164">/ifd/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="2110d-164">/ifd/xmp/exif:exposurebiasvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2110d-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2110d-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2110d-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2110d-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2110d-167">System. Photo. ExposureBias</span><span class="sxs-lookup"><span data-stu-id="2110d-167">System.Photo.ExposureBias</span></span>](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
