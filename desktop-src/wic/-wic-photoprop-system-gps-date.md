---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Directiva de metadatos de la foto System. GPS. Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278839"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="9c61e-103">Directiva de metadatos de la foto System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="9c61e-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="9c61e-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Date](../properties/props-system-gps-date.md) .</span><span class="sxs-lookup"><span data-stu-id="9c61e-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9c61e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9c61e-105">PKEY</span></span>

<span data-ttu-id="9c61e-106">Fecha de PKEY \_ GPS \_</span><span class="sxs-lookup"><span data-stu-id="9c61e-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="9c61e-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="9c61e-107">Containers</span></span>

<span data-ttu-id="9c61e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9c61e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9c61e-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c61e-109">Read-Only</span></span>

<span data-ttu-id="9c61e-110">No</span><span class="sxs-lookup"><span data-stu-id="9c61e-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="9c61e-111">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="9c61e-111">Input Type</span></span>

<span data-ttu-id="9c61e-112">String.</span><span class="sxs-lookup"><span data-stu-id="9c61e-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9c61e-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="9c61e-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="9c61e-114">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="9c61e-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="9c61e-115">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="9c61e-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9c61e-116">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9c61e-116">Read Paths</span></span>



| <span data-ttu-id="9c61e-117">Pedido</span><span class="sxs-lookup"><span data-stu-id="9c61e-117">Order</span></span> | <span data-ttu-id="9c61e-118">Ruta</span><span class="sxs-lookup"><span data-stu-id="9c61e-118">Path</span></span>                      | <span data-ttu-id="9c61e-119">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c61e-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9c61e-120">1</span><span class="sxs-lookup"><span data-stu-id="9c61e-120">1</span></span>     | <span data-ttu-id="9c61e-121">/app1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="9c61e-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="9c61e-122">ascii</span><span class="sxs-lookup"><span data-stu-id="9c61e-122">ascii</span></span>       |
| <span data-ttu-id="9c61e-123">2</span><span class="sxs-lookup"><span data-stu-id="9c61e-123">2</span></span>     | <span data-ttu-id="9c61e-124">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c61e-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="9c61e-125">unicode</span><span class="sxs-lookup"><span data-stu-id="9c61e-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9c61e-126">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9c61e-126">Write Paths</span></span>



| <span data-ttu-id="9c61e-127">Pedido</span><span class="sxs-lookup"><span data-stu-id="9c61e-127">Order</span></span> | <span data-ttu-id="9c61e-128">Ruta</span><span class="sxs-lookup"><span data-stu-id="9c61e-128">Path</span></span>                      | <span data-ttu-id="9c61e-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c61e-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="9c61e-130">1</span><span class="sxs-lookup"><span data-stu-id="9c61e-130">1</span></span>     | <span data-ttu-id="9c61e-131">/app1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="9c61e-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="9c61e-132">ascii</span><span class="sxs-lookup"><span data-stu-id="9c61e-132">ascii</span></span>       |
| <span data-ttu-id="9c61e-133">2</span><span class="sxs-lookup"><span data-stu-id="9c61e-133">2</span></span>     | <span data-ttu-id="9c61e-134">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c61e-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="9c61e-135">unicode</span><span class="sxs-lookup"><span data-stu-id="9c61e-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9c61e-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9c61e-136">Remove Paths</span></span>



| <span data-ttu-id="9c61e-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="9c61e-137">Order</span></span> | <span data-ttu-id="9c61e-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="9c61e-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="9c61e-139">1</span><span class="sxs-lookup"><span data-stu-id="9c61e-139">1</span></span>     | <span data-ttu-id="9c61e-140">/app1/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="9c61e-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="9c61e-141">2</span><span class="sxs-lookup"><span data-stu-id="9c61e-141">2</span></span>     | <span data-ttu-id="9c61e-142">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c61e-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="9c61e-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="9c61e-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9c61e-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9c61e-144">Read Paths</span></span>



| <span data-ttu-id="9c61e-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="9c61e-145">Order</span></span> | <span data-ttu-id="9c61e-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="9c61e-146">Path</span></span>                       | <span data-ttu-id="9c61e-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c61e-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9c61e-148">1</span><span class="sxs-lookup"><span data-stu-id="9c61e-148">1</span></span>     | <span data-ttu-id="9c61e-149">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="9c61e-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="9c61e-150">ascii</span><span class="sxs-lookup"><span data-stu-id="9c61e-150">ascii</span></span>       |
| <span data-ttu-id="9c61e-151">2</span><span class="sxs-lookup"><span data-stu-id="9c61e-151">2</span></span>     | <span data-ttu-id="9c61e-152">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c61e-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="9c61e-153">unicode</span><span class="sxs-lookup"><span data-stu-id="9c61e-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="9c61e-154">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9c61e-154">Write Paths</span></span>



| <span data-ttu-id="9c61e-155">Pedido</span><span class="sxs-lookup"><span data-stu-id="9c61e-155">Order</span></span> | <span data-ttu-id="9c61e-156">Ruta</span><span class="sxs-lookup"><span data-stu-id="9c61e-156">Path</span></span>                       | <span data-ttu-id="9c61e-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c61e-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9c61e-158">1</span><span class="sxs-lookup"><span data-stu-id="9c61e-158">1</span></span>     | <span data-ttu-id="9c61e-159">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="9c61e-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="9c61e-160">ascii</span><span class="sxs-lookup"><span data-stu-id="9c61e-160">ascii</span></span>       |
| <span data-ttu-id="9c61e-161">2</span><span class="sxs-lookup"><span data-stu-id="9c61e-161">2</span></span>     | <span data-ttu-id="9c61e-162">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c61e-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="9c61e-163">unicode</span><span class="sxs-lookup"><span data-stu-id="9c61e-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="9c61e-164">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="9c61e-164">Remove Paths</span></span>



| <span data-ttu-id="9c61e-165">Pedido</span><span class="sxs-lookup"><span data-stu-id="9c61e-165">Order</span></span> | <span data-ttu-id="9c61e-166">Ruta</span><span class="sxs-lookup"><span data-stu-id="9c61e-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="9c61e-167">1</span><span class="sxs-lookup"><span data-stu-id="9c61e-167">1</span></span>     | <span data-ttu-id="9c61e-168">/IFD/GPS/{ushort = 29}</span><span class="sxs-lookup"><span data-stu-id="9c61e-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="9c61e-169">2</span><span class="sxs-lookup"><span data-stu-id="9c61e-169">2</span></span>     | <span data-ttu-id="9c61e-170">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c61e-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c61e-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c61e-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c61e-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c61e-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c61e-173">System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="9c61e-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
