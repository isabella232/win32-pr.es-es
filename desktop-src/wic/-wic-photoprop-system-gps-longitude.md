---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Directiva de metadatos de fotos de System. GPS. longitud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678369"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="9e92f-103">Directiva de metadatos de fotos de System. GPS. longitud</span><span class="sxs-lookup"><span data-stu-id="9e92f-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="9e92f-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. longitude](../properties/props-system-gps-longitude.md) .</span><span class="sxs-lookup"><span data-stu-id="9e92f-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9e92f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9e92f-105">PKEY</span></span>

<span data-ttu-id="9e92f-106">\_Longitud de GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="9e92f-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="9e92f-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="9e92f-107">Containers</span></span>

<span data-ttu-id="9e92f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9e92f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9e92f-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e92f-109">Read-Only</span></span>

<span data-ttu-id="9e92f-110">Sí</span><span class="sxs-lookup"><span data-stu-id="9e92f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9e92f-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="9e92f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9e92f-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="9e92f-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9e92f-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="9e92f-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9e92f-114">Este valor se puede escribir escribiendo en System. GPS. LongitudeNumerator y System. GPS. LongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="9e92f-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="9e92f-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="9e92f-115">It cannot be written directly.</span></span> <span data-ttu-id="9e92f-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="9e92f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9e92f-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="9e92f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9e92f-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9e92f-118">Read Paths</span></span>



| <span data-ttu-id="9e92f-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="9e92f-119">Order</span></span> | <span data-ttu-id="9e92f-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="9e92f-120">Path</span></span>                     | <span data-ttu-id="9e92f-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9e92f-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="9e92f-122">1</span><span class="sxs-lookup"><span data-stu-id="9e92f-122">1</span></span>     | <span data-ttu-id="9e92f-123">/app1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="9e92f-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="9e92f-124">2</span><span class="sxs-lookup"><span data-stu-id="9e92f-124">2</span></span>     | <span data-ttu-id="9e92f-125">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="9e92f-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="9e92f-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9e92f-126">Write Paths</span></span>



| <span data-ttu-id="9e92f-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="9e92f-127">Order</span></span> | <span data-ttu-id="9e92f-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="9e92f-128">Path</span></span>                     | <span data-ttu-id="9e92f-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9e92f-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="9e92f-130">1</span><span class="sxs-lookup"><span data-stu-id="9e92f-130">1</span></span>     | <span data-ttu-id="9e92f-131">/app1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="9e92f-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="9e92f-132">2</span><span class="sxs-lookup"><span data-stu-id="9e92f-132">2</span></span>     | <span data-ttu-id="9e92f-133">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="9e92f-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9e92f-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9e92f-134">Remove Paths</span></span>



| <span data-ttu-id="9e92f-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="9e92f-135">Order</span></span> | <span data-ttu-id="9e92f-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="9e92f-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="9e92f-137">1</span><span class="sxs-lookup"><span data-stu-id="9e92f-137">1</span></span>     | <span data-ttu-id="9e92f-138">/app1/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="9e92f-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="9e92f-139">2</span><span class="sxs-lookup"><span data-stu-id="9e92f-139">2</span></span>     | <span data-ttu-id="9e92f-140">/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="9e92f-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="9e92f-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="9e92f-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9e92f-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9e92f-142">Read Paths</span></span>



| <span data-ttu-id="9e92f-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="9e92f-143">Order</span></span> | <span data-ttu-id="9e92f-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="9e92f-144">Path</span></span>                       | <span data-ttu-id="9e92f-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9e92f-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9e92f-146">1</span><span class="sxs-lookup"><span data-stu-id="9e92f-146">1</span></span>     | <span data-ttu-id="9e92f-147">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="9e92f-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="9e92f-148">2</span><span class="sxs-lookup"><span data-stu-id="9e92f-148">2</span></span>     | <span data-ttu-id="9e92f-149">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="9e92f-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9e92f-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9e92f-150">Write Paths</span></span>



| <span data-ttu-id="9e92f-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="9e92f-151">Order</span></span> | <span data-ttu-id="9e92f-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="9e92f-152">Path</span></span>                       | <span data-ttu-id="9e92f-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9e92f-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9e92f-154">1</span><span class="sxs-lookup"><span data-stu-id="9e92f-154">1</span></span>     | <span data-ttu-id="9e92f-155">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="9e92f-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="9e92f-156">2</span><span class="sxs-lookup"><span data-stu-id="9e92f-156">2</span></span>     | <span data-ttu-id="9e92f-157">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="9e92f-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9e92f-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9e92f-158">Remove Paths</span></span>



| <span data-ttu-id="9e92f-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="9e92f-159">Order</span></span> | <span data-ttu-id="9e92f-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="9e92f-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="9e92f-161">1</span><span class="sxs-lookup"><span data-stu-id="9e92f-161">1</span></span>     | <span data-ttu-id="9e92f-162">/IFD/GPS/{ushort = 4}</span><span class="sxs-lookup"><span data-stu-id="9e92f-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="9e92f-163">2</span><span class="sxs-lookup"><span data-stu-id="9e92f-163">2</span></span>     | <span data-ttu-id="9e92f-164">/ifd/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="9e92f-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9e92f-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e92f-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e92f-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e92f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e92f-167">System. GPS. longitud</span><span class="sxs-lookup"><span data-stu-id="9e92f-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
