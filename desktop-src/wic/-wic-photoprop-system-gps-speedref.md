---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Directiva de metadatos de la foto System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697492"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="8eea1-103">Directiva de metadatos de la foto System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="8eea1-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .</span><span class="sxs-lookup"><span data-stu-id="8eea1-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="8eea1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="8eea1-105">PKEY</span></span>

<span data-ttu-id="8eea1-106">PKEY \_ GPS \_ SpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="8eea1-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="8eea1-107">Containers</span></span>

<span data-ttu-id="8eea1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="8eea1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="8eea1-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8eea1-109">Read-Only</span></span>

<span data-ttu-id="8eea1-110">No</span><span class="sxs-lookup"><span data-stu-id="8eea1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="8eea1-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="8eea1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="8eea1-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="8eea1-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="8eea1-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="8eea1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="8eea1-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="8eea1-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="8eea1-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="8eea1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="8eea1-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="8eea1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="8eea1-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="8eea1-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8eea1-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8eea1-118">Read Paths</span></span>



| <span data-ttu-id="8eea1-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="8eea1-119">Order</span></span> | <span data-ttu-id="8eea1-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="8eea1-120">Path</span></span>                      | <span data-ttu-id="8eea1-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8eea1-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8eea1-122">1</span><span class="sxs-lookup"><span data-stu-id="8eea1-122">1</span></span>     | <span data-ttu-id="8eea1-123">/app1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8eea1-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="8eea1-124">ascii</span><span class="sxs-lookup"><span data-stu-id="8eea1-124">ascii</span></span>       |
| <span data-ttu-id="8eea1-125">2</span><span class="sxs-lookup"><span data-stu-id="8eea1-125">2</span></span>     | <span data-ttu-id="8eea1-126">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="8eea1-127">unicode</span><span class="sxs-lookup"><span data-stu-id="8eea1-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="8eea1-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8eea1-128">Write Paths</span></span>



| <span data-ttu-id="8eea1-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="8eea1-129">Order</span></span> | <span data-ttu-id="8eea1-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="8eea1-130">Path</span></span>                      | <span data-ttu-id="8eea1-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8eea1-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8eea1-132">1</span><span class="sxs-lookup"><span data-stu-id="8eea1-132">1</span></span>     | <span data-ttu-id="8eea1-133">/app1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8eea1-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="8eea1-134">ascii</span><span class="sxs-lookup"><span data-stu-id="8eea1-134">ascii</span></span>       |
| <span data-ttu-id="8eea1-135">2</span><span class="sxs-lookup"><span data-stu-id="8eea1-135">2</span></span>     | <span data-ttu-id="8eea1-136">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="8eea1-137">unicode</span><span class="sxs-lookup"><span data-stu-id="8eea1-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8eea1-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8eea1-138">Remove Paths</span></span>



| <span data-ttu-id="8eea1-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="8eea1-139">Order</span></span> | <span data-ttu-id="8eea1-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="8eea1-140">Path</span></span>                      | <span data-ttu-id="8eea1-141">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8eea1-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8eea1-142">1</span><span class="sxs-lookup"><span data-stu-id="8eea1-142">1</span></span>     | <span data-ttu-id="8eea1-143">/app1/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8eea1-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="8eea1-144">2</span><span class="sxs-lookup"><span data-stu-id="8eea1-144">2</span></span>     | <span data-ttu-id="8eea1-145">/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="8eea1-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="8eea1-146">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="8eea1-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="8eea1-147">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8eea1-147">Read Paths</span></span>



| <span data-ttu-id="8eea1-148">Pedido</span><span class="sxs-lookup"><span data-stu-id="8eea1-148">Order</span></span> | <span data-ttu-id="8eea1-149">Ruta</span><span class="sxs-lookup"><span data-stu-id="8eea1-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="8eea1-150">1</span><span class="sxs-lookup"><span data-stu-id="8eea1-150">1</span></span>     | <span data-ttu-id="8eea1-151">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8eea1-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="8eea1-152">ascii</span><span class="sxs-lookup"><span data-stu-id="8eea1-152">ascii</span></span>   |
| <span data-ttu-id="8eea1-153">2</span><span class="sxs-lookup"><span data-stu-id="8eea1-153">2</span></span>     | <span data-ttu-id="8eea1-154">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="8eea1-155">unicode</span><span class="sxs-lookup"><span data-stu-id="8eea1-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="8eea1-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8eea1-156">Write Paths</span></span>



| <span data-ttu-id="8eea1-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="8eea1-157">Order</span></span> | <span data-ttu-id="8eea1-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="8eea1-158">Path</span></span>                      | <span data-ttu-id="8eea1-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="8eea1-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="8eea1-160">1</span><span class="sxs-lookup"><span data-stu-id="8eea1-160">1</span></span>     | <span data-ttu-id="8eea1-161">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8eea1-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="8eea1-162">ascii</span><span class="sxs-lookup"><span data-stu-id="8eea1-162">ascii</span></span>       |
| <span data-ttu-id="8eea1-163">2</span><span class="sxs-lookup"><span data-stu-id="8eea1-163">2</span></span>     | <span data-ttu-id="8eea1-164">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="8eea1-165">unicode</span><span class="sxs-lookup"><span data-stu-id="8eea1-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="8eea1-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="8eea1-166">Remove Paths</span></span>



| <span data-ttu-id="8eea1-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="8eea1-167">Order</span></span> | <span data-ttu-id="8eea1-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="8eea1-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="8eea1-169">1</span><span class="sxs-lookup"><span data-stu-id="8eea1-169">1</span></span>     | <span data-ttu-id="8eea1-170">/IFD/GPS/{ushort = 12}</span><span class="sxs-lookup"><span data-stu-id="8eea1-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="8eea1-171">2</span><span class="sxs-lookup"><span data-stu-id="8eea1-171">2</span></span>     | <span data-ttu-id="8eea1-172">/ifd/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="8eea1-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8eea1-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8eea1-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eea1-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8eea1-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eea1-175">System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="8eea1-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
