---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Directiva de metadatos de la foto System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083172"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="c79b9-103">Directiva de metadatos de la foto System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="c79b9-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .</span><span class="sxs-lookup"><span data-stu-id="c79b9-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c79b9-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c79b9-105">PKEY</span></span>

<span data-ttu-id="c79b9-106">PKEY \_ GPS \_ DestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="c79b9-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="c79b9-107">Containers</span></span>

<span data-ttu-id="c79b9-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c79b9-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c79b9-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c79b9-109">Read-Only</span></span>

<span data-ttu-id="c79b9-110">Sí</span><span class="sxs-lookup"><span data-stu-id="c79b9-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c79b9-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="c79b9-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c79b9-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="c79b9-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="c79b9-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="c79b9-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="c79b9-114">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="c79b9-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c79b9-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="c79b9-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c79b9-116">Este valor se genera a partir de System. GPS. DestLongitudeNumerator y System. GPS. DestLongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="c79b9-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="c79b9-117">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="c79b9-117">It cannot be written directly.</span></span> <span data-ttu-id="c79b9-118">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="c79b9-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c79b9-119">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="c79b9-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c79b9-120">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c79b9-120">Read Paths</span></span>



| <span data-ttu-id="c79b9-121">Pedido</span><span class="sxs-lookup"><span data-stu-id="c79b9-121">Order</span></span> | <span data-ttu-id="c79b9-122">Ruta</span><span class="sxs-lookup"><span data-stu-id="c79b9-122">Path</span></span>                       | <span data-ttu-id="c79b9-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c79b9-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c79b9-124">1</span><span class="sxs-lookup"><span data-stu-id="c79b9-124">1</span></span>     | <span data-ttu-id="c79b9-125">/app1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="c79b9-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="c79b9-126">2</span><span class="sxs-lookup"><span data-stu-id="c79b9-126">2</span></span>     | <span data-ttu-id="c79b9-127">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c79b9-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c79b9-128">Write Paths</span></span>



| <span data-ttu-id="c79b9-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="c79b9-129">Order</span></span> | <span data-ttu-id="c79b9-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="c79b9-130">Path</span></span>                       | <span data-ttu-id="c79b9-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c79b9-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="c79b9-132">1</span><span class="sxs-lookup"><span data-stu-id="c79b9-132">1</span></span>     | <span data-ttu-id="c79b9-133">/app1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="c79b9-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="c79b9-134">2</span><span class="sxs-lookup"><span data-stu-id="c79b9-134">2</span></span>     | <span data-ttu-id="c79b9-135">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c79b9-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c79b9-136">Remove Paths</span></span>



| <span data-ttu-id="c79b9-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="c79b9-137">Order</span></span> | <span data-ttu-id="c79b9-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="c79b9-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="c79b9-139">1</span><span class="sxs-lookup"><span data-stu-id="c79b9-139">1</span></span>     | <span data-ttu-id="c79b9-140">/app1/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="c79b9-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="c79b9-141">2</span><span class="sxs-lookup"><span data-stu-id="c79b9-141">2</span></span>     | <span data-ttu-id="c79b9-142">/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="c79b9-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="c79b9-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c79b9-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c79b9-144">Read Paths</span></span>



| <span data-ttu-id="c79b9-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="c79b9-145">Order</span></span> | <span data-ttu-id="c79b9-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="c79b9-146">Path</span></span>                           | <span data-ttu-id="c79b9-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c79b9-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="c79b9-148">1</span><span class="sxs-lookup"><span data-stu-id="c79b9-148">1</span></span>     | <span data-ttu-id="c79b9-149">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="c79b9-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="c79b9-150">2</span><span class="sxs-lookup"><span data-stu-id="c79b9-150">2</span></span>     | <span data-ttu-id="c79b9-151">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c79b9-152">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c79b9-152">Write Paths</span></span>



| <span data-ttu-id="c79b9-153">Pedido</span><span class="sxs-lookup"><span data-stu-id="c79b9-153">Order</span></span> | <span data-ttu-id="c79b9-154">Ruta</span><span class="sxs-lookup"><span data-stu-id="c79b9-154">Path</span></span>                           | <span data-ttu-id="c79b9-155">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c79b9-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="c79b9-156">1</span><span class="sxs-lookup"><span data-stu-id="c79b9-156">1</span></span>     | <span data-ttu-id="c79b9-157">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="c79b9-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="c79b9-158">2</span><span class="sxs-lookup"><span data-stu-id="c79b9-158">2</span></span>     | <span data-ttu-id="c79b9-159">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c79b9-160">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c79b9-160">Remove Paths</span></span>



| <span data-ttu-id="c79b9-161">Pedido</span><span class="sxs-lookup"><span data-stu-id="c79b9-161">Order</span></span> | <span data-ttu-id="c79b9-162">Ruta</span><span class="sxs-lookup"><span data-stu-id="c79b9-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="c79b9-163">1</span><span class="sxs-lookup"><span data-stu-id="c79b9-163">1</span></span>     | <span data-ttu-id="c79b9-164">/IFD/GPS/{ushort = 22}</span><span class="sxs-lookup"><span data-stu-id="c79b9-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="c79b9-165">2</span><span class="sxs-lookup"><span data-stu-id="c79b9-165">2</span></span>     | <span data-ttu-id="c79b9-166">/ifd/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c79b9-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c79b9-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c79b9-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c79b9-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c79b9-169">System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="c79b9-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
