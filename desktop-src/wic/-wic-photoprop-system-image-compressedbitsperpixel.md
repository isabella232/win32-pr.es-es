---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Directiva de metadatos de la foto de System. Image. CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706404"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a><span data-ttu-id="17162-103">Directiva de metadatos de la foto de System. Image. CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="17162-103">System.Image.CompressedBitsPerPixel Photo Metadata Policy</span></span>

<span data-ttu-id="17162-104">La Directiva de metadatos de la fotografía para la propiedad [System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) .</span><span class="sxs-lookup"><span data-stu-id="17162-104">The photo metadata policy for the [System.Image.CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="17162-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="17162-105">PKEY</span></span>

<span data-ttu-id="17162-106">PKEY \_ Image \_ CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="17162-106">PKEY\_Image\_CompressedBitsPerPixel</span></span>

### <a name="containers"></a><span data-ttu-id="17162-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="17162-107">Containers</span></span>

<span data-ttu-id="17162-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="17162-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="17162-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="17162-109">Read-Only</span></span>

<span data-ttu-id="17162-110">Sí</span><span class="sxs-lookup"><span data-stu-id="17162-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="17162-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="17162-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="17162-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="17162-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="17162-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="17162-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="17162-114">Este valor se genera a partir de System. Image. CompressedBitsPerPixelNumerator y System. Image. CompressedBitsPerPixelDenominator.</span><span class="sxs-lookup"><span data-stu-id="17162-114">This value is generated from System.Image.CompressedBitsPerPixelNumerator and System.Image.CompressedBitsPerPixelDenominator.</span></span> <span data-ttu-id="17162-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="17162-115">It cannot be written directly.</span></span> <span data-ttu-id="17162-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="17162-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="17162-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="17162-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="17162-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="17162-118">Read Paths</span></span>



| <span data-ttu-id="17162-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="17162-119">Order</span></span> | <span data-ttu-id="17162-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="17162-120">Path</span></span>                             | <span data-ttu-id="17162-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="17162-121">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="17162-122">1</span><span class="sxs-lookup"><span data-stu-id="17162-122">1</span></span>     | <span data-ttu-id="17162-123">/app1/IFD/Exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="17162-123">/app1/ifd/exif/{ushort=37122}</span></span>    |             |
| <span data-ttu-id="17162-124">2</span><span class="sxs-lookup"><span data-stu-id="17162-124">2</span></span>     | <span data-ttu-id="17162-125">/xmp/exif:CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="17162-125">/xmp/exif:CompressedBitsPerPixel</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="17162-126">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="17162-126">Remove Paths</span></span>



| <span data-ttu-id="17162-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="17162-127">Order</span></span> | <span data-ttu-id="17162-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="17162-128">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="17162-129">1</span><span class="sxs-lookup"><span data-stu-id="17162-129">1</span></span>     | <span data-ttu-id="17162-130">/app1/IFD/Exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="17162-130">/app1/ifd/exif/{ushort=37122}</span></span>    |
| <span data-ttu-id="17162-131">2</span><span class="sxs-lookup"><span data-stu-id="17162-131">2</span></span>     | <span data-ttu-id="17162-132">/xmp/exif:compressedbitsperpixel</span><span class="sxs-lookup"><span data-stu-id="17162-132">/xmp/exif:compressedbitsperpixel</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="17162-133">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="17162-133">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="17162-134">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="17162-134">Read Paths</span></span>



| <span data-ttu-id="17162-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="17162-135">Order</span></span> | <span data-ttu-id="17162-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="17162-136">Path</span></span>                                 | <span data-ttu-id="17162-137">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="17162-137">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="17162-138">1</span><span class="sxs-lookup"><span data-stu-id="17162-138">1</span></span>     | <span data-ttu-id="17162-139">/IFD/Exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="17162-139">/ifd/exif/{ushort=37122}</span></span>             |             |
| <span data-ttu-id="17162-140">2</span><span class="sxs-lookup"><span data-stu-id="17162-140">2</span></span>     | <span data-ttu-id="17162-141">/ifd/xmp/exif:CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="17162-141">/ifd/xmp/exif:CompressedBitsPerPixel</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="17162-142">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="17162-142">Remove Paths</span></span>



| <span data-ttu-id="17162-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="17162-143">Order</span></span> | <span data-ttu-id="17162-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="17162-144">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="17162-145">1</span><span class="sxs-lookup"><span data-stu-id="17162-145">1</span></span>     | <span data-ttu-id="17162-146">/IFD/Exif/{ushort = 37122}</span><span class="sxs-lookup"><span data-stu-id="17162-146">/ifd/exif/{ushort=37122}</span></span>             |
| <span data-ttu-id="17162-147">2</span><span class="sxs-lookup"><span data-stu-id="17162-147">2</span></span>     | <span data-ttu-id="17162-148">/ifd/xmp/exif:compressedbitsperpixel</span><span class="sxs-lookup"><span data-stu-id="17162-148">/ifd/xmp/exif:compressedbitsperpixel</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="17162-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17162-149">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="17162-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17162-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17162-151">System. Image. CompressedBitsPerPixel</span><span class="sxs-lookup"><span data-stu-id="17162-151">System.Image.CompressedBitsPerPixel</span></span>](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
