---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Directiva de metadatos de la foto System. GPS. ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716889"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="8e807-103">Directiva de metadatos de la foto System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="8e807-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. ImgDirection](../properties/props-system-gps-imgdirection.md) .</span><span class="sxs-lookup"><span data-stu-id="8e807-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8e807-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8e807-105">PKEY</span></span>

<span data-ttu-id="8e807-106">PKEY \_ GPS \_ ImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="8e807-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="8e807-107">Containers</span></span>

<span data-ttu-id="8e807-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8e807-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8e807-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e807-109">Read-Only</span></span>

<span data-ttu-id="8e807-110">Sí</span><span class="sxs-lookup"><span data-stu-id="8e807-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8e807-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="8e807-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8e807-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="8e807-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8e807-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="8e807-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="8e807-114">Este valor se puede escribir escribiendo en System. GPS. ImgDirectionNumerator y System. GPS. ImgDirectionDenominator.</span><span class="sxs-lookup"><span data-stu-id="8e807-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="8e807-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="8e807-115">It cannot be written directly.</span></span> <span data-ttu-id="8e807-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="8e807-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="8e807-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="8e807-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="8e807-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8e807-118">Read Paths</span></span>



| <span data-ttu-id="8e807-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="8e807-119">Order</span></span> | <span data-ttu-id="8e807-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="8e807-120">Path</span></span>                      | <span data-ttu-id="8e807-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8e807-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8e807-122">1</span><span class="sxs-lookup"><span data-stu-id="8e807-122">1</span></span>     | <span data-ttu-id="8e807-123">/app1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="8e807-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="8e807-124">2</span><span class="sxs-lookup"><span data-stu-id="8e807-124">2</span></span>     | <span data-ttu-id="8e807-125">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8e807-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8e807-126">Write Paths</span></span>



| <span data-ttu-id="8e807-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="8e807-127">Order</span></span> | <span data-ttu-id="8e807-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="8e807-128">Path</span></span>                      | <span data-ttu-id="8e807-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8e807-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8e807-130">1</span><span class="sxs-lookup"><span data-stu-id="8e807-130">1</span></span>     | <span data-ttu-id="8e807-131">/app1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="8e807-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="8e807-132">2</span><span class="sxs-lookup"><span data-stu-id="8e807-132">2</span></span>     | <span data-ttu-id="8e807-133">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8e807-134">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8e807-134">Remove Paths</span></span>



| <span data-ttu-id="8e807-135">Pedido</span><span class="sxs-lookup"><span data-stu-id="8e807-135">Order</span></span> | <span data-ttu-id="8e807-136">Ruta</span><span class="sxs-lookup"><span data-stu-id="8e807-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="8e807-137">1</span><span class="sxs-lookup"><span data-stu-id="8e807-137">1</span></span>     | <span data-ttu-id="8e807-138">/app1/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="8e807-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="8e807-139">2</span><span class="sxs-lookup"><span data-stu-id="8e807-139">2</span></span>     | <span data-ttu-id="8e807-140">/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="8e807-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="8e807-141">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="8e807-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8e807-142">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8e807-142">Read Paths</span></span>



| <span data-ttu-id="8e807-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="8e807-143">Order</span></span> | <span data-ttu-id="8e807-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="8e807-144">Path</span></span>                          | <span data-ttu-id="8e807-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8e807-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8e807-146">1</span><span class="sxs-lookup"><span data-stu-id="8e807-146">1</span></span>     | <span data-ttu-id="8e807-147">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="8e807-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="8e807-148">2</span><span class="sxs-lookup"><span data-stu-id="8e807-148">2</span></span>     | <span data-ttu-id="8e807-149">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="8e807-150">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8e807-150">Write Paths</span></span>



| <span data-ttu-id="8e807-151">Pedido</span><span class="sxs-lookup"><span data-stu-id="8e807-151">Order</span></span> | <span data-ttu-id="8e807-152">Ruta</span><span class="sxs-lookup"><span data-stu-id="8e807-152">Path</span></span>                          | <span data-ttu-id="8e807-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8e807-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="8e807-154">1</span><span class="sxs-lookup"><span data-stu-id="8e807-154">1</span></span>     | <span data-ttu-id="8e807-155">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="8e807-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="8e807-156">2</span><span class="sxs-lookup"><span data-stu-id="8e807-156">2</span></span>     | <span data-ttu-id="8e807-157">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="8e807-158">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8e807-158">Remove Paths</span></span>



| <span data-ttu-id="8e807-159">Pedido</span><span class="sxs-lookup"><span data-stu-id="8e807-159">Order</span></span> | <span data-ttu-id="8e807-160">Ruta</span><span class="sxs-lookup"><span data-stu-id="8e807-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="8e807-161">1</span><span class="sxs-lookup"><span data-stu-id="8e807-161">1</span></span>     | <span data-ttu-id="8e807-162">/IFD/GPS/{ushort = 17}</span><span class="sxs-lookup"><span data-stu-id="8e807-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="8e807-163">2</span><span class="sxs-lookup"><span data-stu-id="8e807-163">2</span></span>     | <span data-ttu-id="8e807-164">/ifd/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="8e807-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8e807-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e807-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e807-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e807-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e807-167">System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="8e807-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
