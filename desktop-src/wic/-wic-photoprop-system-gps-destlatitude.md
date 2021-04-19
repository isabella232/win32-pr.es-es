---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Directiva de metadatos de la foto System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688492"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="cbc4d-103">Directiva de metadatos de la foto System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="cbc4d-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc4d-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cbc4d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="cbc4d-105">PKEY</span></span>

<span data-ttu-id="cbc4d-106">PKEY \_ GPS \_ DestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="cbc4d-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="cbc4d-107">Containers</span></span>

<span data-ttu-id="cbc4d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cbc4d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cbc4d-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cbc4d-109">Read-Only</span></span>

<span data-ttu-id="cbc4d-110">Sí</span><span class="sxs-lookup"><span data-stu-id="cbc4d-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cbc4d-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="cbc4d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cbc4d-112">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="cbc4d-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="cbc4d-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="cbc4d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="cbc4d-114">VT \_ Vector \| VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="cbc4d-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cbc4d-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="cbc4d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="cbc4d-116">Este valor se genera a partir de System. GPS. DestLatitudeNumerator y System. GPS. DestLatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="cbc4d-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="cbc4d-117">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="cbc4d-117">It cannot be written directly.</span></span> <span data-ttu-id="cbc4d-118">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="cbc4d-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="cbc4d-119">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="cbc4d-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="cbc4d-120">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="cbc4d-120">Read Paths</span></span>



| <span data-ttu-id="cbc4d-121">Pedido</span><span class="sxs-lookup"><span data-stu-id="cbc4d-121">Order</span></span> | <span data-ttu-id="cbc4d-122">Ruta</span><span class="sxs-lookup"><span data-stu-id="cbc4d-122">Path</span></span>                      | <span data-ttu-id="cbc4d-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cbc4d-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cbc4d-124">1</span><span class="sxs-lookup"><span data-stu-id="cbc4d-124">1</span></span>     | <span data-ttu-id="cbc4d-125">/app1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="cbc4d-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="cbc4d-126">2</span><span class="sxs-lookup"><span data-stu-id="cbc4d-126">2</span></span>     | <span data-ttu-id="cbc4d-127">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="cbc4d-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="cbc4d-128">Write Paths</span></span>



| <span data-ttu-id="cbc4d-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="cbc4d-129">Order</span></span> | <span data-ttu-id="cbc4d-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="cbc4d-130">Path</span></span>                      | <span data-ttu-id="cbc4d-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cbc4d-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cbc4d-132">1</span><span class="sxs-lookup"><span data-stu-id="cbc4d-132">1</span></span>     | <span data-ttu-id="cbc4d-133">/app1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="cbc4d-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="cbc4d-134">2</span><span class="sxs-lookup"><span data-stu-id="cbc4d-134">2</span></span>     | <span data-ttu-id="cbc4d-135">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="cbc4d-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="cbc4d-136">Remove Paths</span></span>



| <span data-ttu-id="cbc4d-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="cbc4d-137">Order</span></span> | <span data-ttu-id="cbc4d-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="cbc4d-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="cbc4d-139">1</span><span class="sxs-lookup"><span data-stu-id="cbc4d-139">1</span></span>     | <span data-ttu-id="cbc4d-140">/app1/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="cbc4d-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="cbc4d-141">2</span><span class="sxs-lookup"><span data-stu-id="cbc4d-141">2</span></span>     | <span data-ttu-id="cbc4d-142">/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="cbc4d-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="cbc4d-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cbc4d-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="cbc4d-144">Read Paths</span></span>



| <span data-ttu-id="cbc4d-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="cbc4d-145">Order</span></span> | <span data-ttu-id="cbc4d-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="cbc4d-146">Path</span></span>                          | <span data-ttu-id="cbc4d-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cbc4d-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cbc4d-148">1</span><span class="sxs-lookup"><span data-stu-id="cbc4d-148">1</span></span>     | <span data-ttu-id="cbc4d-149">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="cbc4d-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="cbc4d-150">2</span><span class="sxs-lookup"><span data-stu-id="cbc4d-150">2</span></span>     | <span data-ttu-id="cbc4d-151">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="cbc4d-152">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="cbc4d-152">Write Paths</span></span>



| <span data-ttu-id="cbc4d-153">Pedido</span><span class="sxs-lookup"><span data-stu-id="cbc4d-153">Order</span></span> | <span data-ttu-id="cbc4d-154">Ruta</span><span class="sxs-lookup"><span data-stu-id="cbc4d-154">Path</span></span>                          | <span data-ttu-id="cbc4d-155">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cbc4d-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cbc4d-156">1</span><span class="sxs-lookup"><span data-stu-id="cbc4d-156">1</span></span>     | <span data-ttu-id="cbc4d-157">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="cbc4d-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="cbc4d-158">2</span><span class="sxs-lookup"><span data-stu-id="cbc4d-158">2</span></span>     | <span data-ttu-id="cbc4d-159">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="cbc4d-160">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="cbc4d-160">Remove Paths</span></span>



| <span data-ttu-id="cbc4d-161">Pedido</span><span class="sxs-lookup"><span data-stu-id="cbc4d-161">Order</span></span> | <span data-ttu-id="cbc4d-162">Ruta</span><span class="sxs-lookup"><span data-stu-id="cbc4d-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="cbc4d-163">1</span><span class="sxs-lookup"><span data-stu-id="cbc4d-163">1</span></span>     | <span data-ttu-id="cbc4d-164">/IFD/GPS/{ushort = 20}</span><span class="sxs-lookup"><span data-stu-id="cbc4d-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="cbc4d-165">2</span><span class="sxs-lookup"><span data-stu-id="cbc4d-165">2</span></span>     | <span data-ttu-id="cbc4d-166">/ifd/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cbc4d-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbc4d-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbc4d-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbc4d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbc4d-169">System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="cbc4d-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
