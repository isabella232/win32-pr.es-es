---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Directiva de metadatos de la foto System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678481"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="068b6-103">Directiva de metadatos de la foto System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="068b6-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="068b6-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="068b6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="068b6-105">PKEY</span></span>

<span data-ttu-id="068b6-106">PKEY \_ GPS \_ ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="068b6-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="068b6-107">Containers</span></span>

<span data-ttu-id="068b6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="068b6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="068b6-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="068b6-109">Read-Only</span></span>

<span data-ttu-id="068b6-110">No</span><span class="sxs-lookup"><span data-stu-id="068b6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="068b6-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="068b6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="068b6-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="068b6-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="068b6-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="068b6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="068b6-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="068b6-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="068b6-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="068b6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="068b6-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="068b6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="068b6-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="068b6-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="068b6-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="068b6-118">Read Paths</span></span>



| <span data-ttu-id="068b6-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="068b6-119">Order</span></span> | <span data-ttu-id="068b6-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="068b6-120">Path</span></span>                          | <span data-ttu-id="068b6-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="068b6-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="068b6-122">1</span><span class="sxs-lookup"><span data-stu-id="068b6-122">1</span></span>     | <span data-ttu-id="068b6-123">/app1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="068b6-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="068b6-124">2</span><span class="sxs-lookup"><span data-stu-id="068b6-124">2</span></span>     | <span data-ttu-id="068b6-125">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="068b6-126">unicode</span><span class="sxs-lookup"><span data-stu-id="068b6-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="068b6-127">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="068b6-127">Write Paths</span></span>



| <span data-ttu-id="068b6-128">Pedido</span><span class="sxs-lookup"><span data-stu-id="068b6-128">Order</span></span> | <span data-ttu-id="068b6-129">Ruta</span><span class="sxs-lookup"><span data-stu-id="068b6-129">Path</span></span>                          | <span data-ttu-id="068b6-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="068b6-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="068b6-131">1</span><span class="sxs-lookup"><span data-stu-id="068b6-131">1</span></span>     | <span data-ttu-id="068b6-132">/app1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="068b6-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="068b6-133">2</span><span class="sxs-lookup"><span data-stu-id="068b6-133">2</span></span>     | <span data-ttu-id="068b6-134">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="068b6-135">unicode</span><span class="sxs-lookup"><span data-stu-id="068b6-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="068b6-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="068b6-136">Remove Paths</span></span>



| <span data-ttu-id="068b6-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="068b6-137">Order</span></span> | <span data-ttu-id="068b6-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="068b6-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="068b6-139">1</span><span class="sxs-lookup"><span data-stu-id="068b6-139">1</span></span>     | <span data-ttu-id="068b6-140">/app1/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="068b6-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="068b6-141">2</span><span class="sxs-lookup"><span data-stu-id="068b6-141">2</span></span>     | <span data-ttu-id="068b6-142">/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="068b6-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="068b6-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="068b6-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="068b6-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="068b6-144">Read Paths</span></span>



| <span data-ttu-id="068b6-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="068b6-145">Order</span></span> | <span data-ttu-id="068b6-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="068b6-146">Path</span></span>                              | <span data-ttu-id="068b6-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="068b6-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="068b6-148">1</span><span class="sxs-lookup"><span data-stu-id="068b6-148">1</span></span>     | <span data-ttu-id="068b6-149">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="068b6-150">unicode</span><span class="sxs-lookup"><span data-stu-id="068b6-150">unicode</span></span>     |
| <span data-ttu-id="068b6-151">2</span><span class="sxs-lookup"><span data-stu-id="068b6-151">2</span></span>     | <span data-ttu-id="068b6-152">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="068b6-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="068b6-153">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="068b6-153">Write Paths</span></span>



| <span data-ttu-id="068b6-154">Pedido</span><span class="sxs-lookup"><span data-stu-id="068b6-154">Order</span></span> | <span data-ttu-id="068b6-155">Ruta</span><span class="sxs-lookup"><span data-stu-id="068b6-155">Path</span></span>                              | <span data-ttu-id="068b6-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="068b6-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="068b6-157">1</span><span class="sxs-lookup"><span data-stu-id="068b6-157">1</span></span>     | <span data-ttu-id="068b6-158">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="068b6-159">unicode</span><span class="sxs-lookup"><span data-stu-id="068b6-159">unicode</span></span>     |
| <span data-ttu-id="068b6-160">2</span><span class="sxs-lookup"><span data-stu-id="068b6-160">2</span></span>     | <span data-ttu-id="068b6-161">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="068b6-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="068b6-162">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="068b6-162">Remove Paths</span></span>



| <span data-ttu-id="068b6-163">Pedido</span><span class="sxs-lookup"><span data-stu-id="068b6-163">Order</span></span> | <span data-ttu-id="068b6-164">Ruta</span><span class="sxs-lookup"><span data-stu-id="068b6-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="068b6-165">1</span><span class="sxs-lookup"><span data-stu-id="068b6-165">1</span></span>     | <span data-ttu-id="068b6-166">/ifd/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="068b6-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="068b6-167">2</span><span class="sxs-lookup"><span data-stu-id="068b6-167">2</span></span>     | <span data-ttu-id="068b6-168">/IFD/GPS/{ushort = 27}</span><span class="sxs-lookup"><span data-stu-id="068b6-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="068b6-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="068b6-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="068b6-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="068b6-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="068b6-171">System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="068b6-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
