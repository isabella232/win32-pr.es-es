---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Directiva de metadatos de foto de System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707362"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="4bc25-103">Directiva de metadatos de foto de System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="4bc25-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="4bc25-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Track](../properties/props-system-gps-track.md) .</span><span class="sxs-lookup"><span data-stu-id="4bc25-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4bc25-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4bc25-105">PKEY</span></span>

<span data-ttu-id="4bc25-106">\_Pista GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="4bc25-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="4bc25-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4bc25-107">Containers</span></span>

<span data-ttu-id="4bc25-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4bc25-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4bc25-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bc25-109">Read-Only</span></span>

<span data-ttu-id="4bc25-110">Sí</span><span class="sxs-lookup"><span data-stu-id="4bc25-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4bc25-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="4bc25-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4bc25-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4bc25-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4bc25-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="4bc25-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="4bc25-114">Este valor se genera a partir de System. GPS. TrackNumerator y System. GPS. TrackDenominator.</span><span class="sxs-lookup"><span data-stu-id="4bc25-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="4bc25-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="4bc25-115">It cannot be written directly.</span></span> <span data-ttu-id="4bc25-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="4bc25-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4bc25-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="4bc25-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4bc25-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bc25-118">Read Paths</span></span>



| <span data-ttu-id="4bc25-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bc25-119">Order</span></span> | <span data-ttu-id="4bc25-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bc25-120">Path</span></span>                      | <span data-ttu-id="4bc25-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4bc25-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4bc25-122">1</span><span class="sxs-lookup"><span data-stu-id="4bc25-122">1</span></span>     | <span data-ttu-id="4bc25-123">/app1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="4bc25-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="4bc25-124">2</span><span class="sxs-lookup"><span data-stu-id="4bc25-124">2</span></span>     | <span data-ttu-id="4bc25-125">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="4bc25-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="4bc25-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bc25-126">Write Paths</span></span>



| <span data-ttu-id="4bc25-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bc25-127">Order</span></span> | <span data-ttu-id="4bc25-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bc25-128">Path</span></span>                      | <span data-ttu-id="4bc25-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4bc25-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4bc25-130">1</span><span class="sxs-lookup"><span data-stu-id="4bc25-130">1</span></span>     | <span data-ttu-id="4bc25-131">/app1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="4bc25-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="4bc25-132">2</span><span class="sxs-lookup"><span data-stu-id="4bc25-132">2</span></span>     | <span data-ttu-id="4bc25-133">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="4bc25-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4bc25-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bc25-134">Remove Paths</span></span>



| <span data-ttu-id="4bc25-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bc25-135">Order</span></span> | <span data-ttu-id="4bc25-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bc25-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="4bc25-137">1</span><span class="sxs-lookup"><span data-stu-id="4bc25-137">1</span></span>     | <span data-ttu-id="4bc25-138">/app1/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="4bc25-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="4bc25-139">2</span><span class="sxs-lookup"><span data-stu-id="4bc25-139">2</span></span>     | <span data-ttu-id="4bc25-140">/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="4bc25-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="4bc25-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="4bc25-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4bc25-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bc25-142">Read Paths</span></span>



| <span data-ttu-id="4bc25-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bc25-143">Order</span></span> | <span data-ttu-id="4bc25-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bc25-144">Path</span></span>                   | <span data-ttu-id="4bc25-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4bc25-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="4bc25-146">1</span><span class="sxs-lookup"><span data-stu-id="4bc25-146">1</span></span>     | <span data-ttu-id="4bc25-147">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="4bc25-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="4bc25-148">2</span><span class="sxs-lookup"><span data-stu-id="4bc25-148">2</span></span>     | <span data-ttu-id="4bc25-149">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="4bc25-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4bc25-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bc25-150">Write Paths</span></span>



| <span data-ttu-id="4bc25-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bc25-151">Order</span></span> | <span data-ttu-id="4bc25-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bc25-152">Path</span></span>                   | <span data-ttu-id="4bc25-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4bc25-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="4bc25-154">1</span><span class="sxs-lookup"><span data-stu-id="4bc25-154">1</span></span>     | <span data-ttu-id="4bc25-155">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="4bc25-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="4bc25-156">2</span><span class="sxs-lookup"><span data-stu-id="4bc25-156">2</span></span>     | <span data-ttu-id="4bc25-157">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="4bc25-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4bc25-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bc25-158">Remove Paths</span></span>



| <span data-ttu-id="4bc25-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bc25-159">Order</span></span> | <span data-ttu-id="4bc25-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bc25-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="4bc25-161">1</span><span class="sxs-lookup"><span data-stu-id="4bc25-161">1</span></span>     | <span data-ttu-id="4bc25-162">/IFD/GPS/{ushort = 15}</span><span class="sxs-lookup"><span data-stu-id="4bc25-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="4bc25-163">2</span><span class="sxs-lookup"><span data-stu-id="4bc25-163">2</span></span>     | <span data-ttu-id="4bc25-164">/ifd/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="4bc25-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4bc25-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bc25-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bc25-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bc25-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bc25-167">System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="4bc25-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
