---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Directiva de metadatos de foto de System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687664"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="599e1-103">Directiva de metadatos de foto de System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="599e1-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="599e1-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. status](../properties/props-system-gps-status.md) .</span><span class="sxs-lookup"><span data-stu-id="599e1-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="599e1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="599e1-105">PKEY</span></span>

<span data-ttu-id="599e1-106">\_Estado de GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="599e1-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="599e1-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="599e1-107">Containers</span></span>

<span data-ttu-id="599e1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="599e1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="599e1-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="599e1-109">Read-Only</span></span>

<span data-ttu-id="599e1-110">No</span><span class="sxs-lookup"><span data-stu-id="599e1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="599e1-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="599e1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="599e1-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="599e1-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="599e1-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="599e1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="599e1-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="599e1-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="599e1-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="599e1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="599e1-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="599e1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="599e1-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="599e1-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="599e1-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="599e1-118">Read Paths</span></span>



| <span data-ttu-id="599e1-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="599e1-119">Order</span></span> | <span data-ttu-id="599e1-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="599e1-120">Path</span></span>                     | <span data-ttu-id="599e1-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="599e1-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="599e1-122">1</span><span class="sxs-lookup"><span data-stu-id="599e1-122">1</span></span>     | <span data-ttu-id="599e1-123">/app1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="599e1-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="599e1-124">ascii</span><span class="sxs-lookup"><span data-stu-id="599e1-124">ascii</span></span>       |
| <span data-ttu-id="599e1-125">2</span><span class="sxs-lookup"><span data-stu-id="599e1-125">2</span></span>     | <span data-ttu-id="599e1-126">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="599e1-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="599e1-127">unicode</span><span class="sxs-lookup"><span data-stu-id="599e1-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="599e1-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="599e1-128">Write Paths</span></span>



| <span data-ttu-id="599e1-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="599e1-129">Order</span></span> | <span data-ttu-id="599e1-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="599e1-130">Path</span></span>                     | <span data-ttu-id="599e1-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="599e1-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="599e1-132">1</span><span class="sxs-lookup"><span data-stu-id="599e1-132">1</span></span>     | <span data-ttu-id="599e1-133">/app1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="599e1-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="599e1-134">ascii</span><span class="sxs-lookup"><span data-stu-id="599e1-134">ascii</span></span>       |
| <span data-ttu-id="599e1-135">2</span><span class="sxs-lookup"><span data-stu-id="599e1-135">2</span></span>     | <span data-ttu-id="599e1-136">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="599e1-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="599e1-137">unicode</span><span class="sxs-lookup"><span data-stu-id="599e1-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="599e1-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="599e1-138">Remove Paths</span></span>



| <span data-ttu-id="599e1-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="599e1-139">Order</span></span> | <span data-ttu-id="599e1-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="599e1-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="599e1-141">1</span><span class="sxs-lookup"><span data-stu-id="599e1-141">1</span></span>     | <span data-ttu-id="599e1-142">/app1/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="599e1-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="599e1-143">2</span><span class="sxs-lookup"><span data-stu-id="599e1-143">2</span></span>     | <span data-ttu-id="599e1-144">/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="599e1-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="599e1-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="599e1-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="599e1-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="599e1-146">Read Paths</span></span>



| <span data-ttu-id="599e1-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="599e1-147">Order</span></span> | <span data-ttu-id="599e1-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="599e1-148">Path</span></span>                    | <span data-ttu-id="599e1-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="599e1-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="599e1-150">1</span><span class="sxs-lookup"><span data-stu-id="599e1-150">1</span></span>     | <span data-ttu-id="599e1-151">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="599e1-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="599e1-152">ascii</span><span class="sxs-lookup"><span data-stu-id="599e1-152">ascii</span></span>       |
| <span data-ttu-id="599e1-153">2</span><span class="sxs-lookup"><span data-stu-id="599e1-153">2</span></span>     | <span data-ttu-id="599e1-154">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="599e1-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="599e1-155">unicode</span><span class="sxs-lookup"><span data-stu-id="599e1-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="599e1-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="599e1-156">Write Paths</span></span>



| <span data-ttu-id="599e1-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="599e1-157">Order</span></span> | <span data-ttu-id="599e1-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="599e1-158">Path</span></span>                    | <span data-ttu-id="599e1-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="599e1-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="599e1-160">1</span><span class="sxs-lookup"><span data-stu-id="599e1-160">1</span></span>     | <span data-ttu-id="599e1-161">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="599e1-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="599e1-162">ascii</span><span class="sxs-lookup"><span data-stu-id="599e1-162">ascii</span></span>       |
| <span data-ttu-id="599e1-163">2</span><span class="sxs-lookup"><span data-stu-id="599e1-163">2</span></span>     | <span data-ttu-id="599e1-164">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="599e1-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="599e1-165">unicode</span><span class="sxs-lookup"><span data-stu-id="599e1-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="599e1-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="599e1-166">Remove Paths</span></span>



| <span data-ttu-id="599e1-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="599e1-167">Order</span></span> | <span data-ttu-id="599e1-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="599e1-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="599e1-169">1</span><span class="sxs-lookup"><span data-stu-id="599e1-169">1</span></span>     | <span data-ttu-id="599e1-170">/IFD/GPS/{ushort = 9}</span><span class="sxs-lookup"><span data-stu-id="599e1-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="599e1-171">2</span><span class="sxs-lookup"><span data-stu-id="599e1-171">2</span></span>     | <span data-ttu-id="599e1-172">/ifd/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="599e1-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="599e1-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="599e1-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="599e1-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="599e1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="599e1-175">System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="599e1-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
