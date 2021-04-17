---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Directiva de metadatos de la foto System. GPS. VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706407"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="3e1a8-103">Directiva de metadatos de la foto System. GPS. VersionID</span><span class="sxs-lookup"><span data-stu-id="3e1a8-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="3e1a8-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. VersionID](../properties/props-system-gps-versionid.md) .</span><span class="sxs-lookup"><span data-stu-id="3e1a8-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3e1a8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3e1a8-105">PKEY</span></span>

<span data-ttu-id="3e1a8-106">\_VersionID de GPS de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="3e1a8-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="3e1a8-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="3e1a8-107">Containers</span></span>

<span data-ttu-id="3e1a8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3e1a8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3e1a8-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e1a8-109">Read-Only</span></span>

<span data-ttu-id="3e1a8-110">No</span><span class="sxs-lookup"><span data-stu-id="3e1a8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3e1a8-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="3e1a8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3e1a8-112">interfaz de usuario de VT \_ vectorial VT \| \_</span><span class="sxs-lookup"><span data-stu-id="3e1a8-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="3e1a8-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="3e1a8-113">Input Type</span></span>

<span data-ttu-id="3e1a8-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="3e1a8-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3e1a8-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="3e1a8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3e1a8-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="3e1a8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="3e1a8-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="3e1a8-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3e1a8-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3e1a8-118">Read Paths</span></span>



| <span data-ttu-id="3e1a8-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="3e1a8-119">Order</span></span> | <span data-ttu-id="3e1a8-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="3e1a8-120">Path</span></span>                     | <span data-ttu-id="3e1a8-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3e1a8-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3e1a8-122">1</span><span class="sxs-lookup"><span data-stu-id="3e1a8-122">1</span></span>     | <span data-ttu-id="3e1a8-123">/app1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3e1a8-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="3e1a8-124">2</span><span class="sxs-lookup"><span data-stu-id="3e1a8-124">2</span></span>     | <span data-ttu-id="3e1a8-125">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3e1a8-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="3e1a8-126">unicode</span><span class="sxs-lookup"><span data-stu-id="3e1a8-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3e1a8-127">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3e1a8-127">Write Paths</span></span>



| <span data-ttu-id="3e1a8-128">Pedido</span><span class="sxs-lookup"><span data-stu-id="3e1a8-128">Order</span></span> | <span data-ttu-id="3e1a8-129">Ruta</span><span class="sxs-lookup"><span data-stu-id="3e1a8-129">Path</span></span>                     | <span data-ttu-id="3e1a8-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3e1a8-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="3e1a8-131">1</span><span class="sxs-lookup"><span data-stu-id="3e1a8-131">1</span></span>     | <span data-ttu-id="3e1a8-132">/app1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3e1a8-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="3e1a8-133">2</span><span class="sxs-lookup"><span data-stu-id="3e1a8-133">2</span></span>     | <span data-ttu-id="3e1a8-134">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3e1a8-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="3e1a8-135">unicode</span><span class="sxs-lookup"><span data-stu-id="3e1a8-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3e1a8-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3e1a8-136">Remove Paths</span></span>



| <span data-ttu-id="3e1a8-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="3e1a8-137">Order</span></span> | <span data-ttu-id="3e1a8-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="3e1a8-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="3e1a8-139">1</span><span class="sxs-lookup"><span data-stu-id="3e1a8-139">1</span></span>     | <span data-ttu-id="3e1a8-140">/app1/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3e1a8-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="3e1a8-141">2</span><span class="sxs-lookup"><span data-stu-id="3e1a8-141">2</span></span>     | <span data-ttu-id="3e1a8-142">/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="3e1a8-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="3e1a8-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="3e1a8-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3e1a8-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3e1a8-144">Read Paths</span></span>



| <span data-ttu-id="3e1a8-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="3e1a8-145">Order</span></span> | <span data-ttu-id="3e1a8-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="3e1a8-146">Path</span></span>                       | <span data-ttu-id="3e1a8-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3e1a8-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="3e1a8-148">1</span><span class="sxs-lookup"><span data-stu-id="3e1a8-148">1</span></span>     | <span data-ttu-id="3e1a8-149">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3e1a8-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="3e1a8-150">2</span><span class="sxs-lookup"><span data-stu-id="3e1a8-150">2</span></span>     | <span data-ttu-id="3e1a8-151">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3e1a8-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="3e1a8-152">unicode</span><span class="sxs-lookup"><span data-stu-id="3e1a8-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3e1a8-153">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3e1a8-153">Write Paths</span></span>



| <span data-ttu-id="3e1a8-154">Pedido</span><span class="sxs-lookup"><span data-stu-id="3e1a8-154">Order</span></span> | <span data-ttu-id="3e1a8-155">Ruta</span><span class="sxs-lookup"><span data-stu-id="3e1a8-155">Path</span></span>                       | <span data-ttu-id="3e1a8-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3e1a8-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="3e1a8-157">1</span><span class="sxs-lookup"><span data-stu-id="3e1a8-157">1</span></span>     | <span data-ttu-id="3e1a8-158">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3e1a8-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="3e1a8-159">2</span><span class="sxs-lookup"><span data-stu-id="3e1a8-159">2</span></span>     | <span data-ttu-id="3e1a8-160">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="3e1a8-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="3e1a8-161">unicode</span><span class="sxs-lookup"><span data-stu-id="3e1a8-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3e1a8-162">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="3e1a8-162">Remove Paths</span></span>



| <span data-ttu-id="3e1a8-163">Pedido</span><span class="sxs-lookup"><span data-stu-id="3e1a8-163">Order</span></span> | <span data-ttu-id="3e1a8-164">Ruta</span><span class="sxs-lookup"><span data-stu-id="3e1a8-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="3e1a8-165">1</span><span class="sxs-lookup"><span data-stu-id="3e1a8-165">1</span></span>     | <span data-ttu-id="3e1a8-166">/IFD/GPS/{ushort = 0}</span><span class="sxs-lookup"><span data-stu-id="3e1a8-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="3e1a8-167">2</span><span class="sxs-lookup"><span data-stu-id="3e1a8-167">2</span></span>     | <span data-ttu-id="3e1a8-168">/ifd/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="3e1a8-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3e1a8-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e1a8-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e1a8-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e1a8-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e1a8-171">System. GPS. VersionID</span><span class="sxs-lookup"><span data-stu-id="3e1a8-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
