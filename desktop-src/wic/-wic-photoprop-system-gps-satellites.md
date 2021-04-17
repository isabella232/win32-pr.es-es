---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Directiva de metadatos de fotografía de System. GPS. Satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677969"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="c8e63-103">Directiva de metadatos de fotografía de System. GPS. Satellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="c8e63-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Satellites](../properties/props-system-gps-satellites.md) .</span><span class="sxs-lookup"><span data-stu-id="c8e63-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c8e63-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c8e63-105">PKEY</span></span>

<span data-ttu-id="c8e63-106">\_Satélites GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="c8e63-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="c8e63-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="c8e63-107">Containers</span></span>

<span data-ttu-id="c8e63-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c8e63-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c8e63-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8e63-109">Read-Only</span></span>

<span data-ttu-id="c8e63-110">No</span><span class="sxs-lookup"><span data-stu-id="c8e63-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c8e63-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="c8e63-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c8e63-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="c8e63-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c8e63-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="c8e63-113">Input Type</span></span>

<span data-ttu-id="c8e63-114">String.</span><span class="sxs-lookup"><span data-stu-id="c8e63-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c8e63-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="c8e63-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c8e63-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="c8e63-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="c8e63-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="c8e63-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c8e63-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c8e63-118">Read Paths</span></span>



| <span data-ttu-id="c8e63-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="c8e63-119">Order</span></span> | <span data-ttu-id="c8e63-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="c8e63-120">Path</span></span>                     | <span data-ttu-id="c8e63-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8e63-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c8e63-122">1</span><span class="sxs-lookup"><span data-stu-id="c8e63-122">1</span></span>     | <span data-ttu-id="c8e63-123">/app1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c8e63-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="c8e63-124">ascii</span><span class="sxs-lookup"><span data-stu-id="c8e63-124">ascii</span></span>       |
| <span data-ttu-id="c8e63-125">2</span><span class="sxs-lookup"><span data-stu-id="c8e63-125">2</span></span>     | <span data-ttu-id="c8e63-126">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="c8e63-127">unicode</span><span class="sxs-lookup"><span data-stu-id="c8e63-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c8e63-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c8e63-128">Write Paths</span></span>



| <span data-ttu-id="c8e63-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="c8e63-129">Order</span></span> | <span data-ttu-id="c8e63-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="c8e63-130">Path</span></span>                     | <span data-ttu-id="c8e63-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8e63-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="c8e63-132">1</span><span class="sxs-lookup"><span data-stu-id="c8e63-132">1</span></span>     | <span data-ttu-id="c8e63-133">/app1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c8e63-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="c8e63-134">ascii</span><span class="sxs-lookup"><span data-stu-id="c8e63-134">ascii</span></span>       |
| <span data-ttu-id="c8e63-135">2</span><span class="sxs-lookup"><span data-stu-id="c8e63-135">2</span></span>     | <span data-ttu-id="c8e63-136">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="c8e63-137">unicode</span><span class="sxs-lookup"><span data-stu-id="c8e63-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c8e63-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c8e63-138">Remove Paths</span></span>



| <span data-ttu-id="c8e63-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="c8e63-139">Order</span></span> | <span data-ttu-id="c8e63-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="c8e63-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="c8e63-141">1</span><span class="sxs-lookup"><span data-stu-id="c8e63-141">1</span></span>     | <span data-ttu-id="c8e63-142">/app1/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c8e63-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="c8e63-143">2</span><span class="sxs-lookup"><span data-stu-id="c8e63-143">2</span></span>     | <span data-ttu-id="c8e63-144">/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="c8e63-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="c8e63-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c8e63-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c8e63-146">Read Paths</span></span>



| <span data-ttu-id="c8e63-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="c8e63-147">Order</span></span> | <span data-ttu-id="c8e63-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="c8e63-148">Path</span></span>                        | <span data-ttu-id="c8e63-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8e63-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="c8e63-150">1</span><span class="sxs-lookup"><span data-stu-id="c8e63-150">1</span></span>     | <span data-ttu-id="c8e63-151">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c8e63-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="c8e63-152">ascii</span><span class="sxs-lookup"><span data-stu-id="c8e63-152">ascii</span></span>       |
| <span data-ttu-id="c8e63-153">2</span><span class="sxs-lookup"><span data-stu-id="c8e63-153">2</span></span>     | <span data-ttu-id="c8e63-154">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="c8e63-155">unicode</span><span class="sxs-lookup"><span data-stu-id="c8e63-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c8e63-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c8e63-156">Write Paths</span></span>



| <span data-ttu-id="c8e63-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="c8e63-157">Order</span></span> | <span data-ttu-id="c8e63-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="c8e63-158">Path</span></span>                        | <span data-ttu-id="c8e63-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8e63-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="c8e63-160">1</span><span class="sxs-lookup"><span data-stu-id="c8e63-160">1</span></span>     | <span data-ttu-id="c8e63-161">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c8e63-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="c8e63-162">ascii</span><span class="sxs-lookup"><span data-stu-id="c8e63-162">ascii</span></span>       |
| <span data-ttu-id="c8e63-163">2</span><span class="sxs-lookup"><span data-stu-id="c8e63-163">2</span></span>     | <span data-ttu-id="c8e63-164">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="c8e63-165">unicode</span><span class="sxs-lookup"><span data-stu-id="c8e63-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c8e63-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="c8e63-166">Remove Paths</span></span>



| <span data-ttu-id="c8e63-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="c8e63-167">Order</span></span> | <span data-ttu-id="c8e63-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="c8e63-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="c8e63-169">1</span><span class="sxs-lookup"><span data-stu-id="c8e63-169">1</span></span>     | <span data-ttu-id="c8e63-170">/IFD/GPS/{ushort = 8}</span><span class="sxs-lookup"><span data-stu-id="c8e63-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="c8e63-171">2</span><span class="sxs-lookup"><span data-stu-id="c8e63-171">2</span></span>     | <span data-ttu-id="c8e63-172">/ifd/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="c8e63-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c8e63-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8e63-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8e63-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8e63-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8e63-175">System. GPS. satélites</span><span class="sxs-lookup"><span data-stu-id="c8e63-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
