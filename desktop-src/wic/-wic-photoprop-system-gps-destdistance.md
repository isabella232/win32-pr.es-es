---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Directiva de metadatos de la foto System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687874"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="542e7-103">Directiva de metadatos de la foto System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="542e7-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="542e7-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="542e7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="542e7-105">PKEY</span></span>

<span data-ttu-id="542e7-106">PKEY \_ GPS \_ DestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="542e7-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="542e7-107">Containers</span></span>

<span data-ttu-id="542e7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="542e7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="542e7-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="542e7-109">Read-Only</span></span>

<span data-ttu-id="542e7-110">Sí</span><span class="sxs-lookup"><span data-stu-id="542e7-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="542e7-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="542e7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="542e7-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="542e7-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="542e7-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="542e7-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="542e7-114">Este valor se genera a partir de System. GPS. DestDistanceNumerator y System. GPS. DestDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="542e7-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="542e7-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="542e7-115">It cannot be written directly.</span></span> <span data-ttu-id="542e7-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="542e7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="542e7-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="542e7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="542e7-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="542e7-118">Read Paths</span></span>



| <span data-ttu-id="542e7-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="542e7-119">Order</span></span> | <span data-ttu-id="542e7-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="542e7-120">Path</span></span>                      | <span data-ttu-id="542e7-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="542e7-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="542e7-122">1</span><span class="sxs-lookup"><span data-stu-id="542e7-122">1</span></span>     | <span data-ttu-id="542e7-123">/app1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="542e7-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="542e7-124">2</span><span class="sxs-lookup"><span data-stu-id="542e7-124">2</span></span>     | <span data-ttu-id="542e7-125">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="542e7-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="542e7-126">Write Paths</span></span>



| <span data-ttu-id="542e7-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="542e7-127">Order</span></span> | <span data-ttu-id="542e7-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="542e7-128">Path</span></span>                      | <span data-ttu-id="542e7-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="542e7-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="542e7-130">1</span><span class="sxs-lookup"><span data-stu-id="542e7-130">1</span></span>     | <span data-ttu-id="542e7-131">/app1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="542e7-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="542e7-132">2</span><span class="sxs-lookup"><span data-stu-id="542e7-132">2</span></span>     | <span data-ttu-id="542e7-133">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="542e7-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="542e7-134">Remove Paths</span></span>



| <span data-ttu-id="542e7-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="542e7-135">Order</span></span> | <span data-ttu-id="542e7-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="542e7-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="542e7-137">1</span><span class="sxs-lookup"><span data-stu-id="542e7-137">1</span></span>     | <span data-ttu-id="542e7-138">/app1/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="542e7-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="542e7-139">2</span><span class="sxs-lookup"><span data-stu-id="542e7-139">2</span></span>     | <span data-ttu-id="542e7-140">/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="542e7-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="542e7-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="542e7-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="542e7-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="542e7-142">Read Paths</span></span>



| <span data-ttu-id="542e7-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="542e7-143">Order</span></span> | <span data-ttu-id="542e7-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="542e7-144">Path</span></span>                          | <span data-ttu-id="542e7-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="542e7-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="542e7-146">1</span><span class="sxs-lookup"><span data-stu-id="542e7-146">1</span></span>     | <span data-ttu-id="542e7-147">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="542e7-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="542e7-148">2</span><span class="sxs-lookup"><span data-stu-id="542e7-148">2</span></span>     | <span data-ttu-id="542e7-149">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="542e7-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="542e7-150">Write Paths</span></span>



| <span data-ttu-id="542e7-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="542e7-151">Order</span></span> | <span data-ttu-id="542e7-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="542e7-152">Path</span></span>                          | <span data-ttu-id="542e7-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="542e7-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="542e7-154">1</span><span class="sxs-lookup"><span data-stu-id="542e7-154">1</span></span>     | <span data-ttu-id="542e7-155">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="542e7-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="542e7-156">2</span><span class="sxs-lookup"><span data-stu-id="542e7-156">2</span></span>     | <span data-ttu-id="542e7-157">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="542e7-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="542e7-158">Remove Paths</span></span>



| <span data-ttu-id="542e7-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="542e7-159">Order</span></span> | <span data-ttu-id="542e7-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="542e7-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="542e7-161">1</span><span class="sxs-lookup"><span data-stu-id="542e7-161">1</span></span>     | <span data-ttu-id="542e7-162">/IFD/GPS/{ushort = 26}</span><span class="sxs-lookup"><span data-stu-id="542e7-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="542e7-163">2</span><span class="sxs-lookup"><span data-stu-id="542e7-163">2</span></span>     | <span data-ttu-id="542e7-164">/ifd/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="542e7-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="542e7-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="542e7-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="542e7-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="542e7-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="542e7-167">System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="542e7-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
