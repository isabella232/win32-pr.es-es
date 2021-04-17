---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Directiva de metadatos de la foto de System. Photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678224"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a><span data-ttu-id="9fcdb-103">Directiva de metadatos de la foto de System. Photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-103">System.Photo.PhotometricInterpretation Photo Metadata Policy</span></span>

<span data-ttu-id="9fcdb-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) .</span><span class="sxs-lookup"><span data-stu-id="9fcdb-104">The photo metadata policy for the [System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9fcdb-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9fcdb-105">PKEY</span></span>

<span data-ttu-id="9fcdb-106">PKEY \_ Photo \_ PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-106">PKEY\_Photo\_PhotometricInterpretation</span></span>

### <a name="containers"></a><span data-ttu-id="9fcdb-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="9fcdb-107">Containers</span></span>

<span data-ttu-id="9fcdb-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9fcdb-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9fcdb-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fcdb-109">Read-Only</span></span>

<span data-ttu-id="9fcdb-110">Sí</span><span class="sxs-lookup"><span data-stu-id="9fcdb-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9fcdb-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="9fcdb-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9fcdb-112">VT \_ UI2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="9fcdb-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="9fcdb-113">Input Type</span></span>

<span data-ttu-id="9fcdb-114">UShort</span><span class="sxs-lookup"><span data-stu-id="9fcdb-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9fcdb-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="9fcdb-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9fcdb-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="9fcdb-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9fcdb-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="9fcdb-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9fcdb-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9fcdb-118">Read Paths</span></span>



| <span data-ttu-id="9fcdb-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="9fcdb-119">Order</span></span> | <span data-ttu-id="9fcdb-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="9fcdb-120">Path</span></span>                                | <span data-ttu-id="9fcdb-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9fcdb-121">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="9fcdb-122">1</span><span class="sxs-lookup"><span data-stu-id="9fcdb-122">1</span></span>     | <span data-ttu-id="9fcdb-123">/app1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="9fcdb-123">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="9fcdb-124">ushort</span><span class="sxs-lookup"><span data-stu-id="9fcdb-124">ushort</span></span>      |
| <span data-ttu-id="9fcdb-125">2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-125">2</span></span>     | <span data-ttu-id="9fcdb-126">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-126">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="9fcdb-127">unicode</span><span class="sxs-lookup"><span data-stu-id="9fcdb-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9fcdb-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9fcdb-128">Write Paths</span></span>



| <span data-ttu-id="9fcdb-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="9fcdb-129">Order</span></span> | <span data-ttu-id="9fcdb-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="9fcdb-130">Path</span></span>                                | <span data-ttu-id="9fcdb-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9fcdb-131">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="9fcdb-132">1</span><span class="sxs-lookup"><span data-stu-id="9fcdb-132">1</span></span>     | <span data-ttu-id="9fcdb-133">/app1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="9fcdb-133">/app1/ifd/{ushort=262}</span></span>              | <span data-ttu-id="9fcdb-134">ushort</span><span class="sxs-lookup"><span data-stu-id="9fcdb-134">ushort</span></span>      |
| <span data-ttu-id="9fcdb-135">2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-135">2</span></span>     | <span data-ttu-id="9fcdb-136">/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-136">/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="9fcdb-137">unicode</span><span class="sxs-lookup"><span data-stu-id="9fcdb-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9fcdb-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9fcdb-138">Remove Paths</span></span>



| <span data-ttu-id="9fcdb-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="9fcdb-139">Order</span></span> | <span data-ttu-id="9fcdb-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="9fcdb-140">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="9fcdb-141">1</span><span class="sxs-lookup"><span data-stu-id="9fcdb-141">1</span></span>     | <span data-ttu-id="9fcdb-142">/app1/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="9fcdb-142">/app1/ifd/{ushort=262}</span></span>              |
| <span data-ttu-id="9fcdb-143">2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-143">2</span></span>     | <span data-ttu-id="9fcdb-144">/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-144">/xmp/tiff:photometricinterpretation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="9fcdb-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="9fcdb-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9fcdb-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9fcdb-146">Read Paths</span></span>



| <span data-ttu-id="9fcdb-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="9fcdb-147">Order</span></span> | <span data-ttu-id="9fcdb-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="9fcdb-148">Path</span></span>                                    | <span data-ttu-id="9fcdb-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9fcdb-149">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="9fcdb-150">1</span><span class="sxs-lookup"><span data-stu-id="9fcdb-150">1</span></span>     | <span data-ttu-id="9fcdb-151">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="9fcdb-151">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="9fcdb-152">ushort</span><span class="sxs-lookup"><span data-stu-id="9fcdb-152">ushort</span></span>      |
| <span data-ttu-id="9fcdb-153">2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-153">2</span></span>     | <span data-ttu-id="9fcdb-154">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-154">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="9fcdb-155">unicode</span><span class="sxs-lookup"><span data-stu-id="9fcdb-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9fcdb-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9fcdb-156">Write Paths</span></span>



| <span data-ttu-id="9fcdb-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="9fcdb-157">Order</span></span> | <span data-ttu-id="9fcdb-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="9fcdb-158">Path</span></span>                                    | <span data-ttu-id="9fcdb-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9fcdb-159">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="9fcdb-160">1</span><span class="sxs-lookup"><span data-stu-id="9fcdb-160">1</span></span>     | <span data-ttu-id="9fcdb-161">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="9fcdb-161">/ifd/{ushort=262}</span></span>                       | <span data-ttu-id="9fcdb-162">ushort</span><span class="sxs-lookup"><span data-stu-id="9fcdb-162">ushort</span></span>      |
| <span data-ttu-id="9fcdb-163">2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-163">2</span></span>     | <span data-ttu-id="9fcdb-164">/ifd/xmp/tiff:PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-164">/ifd/xmp/tiff:PhotometricInterpretation</span></span> | <span data-ttu-id="9fcdb-165">unicode</span><span class="sxs-lookup"><span data-stu-id="9fcdb-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9fcdb-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9fcdb-166">Remove Paths</span></span>



| <span data-ttu-id="9fcdb-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="9fcdb-167">Order</span></span> | <span data-ttu-id="9fcdb-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="9fcdb-168">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="9fcdb-169">1</span><span class="sxs-lookup"><span data-stu-id="9fcdb-169">1</span></span>     | <span data-ttu-id="9fcdb-170">/IFD/{ushort = 262}</span><span class="sxs-lookup"><span data-stu-id="9fcdb-170">/ifd/{ushort=262}</span></span>                       |
| <span data-ttu-id="9fcdb-171">2</span><span class="sxs-lookup"><span data-stu-id="9fcdb-171">2</span></span>     | <span data-ttu-id="9fcdb-172">/ifd/xmp/tiff:photometricinterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-172">/ifd/xmp/tiff:photometricinterpretation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9fcdb-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fcdb-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fcdb-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fcdb-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fcdb-175">System. Photo. PhotometricInterpretation</span><span class="sxs-lookup"><span data-stu-id="9fcdb-175">System.Photo.PhotometricInterpretation</span></span>](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
