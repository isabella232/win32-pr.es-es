---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Directiva de metadatos de la foto System. GPS. MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002097"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="2c357-103">Directiva de metadatos de la foto System. GPS. MeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="2c357-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. MeasureMode](../properties/props-system-gps-measuremode.md) .</span><span class="sxs-lookup"><span data-stu-id="2c357-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2c357-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2c357-105">PKEY</span></span>

<span data-ttu-id="2c357-106">PKEY \_ GPS \_ MeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="2c357-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="2c357-107">Containers</span></span>

<span data-ttu-id="2c357-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2c357-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2c357-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c357-109">Read-Only</span></span>

<span data-ttu-id="2c357-110">No</span><span class="sxs-lookup"><span data-stu-id="2c357-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2c357-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="2c357-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2c357-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="2c357-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="2c357-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="2c357-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="2c357-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="2c357-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2c357-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="2c357-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="2c357-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="2c357-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="2c357-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="2c357-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2c357-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2c357-118">Read Paths</span></span>



| <span data-ttu-id="2c357-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="2c357-119">Order</span></span> | <span data-ttu-id="2c357-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="2c357-120">Path</span></span>                      | <span data-ttu-id="2c357-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2c357-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2c357-122">1</span><span class="sxs-lookup"><span data-stu-id="2c357-122">1</span></span>     | <span data-ttu-id="2c357-123">/app1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="2c357-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="2c357-124">ascii</span><span class="sxs-lookup"><span data-stu-id="2c357-124">ascii</span></span>       |
| <span data-ttu-id="2c357-125">2</span><span class="sxs-lookup"><span data-stu-id="2c357-125">2</span></span>     | <span data-ttu-id="2c357-126">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="2c357-127">unicode</span><span class="sxs-lookup"><span data-stu-id="2c357-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2c357-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2c357-128">Write Paths</span></span>



| <span data-ttu-id="2c357-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="2c357-129">Order</span></span> | <span data-ttu-id="2c357-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="2c357-130">Path</span></span>                      | <span data-ttu-id="2c357-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2c357-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="2c357-132">1</span><span class="sxs-lookup"><span data-stu-id="2c357-132">1</span></span>     | <span data-ttu-id="2c357-133">/app1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="2c357-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="2c357-134">ascii</span><span class="sxs-lookup"><span data-stu-id="2c357-134">ascii</span></span>       |
| <span data-ttu-id="2c357-135">2</span><span class="sxs-lookup"><span data-stu-id="2c357-135">2</span></span>     | <span data-ttu-id="2c357-136">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="2c357-137">unicode</span><span class="sxs-lookup"><span data-stu-id="2c357-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2c357-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2c357-138">Remove Paths</span></span>



| <span data-ttu-id="2c357-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="2c357-139">Order</span></span> | <span data-ttu-id="2c357-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="2c357-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="2c357-141">1</span><span class="sxs-lookup"><span data-stu-id="2c357-141">1</span></span>     | <span data-ttu-id="2c357-142">/app1/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="2c357-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="2c357-143">2</span><span class="sxs-lookup"><span data-stu-id="2c357-143">2</span></span>     | <span data-ttu-id="2c357-144">/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="2c357-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="2c357-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="2c357-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2c357-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2c357-146">Read Paths</span></span>



| <span data-ttu-id="2c357-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="2c357-147">Order</span></span> | <span data-ttu-id="2c357-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="2c357-148">Path</span></span>                         | <span data-ttu-id="2c357-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2c357-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="2c357-150">1</span><span class="sxs-lookup"><span data-stu-id="2c357-150">1</span></span>     | <span data-ttu-id="2c357-151">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="2c357-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="2c357-152">ascii</span><span class="sxs-lookup"><span data-stu-id="2c357-152">ascii</span></span>       |
| <span data-ttu-id="2c357-153">2</span><span class="sxs-lookup"><span data-stu-id="2c357-153">2</span></span>     | <span data-ttu-id="2c357-154">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="2c357-155">unicode</span><span class="sxs-lookup"><span data-stu-id="2c357-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2c357-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2c357-156">Write Paths</span></span>



| <span data-ttu-id="2c357-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="2c357-157">Order</span></span> | <span data-ttu-id="2c357-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="2c357-158">Path</span></span>                         | <span data-ttu-id="2c357-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2c357-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="2c357-160">1</span><span class="sxs-lookup"><span data-stu-id="2c357-160">1</span></span>     | <span data-ttu-id="2c357-161">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="2c357-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="2c357-162">ascii</span><span class="sxs-lookup"><span data-stu-id="2c357-162">ascii</span></span>       |
| <span data-ttu-id="2c357-163">2</span><span class="sxs-lookup"><span data-stu-id="2c357-163">2</span></span>     | <span data-ttu-id="2c357-164">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="2c357-165">unicode</span><span class="sxs-lookup"><span data-stu-id="2c357-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2c357-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="2c357-166">Remove Paths</span></span>



| <span data-ttu-id="2c357-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="2c357-167">Order</span></span> | <span data-ttu-id="2c357-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="2c357-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="2c357-169">1</span><span class="sxs-lookup"><span data-stu-id="2c357-169">1</span></span>     | <span data-ttu-id="2c357-170">/IFD/GPS/{ushort = 10}</span><span class="sxs-lookup"><span data-stu-id="2c357-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="2c357-171">2</span><span class="sxs-lookup"><span data-stu-id="2c357-171">2</span></span>     | <span data-ttu-id="2c357-172">/ifd/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="2c357-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2c357-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c357-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c357-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c357-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c357-175">System. GPS. MeasureMode</span><span class="sxs-lookup"><span data-stu-id="2c357-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
