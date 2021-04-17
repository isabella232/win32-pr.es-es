---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Directiva de metadatos de la foto System. GPS. Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706880"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="4c6d3-103">Directiva de metadatos de la foto System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="4c6d3-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Latitude](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="4c6d3-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4c6d3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4c6d3-105">PKEY</span></span>

<span data-ttu-id="4c6d3-106">PKEY \_ GPS \_ Latitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="4c6d3-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4c6d3-107">Containers</span></span>

<span data-ttu-id="4c6d3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4c6d3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4c6d3-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c6d3-109">Read-Only</span></span>

<span data-ttu-id="4c6d3-110">Sí</span><span class="sxs-lookup"><span data-stu-id="4c6d3-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4c6d3-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="4c6d3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4c6d3-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="4c6d3-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4c6d3-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="4c6d3-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="4c6d3-114">Este valor se puede escribir escribiendo en System. GPS. LatitudeNumerator y System. GPS. LatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="4c6d3-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="4c6d3-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="4c6d3-115">It cannot be written directly.</span></span> <span data-ttu-id="4c6d3-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="4c6d3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4c6d3-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="4c6d3-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4c6d3-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4c6d3-118">Read Paths</span></span>



| <span data-ttu-id="4c6d3-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="4c6d3-119">Order</span></span> | <span data-ttu-id="4c6d3-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="4c6d3-120">Path</span></span>                     | <span data-ttu-id="4c6d3-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4c6d3-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4c6d3-122">1</span><span class="sxs-lookup"><span data-stu-id="4c6d3-122">1</span></span>     | <span data-ttu-id="4c6d3-123">/app1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="4c6d3-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="4c6d3-124">2</span><span class="sxs-lookup"><span data-stu-id="4c6d3-124">2</span></span>     | <span data-ttu-id="4c6d3-125">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="4c6d3-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4c6d3-126">Write Paths</span></span>



| <span data-ttu-id="4c6d3-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="4c6d3-127">Order</span></span> | <span data-ttu-id="4c6d3-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="4c6d3-128">Path</span></span>                     | <span data-ttu-id="4c6d3-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4c6d3-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4c6d3-130">1</span><span class="sxs-lookup"><span data-stu-id="4c6d3-130">1</span></span>     | <span data-ttu-id="4c6d3-131">/app1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="4c6d3-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="4c6d3-132">2</span><span class="sxs-lookup"><span data-stu-id="4c6d3-132">2</span></span>     | <span data-ttu-id="4c6d3-133">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4c6d3-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4c6d3-134">Remove Paths</span></span>



| <span data-ttu-id="4c6d3-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="4c6d3-135">Order</span></span> | <span data-ttu-id="4c6d3-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="4c6d3-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4c6d3-137">1</span><span class="sxs-lookup"><span data-stu-id="4c6d3-137">1</span></span>     | <span data-ttu-id="4c6d3-138">/app1/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="4c6d3-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="4c6d3-139">2</span><span class="sxs-lookup"><span data-stu-id="4c6d3-139">2</span></span>     | <span data-ttu-id="4c6d3-140">/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="4c6d3-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="4c6d3-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4c6d3-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4c6d3-142">Read Paths</span></span>



| <span data-ttu-id="4c6d3-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="4c6d3-143">Order</span></span> | <span data-ttu-id="4c6d3-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="4c6d3-144">Path</span></span>                      | <span data-ttu-id="4c6d3-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4c6d3-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4c6d3-146">1</span><span class="sxs-lookup"><span data-stu-id="4c6d3-146">1</span></span>     | <span data-ttu-id="4c6d3-147">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="4c6d3-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="4c6d3-148">2</span><span class="sxs-lookup"><span data-stu-id="4c6d3-148">2</span></span>     | <span data-ttu-id="4c6d3-149">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="4c6d3-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4c6d3-150">Write Paths</span></span>



| <span data-ttu-id="4c6d3-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="4c6d3-151">Order</span></span> | <span data-ttu-id="4c6d3-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="4c6d3-152">Path</span></span>                      | <span data-ttu-id="4c6d3-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4c6d3-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4c6d3-154">1</span><span class="sxs-lookup"><span data-stu-id="4c6d3-154">1</span></span>     | <span data-ttu-id="4c6d3-155">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="4c6d3-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="4c6d3-156">2</span><span class="sxs-lookup"><span data-stu-id="4c6d3-156">2</span></span>     | <span data-ttu-id="4c6d3-157">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="4c6d3-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4c6d3-158">Remove Paths</span></span>



| <span data-ttu-id="4c6d3-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="4c6d3-159">Order</span></span> | <span data-ttu-id="4c6d3-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="4c6d3-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="4c6d3-161">1</span><span class="sxs-lookup"><span data-stu-id="4c6d3-161">1</span></span>     | <span data-ttu-id="4c6d3-162">/IFD/GPS/{ushort = 2}</span><span class="sxs-lookup"><span data-stu-id="4c6d3-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="4c6d3-163">2</span><span class="sxs-lookup"><span data-stu-id="4c6d3-163">2</span></span>     | <span data-ttu-id="4c6d3-164">/ifd/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4c6d3-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c6d3-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c6d3-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c6d3-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c6d3-167">System. GPS. Latitude</span><span class="sxs-lookup"><span data-stu-id="4c6d3-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
