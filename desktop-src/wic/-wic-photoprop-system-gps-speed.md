---
description: La Directiva de metadatos de fotos para la propiedad System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Directiva de metadatos de foto de System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697493"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="1acc0-103">Directiva de metadatos de foto de System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="1acc0-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="1acc0-104">La Directiva de metadatos de fotos para la propiedad [System. GPS. Speed](../properties/props-system-gps-speed.md) .</span><span class="sxs-lookup"><span data-stu-id="1acc0-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1acc0-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1acc0-105">PKEY</span></span>

<span data-ttu-id="1acc0-106">\_Velocidad de GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="1acc0-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="1acc0-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="1acc0-107">Containers</span></span>

<span data-ttu-id="1acc0-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1acc0-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1acc0-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1acc0-109">Read-Only</span></span>

<span data-ttu-id="1acc0-110">Sí</span><span class="sxs-lookup"><span data-stu-id="1acc0-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1acc0-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="1acc0-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1acc0-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1acc0-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1acc0-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="1acc0-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="1acc0-114">Este valor se genera a partir de System. GPS. SpeedNumerator y System. GPS. SpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="1acc0-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="1acc0-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="1acc0-115">It cannot be written directly.</span></span> <span data-ttu-id="1acc0-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="1acc0-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1acc0-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="1acc0-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1acc0-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1acc0-118">Read Paths</span></span>



| <span data-ttu-id="1acc0-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="1acc0-119">Order</span></span> | <span data-ttu-id="1acc0-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="1acc0-120">Path</span></span>                      | <span data-ttu-id="1acc0-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1acc0-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="1acc0-122">1</span><span class="sxs-lookup"><span data-stu-id="1acc0-122">1</span></span>     | <span data-ttu-id="1acc0-123">/app1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="1acc0-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="1acc0-124">2</span><span class="sxs-lookup"><span data-stu-id="1acc0-124">2</span></span>     | <span data-ttu-id="1acc0-125">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="1acc0-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="1acc0-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1acc0-126">Write Paths</span></span>



| <span data-ttu-id="1acc0-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="1acc0-127">Order</span></span> | <span data-ttu-id="1acc0-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="1acc0-128">Path</span></span>                      | <span data-ttu-id="1acc0-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1acc0-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="1acc0-130">1</span><span class="sxs-lookup"><span data-stu-id="1acc0-130">1</span></span>     | <span data-ttu-id="1acc0-131">/app1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="1acc0-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="1acc0-132">2</span><span class="sxs-lookup"><span data-stu-id="1acc0-132">2</span></span>     | <span data-ttu-id="1acc0-133">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="1acc0-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1acc0-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1acc0-134">Remove Paths</span></span>



| <span data-ttu-id="1acc0-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="1acc0-135">Order</span></span> | <span data-ttu-id="1acc0-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="1acc0-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="1acc0-137">1</span><span class="sxs-lookup"><span data-stu-id="1acc0-137">1</span></span>     | <span data-ttu-id="1acc0-138">/app1/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="1acc0-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="1acc0-139">2</span><span class="sxs-lookup"><span data-stu-id="1acc0-139">2</span></span>     | <span data-ttu-id="1acc0-140">/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="1acc0-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="1acc0-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="1acc0-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1acc0-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1acc0-142">Read Paths</span></span>



| <span data-ttu-id="1acc0-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="1acc0-143">Order</span></span> | <span data-ttu-id="1acc0-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="1acc0-144">Path</span></span>                   | <span data-ttu-id="1acc0-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1acc0-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="1acc0-146">1</span><span class="sxs-lookup"><span data-stu-id="1acc0-146">1</span></span>     | <span data-ttu-id="1acc0-147">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="1acc0-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="1acc0-148">2</span><span class="sxs-lookup"><span data-stu-id="1acc0-148">2</span></span>     | <span data-ttu-id="1acc0-149">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="1acc0-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="1acc0-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1acc0-150">Write Paths</span></span>



| <span data-ttu-id="1acc0-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="1acc0-151">Order</span></span> | <span data-ttu-id="1acc0-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="1acc0-152">Path</span></span>                   | <span data-ttu-id="1acc0-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1acc0-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="1acc0-154">1</span><span class="sxs-lookup"><span data-stu-id="1acc0-154">1</span></span>     | <span data-ttu-id="1acc0-155">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="1acc0-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="1acc0-156">2</span><span class="sxs-lookup"><span data-stu-id="1acc0-156">2</span></span>     | <span data-ttu-id="1acc0-157">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="1acc0-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="1acc0-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="1acc0-158">Remove Paths</span></span>



| <span data-ttu-id="1acc0-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="1acc0-159">Order</span></span> | <span data-ttu-id="1acc0-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="1acc0-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="1acc0-161">1</span><span class="sxs-lookup"><span data-stu-id="1acc0-161">1</span></span>     | <span data-ttu-id="1acc0-162">/IFD/GPS/{ushort = 13}</span><span class="sxs-lookup"><span data-stu-id="1acc0-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="1acc0-163">2</span><span class="sxs-lookup"><span data-stu-id="1acc0-163">2</span></span>     | <span data-ttu-id="1acc0-164">/ifd/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="1acc0-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1acc0-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1acc0-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1acc0-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1acc0-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1acc0-167">System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="1acc0-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
