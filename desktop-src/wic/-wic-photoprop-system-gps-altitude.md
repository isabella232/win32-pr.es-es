---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. altitud.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Directiva de metadatos de la foto System. GPS. altitud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716896"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="1e1c7-103">Directiva de metadatos de la foto System. GPS. altitud</span><span class="sxs-lookup"><span data-stu-id="1e1c7-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="1e1c7-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. altitud](../properties/props-system-gps-altitude.md) .</span><span class="sxs-lookup"><span data-stu-id="1e1c7-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1e1c7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1e1c7-105">PKEY</span></span>

<span data-ttu-id="1e1c7-106">\_Altitud de GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="1e1c7-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="1e1c7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e1c7-107">Description</span></span>

<span data-ttu-id="1e1c7-108">La altitud se indica como un valor absoluto al que se hace referencia en metros.</span><span class="sxs-lookup"><span data-stu-id="1e1c7-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="1e1c7-109">Contenedores</span><span class="sxs-lookup"><span data-stu-id="1e1c7-109">Containers</span></span>

<span data-ttu-id="1e1c7-110">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1e1c7-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1e1c7-111">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e1c7-111">Read-Only</span></span>

<span data-ttu-id="1e1c7-112">Sí</span><span class="sxs-lookup"><span data-stu-id="1e1c7-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1e1c7-113">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="1e1c7-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1e1c7-114">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1e1c7-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="1e1c7-115">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="1e1c7-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="1e1c7-116">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1e1c7-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1e1c7-117">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="1e1c7-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="1e1c7-118">Este valor se puede escribir escribiendo en System. GPS. altitud. Numerator y System. GPS. altitud. denominador.</span><span class="sxs-lookup"><span data-stu-id="1e1c7-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="1e1c7-119">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="1e1c7-119">It cannot be written directly.</span></span> <span data-ttu-id="1e1c7-120">Las rutas de acceso de escritura de las tablas siguientes indican dónde se puede guardar el valor cuando se genera, no cuando se escribe directamente.</span><span class="sxs-lookup"><span data-stu-id="1e1c7-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="1e1c7-121">Cuando se lee el valor, se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="1e1c7-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1e1c7-122">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="1e1c7-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1e1c7-123">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1e1c7-123">Read Paths</span></span>



| <span data-ttu-id="1e1c7-124">Pedido</span><span class="sxs-lookup"><span data-stu-id="1e1c7-124">Order</span></span> | <span data-ttu-id="1e1c7-125">Ruta</span><span class="sxs-lookup"><span data-stu-id="1e1c7-125">Path</span></span>                     | <span data-ttu-id="1e1c7-126">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1e1c7-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1e1c7-127">1</span><span class="sxs-lookup"><span data-stu-id="1e1c7-127">1</span></span>     | <span data-ttu-id="1e1c7-128">/app1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="1e1c7-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="1e1c7-129">2</span><span class="sxs-lookup"><span data-stu-id="1e1c7-129">2</span></span>     | <span data-ttu-id="1e1c7-130">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="1e1c7-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="1e1c7-131">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1e1c7-131">Write Paths</span></span>



| <span data-ttu-id="1e1c7-132">Pedido</span><span class="sxs-lookup"><span data-stu-id="1e1c7-132">Order</span></span> | <span data-ttu-id="1e1c7-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="1e1c7-133">Path</span></span>                     | <span data-ttu-id="1e1c7-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1e1c7-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="1e1c7-135">1</span><span class="sxs-lookup"><span data-stu-id="1e1c7-135">1</span></span>     | <span data-ttu-id="1e1c7-136">/app1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="1e1c7-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="1e1c7-137">2</span><span class="sxs-lookup"><span data-stu-id="1e1c7-137">2</span></span>     | <span data-ttu-id="1e1c7-138">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="1e1c7-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1e1c7-139">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1e1c7-139">Remove Paths</span></span>



| <span data-ttu-id="1e1c7-140">Pedido</span><span class="sxs-lookup"><span data-stu-id="1e1c7-140">Order</span></span> | <span data-ttu-id="1e1c7-141">Ruta</span><span class="sxs-lookup"><span data-stu-id="1e1c7-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="1e1c7-142">1</span><span class="sxs-lookup"><span data-stu-id="1e1c7-142">1</span></span>     | <span data-ttu-id="1e1c7-143">/app1/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="1e1c7-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="1e1c7-144">2</span><span class="sxs-lookup"><span data-stu-id="1e1c7-144">2</span></span>     | <span data-ttu-id="1e1c7-145">/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="1e1c7-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="1e1c7-146">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="1e1c7-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1e1c7-147">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1e1c7-147">Read Paths</span></span>



| <span data-ttu-id="1e1c7-148">Pedido</span><span class="sxs-lookup"><span data-stu-id="1e1c7-148">Order</span></span> | <span data-ttu-id="1e1c7-149">Ruta</span><span class="sxs-lookup"><span data-stu-id="1e1c7-149">Path</span></span>                      | <span data-ttu-id="1e1c7-150">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1e1c7-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="1e1c7-151">1</span><span class="sxs-lookup"><span data-stu-id="1e1c7-151">1</span></span>     | <span data-ttu-id="1e1c7-152">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="1e1c7-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="1e1c7-153">2</span><span class="sxs-lookup"><span data-stu-id="1e1c7-153">2</span></span>     | <span data-ttu-id="1e1c7-154">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="1e1c7-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="1e1c7-155">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1e1c7-155">Write Paths</span></span>



| <span data-ttu-id="1e1c7-156">Pedido</span><span class="sxs-lookup"><span data-stu-id="1e1c7-156">Order</span></span> | <span data-ttu-id="1e1c7-157">Ruta</span><span class="sxs-lookup"><span data-stu-id="1e1c7-157">Path</span></span>                      | <span data-ttu-id="1e1c7-158">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1e1c7-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="1e1c7-159">1</span><span class="sxs-lookup"><span data-stu-id="1e1c7-159">1</span></span>     | <span data-ttu-id="1e1c7-160">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="1e1c7-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="1e1c7-161">2</span><span class="sxs-lookup"><span data-stu-id="1e1c7-161">2</span></span>     | <span data-ttu-id="1e1c7-162">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="1e1c7-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1e1c7-163">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1e1c7-163">Remove Paths</span></span>



| <span data-ttu-id="1e1c7-164">Pedido</span><span class="sxs-lookup"><span data-stu-id="1e1c7-164">Order</span></span> | <span data-ttu-id="1e1c7-165">Ruta</span><span class="sxs-lookup"><span data-stu-id="1e1c7-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="1e1c7-166">1</span><span class="sxs-lookup"><span data-stu-id="1e1c7-166">1</span></span>     | <span data-ttu-id="1e1c7-167">/IFD/GPS/{ushort = 6}</span><span class="sxs-lookup"><span data-stu-id="1e1c7-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="1e1c7-168">2</span><span class="sxs-lookup"><span data-stu-id="1e1c7-168">2</span></span>     | <span data-ttu-id="1e1c7-169">/ifd/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="1e1c7-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="1e1c7-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e1c7-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e1c7-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e1c7-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e1c7-172">System. GPS. altitud</span><span class="sxs-lookup"><span data-stu-id="1e1c7-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
