---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Directiva de metadatos de la foto de System. Photo. ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002578"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="0952b-103">Directiva de metadatos de la foto de System. Photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="0952b-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. ProgramMode](../properties/props-system-photo-programmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0952b-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0952b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0952b-105">PKEY</span></span>

<span data-ttu-id="0952b-106">PKEY \_ Photo \_ ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="0952b-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="0952b-107">Containers</span></span>

<span data-ttu-id="0952b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0952b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0952b-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0952b-109">Read-Only</span></span>

<span data-ttu-id="0952b-110">No</span><span class="sxs-lookup"><span data-stu-id="0952b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0952b-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="0952b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0952b-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="0952b-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="0952b-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="0952b-113">Input Type</span></span>

<span data-ttu-id="0952b-114">UShort</span><span class="sxs-lookup"><span data-stu-id="0952b-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0952b-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="0952b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0952b-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="0952b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0952b-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="0952b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0952b-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="0952b-118">Read Paths</span></span>



| <span data-ttu-id="0952b-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="0952b-119">Order</span></span> | <span data-ttu-id="0952b-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="0952b-120">Path</span></span>                          | <span data-ttu-id="0952b-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0952b-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0952b-122">1</span><span class="sxs-lookup"><span data-stu-id="0952b-122">1</span></span>     | <span data-ttu-id="0952b-123">/app1/IFD/Exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0952b-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="0952b-124">ushort</span><span class="sxs-lookup"><span data-stu-id="0952b-124">ushort</span></span>      |
| <span data-ttu-id="0952b-125">2</span><span class="sxs-lookup"><span data-stu-id="0952b-125">2</span></span>     | <span data-ttu-id="0952b-126">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="0952b-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="0952b-127">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-127">unicode</span></span>     |
| <span data-ttu-id="0952b-128">3</span><span class="sxs-lookup"><span data-stu-id="0952b-128">3</span></span>     | <span data-ttu-id="0952b-129">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="0952b-130">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0952b-131">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="0952b-131">Write Paths</span></span>



| <span data-ttu-id="0952b-132">Pedido</span><span class="sxs-lookup"><span data-stu-id="0952b-132">Order</span></span> | <span data-ttu-id="0952b-133">Ruta</span><span class="sxs-lookup"><span data-stu-id="0952b-133">Path</span></span>                          | <span data-ttu-id="0952b-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0952b-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0952b-135">1</span><span class="sxs-lookup"><span data-stu-id="0952b-135">1</span></span>     | <span data-ttu-id="0952b-136">/app1/IFD/Exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0952b-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="0952b-137">ushort</span><span class="sxs-lookup"><span data-stu-id="0952b-137">ushort</span></span>      |
| <span data-ttu-id="0952b-138">2</span><span class="sxs-lookup"><span data-stu-id="0952b-138">2</span></span>     | <span data-ttu-id="0952b-139">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="0952b-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="0952b-140">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-140">unicode</span></span>     |
| <span data-ttu-id="0952b-141">3</span><span class="sxs-lookup"><span data-stu-id="0952b-141">3</span></span>     | <span data-ttu-id="0952b-142">/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="0952b-143">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0952b-144">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="0952b-144">Remove Paths</span></span>



| <span data-ttu-id="0952b-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="0952b-145">Order</span></span> | <span data-ttu-id="0952b-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="0952b-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0952b-147">1</span><span class="sxs-lookup"><span data-stu-id="0952b-147">1</span></span>     | <span data-ttu-id="0952b-148">/app1/IFD/Exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0952b-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="0952b-149">2</span><span class="sxs-lookup"><span data-stu-id="0952b-149">2</span></span>     | <span data-ttu-id="0952b-150">/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="0952b-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="0952b-151">3</span><span class="sxs-lookup"><span data-stu-id="0952b-151">3</span></span>     | <span data-ttu-id="0952b-152">/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="0952b-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="0952b-153">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="0952b-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0952b-154">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="0952b-154">Read Paths</span></span>



| <span data-ttu-id="0952b-155">Pedido</span><span class="sxs-lookup"><span data-stu-id="0952b-155">Order</span></span> | <span data-ttu-id="0952b-156">Ruta</span><span class="sxs-lookup"><span data-stu-id="0952b-156">Path</span></span>                          | <span data-ttu-id="0952b-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0952b-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0952b-158">1</span><span class="sxs-lookup"><span data-stu-id="0952b-158">1</span></span>     | <span data-ttu-id="0952b-159">/IFD/Exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0952b-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="0952b-160">ushort</span><span class="sxs-lookup"><span data-stu-id="0952b-160">ushort</span></span>      |
| <span data-ttu-id="0952b-161">2</span><span class="sxs-lookup"><span data-stu-id="0952b-161">2</span></span>     | <span data-ttu-id="0952b-162">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="0952b-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="0952b-163">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-163">unicode</span></span>     |
| <span data-ttu-id="0952b-164">3</span><span class="sxs-lookup"><span data-stu-id="0952b-164">3</span></span>     | <span data-ttu-id="0952b-165">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="0952b-166">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0952b-167">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="0952b-167">Write Paths</span></span>



| <span data-ttu-id="0952b-168">Pedido</span><span class="sxs-lookup"><span data-stu-id="0952b-168">Order</span></span> | <span data-ttu-id="0952b-169">Ruta</span><span class="sxs-lookup"><span data-stu-id="0952b-169">Path</span></span>                          | <span data-ttu-id="0952b-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0952b-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0952b-171">1</span><span class="sxs-lookup"><span data-stu-id="0952b-171">1</span></span>     | <span data-ttu-id="0952b-172">/IFD/Exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0952b-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="0952b-173">ushort</span><span class="sxs-lookup"><span data-stu-id="0952b-173">ushort</span></span>      |
| <span data-ttu-id="0952b-174">2</span><span class="sxs-lookup"><span data-stu-id="0952b-174">2</span></span>     | <span data-ttu-id="0952b-175">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="0952b-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="0952b-176">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-176">unicode</span></span>     |
| <span data-ttu-id="0952b-177">3</span><span class="sxs-lookup"><span data-stu-id="0952b-177">3</span></span>     | <span data-ttu-id="0952b-178">/ifd/xmp/exif:ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="0952b-179">unicode</span><span class="sxs-lookup"><span data-stu-id="0952b-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0952b-180">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="0952b-180">Remove Paths</span></span>



| <span data-ttu-id="0952b-181">Pedido</span><span class="sxs-lookup"><span data-stu-id="0952b-181">Order</span></span> | <span data-ttu-id="0952b-182">Ruta</span><span class="sxs-lookup"><span data-stu-id="0952b-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0952b-183">1</span><span class="sxs-lookup"><span data-stu-id="0952b-183">1</span></span>     | <span data-ttu-id="0952b-184">/IFD/Exif/{ushort = 34850}</span><span class="sxs-lookup"><span data-stu-id="0952b-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="0952b-185">2</span><span class="sxs-lookup"><span data-stu-id="0952b-185">2</span></span>     | <span data-ttu-id="0952b-186">/ifd/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="0952b-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="0952b-187">3</span><span class="sxs-lookup"><span data-stu-id="0952b-187">3</span></span>     | <span data-ttu-id="0952b-188">/ifd/xmp/exif:programmode</span><span class="sxs-lookup"><span data-stu-id="0952b-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="0952b-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0952b-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0952b-190">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0952b-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0952b-191">System. Photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="0952b-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
