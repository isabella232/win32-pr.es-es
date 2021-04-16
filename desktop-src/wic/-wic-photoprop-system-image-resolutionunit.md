---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Directiva de metadatos de la foto de System. Image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706400"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a><span data-ttu-id="074af-103">Directiva de metadatos de la foto de System. Image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-103">System.Image.ResolutionUnit Photo Metadata Policy</span></span>

<span data-ttu-id="074af-104">La Directiva de metadatos de la fotografía para la propiedad [System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .</span><span class="sxs-lookup"><span data-stu-id="074af-104">The photo metadata policy for the [System.Image.ResolutionUnit](../properties/props-system-image-resolutionunit.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="074af-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="074af-105">PKEY</span></span>

<span data-ttu-id="074af-106">PKEY \_ Image \_ ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-106">PKEY\_Image\_ResolutionUnit</span></span>

### <a name="containers"></a><span data-ttu-id="074af-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="074af-107">Containers</span></span>

<span data-ttu-id="074af-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="074af-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="074af-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="074af-109">Read-Only</span></span>

<span data-ttu-id="074af-110">Sí.</span><span class="sxs-lookup"><span data-stu-id="074af-110">Yes.</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="074af-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="074af-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="074af-112">I2 de VT \_</span><span class="sxs-lookup"><span data-stu-id="074af-112">VT\_I2</span></span>

### <a name="input-type"></a><span data-ttu-id="074af-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="074af-113">Input Type</span></span>

<span data-ttu-id="074af-114">UShort</span><span class="sxs-lookup"><span data-stu-id="074af-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="074af-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="074af-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="074af-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="074af-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="074af-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="074af-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="074af-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="074af-118">Read Paths</span></span>



| <span data-ttu-id="074af-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="074af-119">Order</span></span> | <span data-ttu-id="074af-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="074af-120">Path</span></span>                     | <span data-ttu-id="074af-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="074af-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="074af-122">1</span><span class="sxs-lookup"><span data-stu-id="074af-122">1</span></span>     | <span data-ttu-id="074af-123">/app1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="074af-123">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="074af-124">ushort</span><span class="sxs-lookup"><span data-stu-id="074af-124">ushort</span></span>      |
| <span data-ttu-id="074af-125">2</span><span class="sxs-lookup"><span data-stu-id="074af-125">2</span></span>     | <span data-ttu-id="074af-126">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-126">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="074af-127">unicode</span><span class="sxs-lookup"><span data-stu-id="074af-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="074af-128">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="074af-128">Write Paths</span></span>



| <span data-ttu-id="074af-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="074af-129">Order</span></span> | <span data-ttu-id="074af-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="074af-130">Path</span></span>                     | <span data-ttu-id="074af-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="074af-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="074af-132">1</span><span class="sxs-lookup"><span data-stu-id="074af-132">1</span></span>     | <span data-ttu-id="074af-133">/app1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="074af-133">/app1/ifd/{ushort=296}</span></span>   | <span data-ttu-id="074af-134">ushort</span><span class="sxs-lookup"><span data-stu-id="074af-134">ushort</span></span>      |
| <span data-ttu-id="074af-135">2</span><span class="sxs-lookup"><span data-stu-id="074af-135">2</span></span>     | <span data-ttu-id="074af-136">/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-136">/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="074af-137">unicode</span><span class="sxs-lookup"><span data-stu-id="074af-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="074af-138">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="074af-138">Remove Paths</span></span>



| <span data-ttu-id="074af-139">Pedido</span><span class="sxs-lookup"><span data-stu-id="074af-139">Order</span></span> | <span data-ttu-id="074af-140">Ruta</span><span class="sxs-lookup"><span data-stu-id="074af-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="074af-141">1</span><span class="sxs-lookup"><span data-stu-id="074af-141">1</span></span>     | <span data-ttu-id="074af-142">/app1/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="074af-142">/app1/ifd/{ushort=296}</span></span>   |
| <span data-ttu-id="074af-143">2</span><span class="sxs-lookup"><span data-stu-id="074af-143">2</span></span>     | <span data-ttu-id="074af-144">/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="074af-144">/xmp/tiff:resolutionunit</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="074af-145">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="074af-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="074af-146">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="074af-146">Read Paths</span></span>



| <span data-ttu-id="074af-147">Pedido</span><span class="sxs-lookup"><span data-stu-id="074af-147">Order</span></span> | <span data-ttu-id="074af-148">Ruta</span><span class="sxs-lookup"><span data-stu-id="074af-148">Path</span></span>                         | <span data-ttu-id="074af-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="074af-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="074af-150">1</span><span class="sxs-lookup"><span data-stu-id="074af-150">1</span></span>     | <span data-ttu-id="074af-151">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="074af-151">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="074af-152">ushort</span><span class="sxs-lookup"><span data-stu-id="074af-152">ushort</span></span>      |
| <span data-ttu-id="074af-153">2</span><span class="sxs-lookup"><span data-stu-id="074af-153">2</span></span>     | <span data-ttu-id="074af-154">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-154">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="074af-155">unicode</span><span class="sxs-lookup"><span data-stu-id="074af-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="074af-156">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="074af-156">Write Paths</span></span>



| <span data-ttu-id="074af-157">Pedido</span><span class="sxs-lookup"><span data-stu-id="074af-157">Order</span></span> | <span data-ttu-id="074af-158">Ruta</span><span class="sxs-lookup"><span data-stu-id="074af-158">Path</span></span>                         | <span data-ttu-id="074af-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="074af-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="074af-160">1</span><span class="sxs-lookup"><span data-stu-id="074af-160">1</span></span>     | <span data-ttu-id="074af-161">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="074af-161">/ifd/{ushort=296}</span></span>            | <span data-ttu-id="074af-162">ushort</span><span class="sxs-lookup"><span data-stu-id="074af-162">ushort</span></span>      |
| <span data-ttu-id="074af-163">2</span><span class="sxs-lookup"><span data-stu-id="074af-163">2</span></span>     | <span data-ttu-id="074af-164">/ifd/xmp/tiff:ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-164">/ifd/xmp/tiff:ResolutionUnit</span></span> | <span data-ttu-id="074af-165">unicode</span><span class="sxs-lookup"><span data-stu-id="074af-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="074af-166">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="074af-166">Remove Paths</span></span>



| <span data-ttu-id="074af-167">Pedido</span><span class="sxs-lookup"><span data-stu-id="074af-167">Order</span></span> | <span data-ttu-id="074af-168">Ruta</span><span class="sxs-lookup"><span data-stu-id="074af-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="074af-169">1</span><span class="sxs-lookup"><span data-stu-id="074af-169">1</span></span>     | <span data-ttu-id="074af-170">/IFD/{ushort = 296}</span><span class="sxs-lookup"><span data-stu-id="074af-170">/ifd/{ushort=296}</span></span>            |
| <span data-ttu-id="074af-171">2</span><span class="sxs-lookup"><span data-stu-id="074af-171">2</span></span>     | <span data-ttu-id="074af-172">/ifd/xmp/tiff:resolutionunit</span><span class="sxs-lookup"><span data-stu-id="074af-172">/ifd/xmp/tiff:resolutionunit</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="074af-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="074af-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="074af-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="074af-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="074af-175">System. Image. ResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="074af-175">System.Image.ResolutionUnit</span></span>](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
