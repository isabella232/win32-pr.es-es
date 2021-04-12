---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Directiva de metadatos de la foto System. GPS. DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361316"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="e268f-103">Directiva de metadatos de la foto System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="e268f-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestBearing](../properties/props-system-gps-destbearing.md) .</span><span class="sxs-lookup"><span data-stu-id="e268f-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e268f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e268f-105">PKEY</span></span>

<span data-ttu-id="e268f-106">PKEY \_ GPS \_ DestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="e268f-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="e268f-107">Containers</span></span>

<span data-ttu-id="e268f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e268f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e268f-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e268f-109">Read-Only</span></span>

<span data-ttu-id="e268f-110">Sí</span><span class="sxs-lookup"><span data-stu-id="e268f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e268f-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="e268f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e268f-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="e268f-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e268f-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="e268f-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="e268f-114">Este valor se puede escribir escribiendo en System. GPS. DestBearingNumerator y System. GPS. DestBearingDenominator.</span><span class="sxs-lookup"><span data-stu-id="e268f-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="e268f-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="e268f-115">It cannot be written directly.</span></span> <span data-ttu-id="e268f-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="e268f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e268f-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="e268f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e268f-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e268f-118">Read Paths</span></span>



| <span data-ttu-id="e268f-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="e268f-119">Order</span></span> | <span data-ttu-id="e268f-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="e268f-120">Path</span></span>                      | <span data-ttu-id="e268f-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e268f-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e268f-122">1</span><span class="sxs-lookup"><span data-stu-id="e268f-122">1</span></span>     | <span data-ttu-id="e268f-123">/app1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e268f-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="e268f-124">2</span><span class="sxs-lookup"><span data-stu-id="e268f-124">2</span></span>     | <span data-ttu-id="e268f-125">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="e268f-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e268f-126">Write Paths</span></span>



| <span data-ttu-id="e268f-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="e268f-127">Order</span></span> | <span data-ttu-id="e268f-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="e268f-128">Path</span></span>                      | <span data-ttu-id="e268f-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e268f-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e268f-130">1</span><span class="sxs-lookup"><span data-stu-id="e268f-130">1</span></span>     | <span data-ttu-id="e268f-131">/app1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e268f-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="e268f-132">2</span><span class="sxs-lookup"><span data-stu-id="e268f-132">2</span></span>     | <span data-ttu-id="e268f-133">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e268f-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e268f-134">Remove Paths</span></span>



| <span data-ttu-id="e268f-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="e268f-135">Order</span></span> | <span data-ttu-id="e268f-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="e268f-136">Path</span></span>                      | <span data-ttu-id="e268f-137">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e268f-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="e268f-138">1</span><span class="sxs-lookup"><span data-stu-id="e268f-138">1</span></span>     | <span data-ttu-id="e268f-139">/app1/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e268f-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="e268f-140">2</span><span class="sxs-lookup"><span data-stu-id="e268f-140">2</span></span>     | <span data-ttu-id="e268f-141">/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="e268f-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="e268f-142">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="e268f-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e268f-143">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e268f-143">Read Paths</span></span>



| <span data-ttu-id="e268f-144">Pedido</span><span class="sxs-lookup"><span data-stu-id="e268f-144">Order</span></span> | <span data-ttu-id="e268f-145">Ruta</span><span class="sxs-lookup"><span data-stu-id="e268f-145">Path</span></span>                         | <span data-ttu-id="e268f-146">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e268f-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="e268f-147">1</span><span class="sxs-lookup"><span data-stu-id="e268f-147">1</span></span>     | <span data-ttu-id="e268f-148">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e268f-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="e268f-149">2</span><span class="sxs-lookup"><span data-stu-id="e268f-149">2</span></span>     | <span data-ttu-id="e268f-150">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e268f-151">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e268f-151">Write Paths</span></span>



| <span data-ttu-id="e268f-152">Pedido</span><span class="sxs-lookup"><span data-stu-id="e268f-152">Order</span></span> | <span data-ttu-id="e268f-153">Ruta</span><span class="sxs-lookup"><span data-stu-id="e268f-153">Path</span></span>                         | <span data-ttu-id="e268f-154">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e268f-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="e268f-155">1</span><span class="sxs-lookup"><span data-stu-id="e268f-155">1</span></span>     | <span data-ttu-id="e268f-156">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e268f-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="e268f-157">2</span><span class="sxs-lookup"><span data-stu-id="e268f-157">2</span></span>     | <span data-ttu-id="e268f-158">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e268f-159">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="e268f-159">Remove Paths</span></span>



| <span data-ttu-id="e268f-160">Pedido</span><span class="sxs-lookup"><span data-stu-id="e268f-160">Order</span></span> | <span data-ttu-id="e268f-161">Ruta</span><span class="sxs-lookup"><span data-stu-id="e268f-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="e268f-162">1</span><span class="sxs-lookup"><span data-stu-id="e268f-162">1</span></span>     | <span data-ttu-id="e268f-163">/IFD/GPS/{ushort = 24}</span><span class="sxs-lookup"><span data-stu-id="e268f-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="e268f-164">2</span><span class="sxs-lookup"><span data-stu-id="e268f-164">2</span></span>     | <span data-ttu-id="e268f-165">/ifd/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="e268f-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e268f-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e268f-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e268f-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e268f-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e268f-168">System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="e268f-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
