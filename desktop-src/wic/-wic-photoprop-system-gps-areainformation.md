---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Directiva de metadatos de la foto System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360882"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="ead56-103">Directiva de metadatos de la foto System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="ead56-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .</span><span class="sxs-lookup"><span data-stu-id="ead56-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="ead56-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="ead56-105">PKEY</span></span>

<span data-ttu-id="ead56-106">PKEY \_ GPS \_ AreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="ead56-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="ead56-107">Containers</span></span>

<span data-ttu-id="ead56-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="ead56-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="ead56-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ead56-109">Read-Only</span></span>

<span data-ttu-id="ead56-110">No</span><span class="sxs-lookup"><span data-stu-id="ead56-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="ead56-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="ead56-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="ead56-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="ead56-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="ead56-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="ead56-113">Input Type</span></span>

<span data-ttu-id="ead56-114">String.</span><span class="sxs-lookup"><span data-stu-id="ead56-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="ead56-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="ead56-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="ead56-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="ead56-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="ead56-117">Directivas JPEG</span><span class="sxs-lookup"><span data-stu-id="ead56-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ead56-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ead56-118">Read Paths</span></span>



| <span data-ttu-id="ead56-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="ead56-119">Order</span></span> | <span data-ttu-id="ead56-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="ead56-120">Path</span></span>                         | <span data-ttu-id="ead56-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ead56-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ead56-122">1</span><span class="sxs-lookup"><span data-stu-id="ead56-122">1</span></span>     | <span data-ttu-id="ead56-123">/app1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="ead56-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="ead56-124">2</span><span class="sxs-lookup"><span data-stu-id="ead56-124">2</span></span>     | <span data-ttu-id="ead56-125">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="ead56-126">unicode</span><span class="sxs-lookup"><span data-stu-id="ead56-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ead56-127">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ead56-127">Write Paths</span></span>



| <span data-ttu-id="ead56-128">Pedido</span><span class="sxs-lookup"><span data-stu-id="ead56-128">Order</span></span> | <span data-ttu-id="ead56-129">Ruta</span><span class="sxs-lookup"><span data-stu-id="ead56-129">Path</span></span>                         | <span data-ttu-id="ead56-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ead56-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="ead56-131">1</span><span class="sxs-lookup"><span data-stu-id="ead56-131">1</span></span>     | <span data-ttu-id="ead56-132">/app1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="ead56-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="ead56-133">2</span><span class="sxs-lookup"><span data-stu-id="ead56-133">2</span></span>     | <span data-ttu-id="ead56-134">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="ead56-135">unicode</span><span class="sxs-lookup"><span data-stu-id="ead56-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ead56-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ead56-136">Remove Paths</span></span>



| <span data-ttu-id="ead56-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="ead56-137">Order</span></span> | <span data-ttu-id="ead56-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="ead56-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="ead56-139">1</span><span class="sxs-lookup"><span data-stu-id="ead56-139">1</span></span>     | <span data-ttu-id="ead56-140">/app1/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="ead56-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="ead56-141">2</span><span class="sxs-lookup"><span data-stu-id="ead56-141">2</span></span>     | <span data-ttu-id="ead56-142">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="ead56-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="ead56-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="ead56-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ead56-144">Read Paths</span></span>



| <span data-ttu-id="ead56-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="ead56-145">Order</span></span> | <span data-ttu-id="ead56-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="ead56-146">Path</span></span>                             | <span data-ttu-id="ead56-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ead56-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="ead56-148">1</span><span class="sxs-lookup"><span data-stu-id="ead56-148">1</span></span>     | <span data-ttu-id="ead56-149">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="ead56-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="ead56-150">2</span><span class="sxs-lookup"><span data-stu-id="ead56-150">2</span></span>     | <span data-ttu-id="ead56-151">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="ead56-152">unicode</span><span class="sxs-lookup"><span data-stu-id="ead56-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="ead56-153">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ead56-153">Write Paths</span></span>



| <span data-ttu-id="ead56-154">Pedido</span><span class="sxs-lookup"><span data-stu-id="ead56-154">Order</span></span> | <span data-ttu-id="ead56-155">Ruta</span><span class="sxs-lookup"><span data-stu-id="ead56-155">Path</span></span>                             | <span data-ttu-id="ead56-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="ead56-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="ead56-157">1</span><span class="sxs-lookup"><span data-stu-id="ead56-157">1</span></span>     | <span data-ttu-id="ead56-158">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="ead56-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="ead56-159">2</span><span class="sxs-lookup"><span data-stu-id="ead56-159">2</span></span>     | <span data-ttu-id="ead56-160">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="ead56-161">unicode</span><span class="sxs-lookup"><span data-stu-id="ead56-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="ead56-162">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="ead56-162">Remove Paths</span></span>



| <span data-ttu-id="ead56-163">Pedido</span><span class="sxs-lookup"><span data-stu-id="ead56-163">Order</span></span> | <span data-ttu-id="ead56-164">Ruta</span><span class="sxs-lookup"><span data-stu-id="ead56-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="ead56-165">1</span><span class="sxs-lookup"><span data-stu-id="ead56-165">1</span></span>     | <span data-ttu-id="ead56-166">/IFD/GPS/{ushort = 28}</span><span class="sxs-lookup"><span data-stu-id="ead56-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="ead56-167">2</span><span class="sxs-lookup"><span data-stu-id="ead56-167">2</span></span>     | <span data-ttu-id="ead56-168">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ead56-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ead56-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="ead56-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ead56-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead56-171">System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="ead56-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
