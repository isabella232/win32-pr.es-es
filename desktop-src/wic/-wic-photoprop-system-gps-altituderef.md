---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Directiva de metadatos de la foto System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716895"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="34a40-103">Directiva de metadatos de la foto System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="34a40-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="34a40-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="34a40-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="34a40-105">PKEY</span></span>

<span data-ttu-id="34a40-106">PKEY \_ GPS \_ AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="34a40-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="34a40-107">Description</span></span>

<span data-ttu-id="34a40-108">Indica la altitud utilizada como altitud de referencia.</span><span class="sxs-lookup"><span data-stu-id="34a40-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="34a40-109">Un valor de 0 indica que la altitud está por encima del nivel del mar.</span><span class="sxs-lookup"><span data-stu-id="34a40-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="34a40-110">Un valor de 1 indica una altitud por debajo del nivel del mar.</span><span class="sxs-lookup"><span data-stu-id="34a40-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="34a40-111">Contenedores</span><span class="sxs-lookup"><span data-stu-id="34a40-111">Containers</span></span>

<span data-ttu-id="34a40-112">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="34a40-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="34a40-113">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="34a40-113">Read-Only</span></span>

<span data-ttu-id="34a40-114">No</span><span class="sxs-lookup"><span data-stu-id="34a40-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="34a40-115">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="34a40-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="34a40-116">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="34a40-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="34a40-117">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="34a40-117">Input Type</span></span>

<span data-ttu-id="34a40-118">Bytes.</span><span class="sxs-lookup"><span data-stu-id="34a40-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="34a40-119">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="34a40-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="34a40-120">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="34a40-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="34a40-121">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="34a40-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="34a40-122">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="34a40-122">Read Paths</span></span>



| <span data-ttu-id="34a40-123">Pedido</span><span class="sxs-lookup"><span data-stu-id="34a40-123">Order</span></span> | <span data-ttu-id="34a40-124">Ruta</span><span class="sxs-lookup"><span data-stu-id="34a40-124">Path</span></span>                     | <span data-ttu-id="34a40-125">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34a40-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="34a40-126">1</span><span class="sxs-lookup"><span data-stu-id="34a40-126">1</span></span>     | <span data-ttu-id="34a40-127">/app1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="34a40-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="34a40-128">byte</span><span class="sxs-lookup"><span data-stu-id="34a40-128">byte</span></span>        |
| <span data-ttu-id="34a40-129">2</span><span class="sxs-lookup"><span data-stu-id="34a40-129">2</span></span>     | <span data-ttu-id="34a40-130">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="34a40-131">unicode</span><span class="sxs-lookup"><span data-stu-id="34a40-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="34a40-132">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="34a40-132">Write Paths</span></span>



| <span data-ttu-id="34a40-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="34a40-133">Order</span></span> | <span data-ttu-id="34a40-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="34a40-134">Path</span></span>                     | <span data-ttu-id="34a40-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34a40-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="34a40-136">1</span><span class="sxs-lookup"><span data-stu-id="34a40-136">1</span></span>     | <span data-ttu-id="34a40-137">/app1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="34a40-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="34a40-138">byte</span><span class="sxs-lookup"><span data-stu-id="34a40-138">byte</span></span>        |
| <span data-ttu-id="34a40-139">2</span><span class="sxs-lookup"><span data-stu-id="34a40-139">2</span></span>     | <span data-ttu-id="34a40-140">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="34a40-141">unicode</span><span class="sxs-lookup"><span data-stu-id="34a40-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="34a40-142">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="34a40-142">Remove Paths</span></span>



| <span data-ttu-id="34a40-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="34a40-143">Order</span></span> | <span data-ttu-id="34a40-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="34a40-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="34a40-145">1</span><span class="sxs-lookup"><span data-stu-id="34a40-145">1</span></span>     | <span data-ttu-id="34a40-146">/app1/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="34a40-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="34a40-147">2</span><span class="sxs-lookup"><span data-stu-id="34a40-147">2</span></span>     | <span data-ttu-id="34a40-148">/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="34a40-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="34a40-149">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="34a40-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="34a40-150">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="34a40-150">Read Paths</span></span>



| <span data-ttu-id="34a40-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="34a40-151">Order</span></span> | <span data-ttu-id="34a40-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="34a40-152">Path</span></span>                         | <span data-ttu-id="34a40-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34a40-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="34a40-154">1</span><span class="sxs-lookup"><span data-stu-id="34a40-154">1</span></span>     | <span data-ttu-id="34a40-155">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="34a40-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="34a40-156">byte</span><span class="sxs-lookup"><span data-stu-id="34a40-156">byte</span></span>        |
| <span data-ttu-id="34a40-157">2</span><span class="sxs-lookup"><span data-stu-id="34a40-157">2</span></span>     | <span data-ttu-id="34a40-158">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="34a40-159">unicode</span><span class="sxs-lookup"><span data-stu-id="34a40-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="34a40-160">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="34a40-160">Write Paths</span></span>



| <span data-ttu-id="34a40-161">Pedido</span><span class="sxs-lookup"><span data-stu-id="34a40-161">Order</span></span> | <span data-ttu-id="34a40-162">Ruta</span><span class="sxs-lookup"><span data-stu-id="34a40-162">Path</span></span>                         | <span data-ttu-id="34a40-163">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34a40-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="34a40-164">1</span><span class="sxs-lookup"><span data-stu-id="34a40-164">1</span></span>     | <span data-ttu-id="34a40-165">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="34a40-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="34a40-166">byte</span><span class="sxs-lookup"><span data-stu-id="34a40-166">byte</span></span>        |
| <span data-ttu-id="34a40-167">2</span><span class="sxs-lookup"><span data-stu-id="34a40-167">2</span></span>     | <span data-ttu-id="34a40-168">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="34a40-169">unicode</span><span class="sxs-lookup"><span data-stu-id="34a40-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="34a40-170">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="34a40-170">Remove Paths</span></span>



| <span data-ttu-id="34a40-171">Pedido</span><span class="sxs-lookup"><span data-stu-id="34a40-171">Order</span></span> | <span data-ttu-id="34a40-172">Ruta</span><span class="sxs-lookup"><span data-stu-id="34a40-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="34a40-173">1</span><span class="sxs-lookup"><span data-stu-id="34a40-173">1</span></span>     | <span data-ttu-id="34a40-174">/IFD/GPS/{ushort = 5}</span><span class="sxs-lookup"><span data-stu-id="34a40-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="34a40-175">2</span><span class="sxs-lookup"><span data-stu-id="34a40-175">2</span></span>     | <span data-ttu-id="34a40-176">/ifd/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="34a40-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="34a40-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34a40-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="34a40-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34a40-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34a40-179">System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="34a40-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
