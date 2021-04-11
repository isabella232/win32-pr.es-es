---
description: La Directiva de metadatos de la fotografía para la propiedad System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Directiva de metadatos de la foto System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083162"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="4d711-103">Directiva de metadatos de la foto System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="4d711-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="4d711-104">La Directiva de metadatos de la fotografía para la propiedad [System. SimpleRating](../properties/props-system-simplerating.md) .</span><span class="sxs-lookup"><span data-stu-id="4d711-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4d711-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4d711-105">PKEY</span></span>

<span data-ttu-id="4d711-106">PKEY \_ SimpleRating</span><span class="sxs-lookup"><span data-stu-id="4d711-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="4d711-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4d711-107">Containers</span></span>

<span data-ttu-id="4d711-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4d711-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4d711-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d711-109">Read-Only</span></span>

<span data-ttu-id="4d711-110">No</span><span class="sxs-lookup"><span data-stu-id="4d711-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4d711-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="4d711-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4d711-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="4d711-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4d711-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="4d711-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4d711-114">Puede ser VT \_ UI1, VT \_ UI2 o VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="4d711-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="4d711-115">El valor entero puede oscilar entre 0 y 5.</span><span class="sxs-lookup"><span data-stu-id="4d711-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4d711-116">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="4d711-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="4d711-117">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="4d711-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4d711-118">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="4d711-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4d711-119">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4d711-119">Read Paths</span></span>



| <span data-ttu-id="4d711-120">Pedido</span><span class="sxs-lookup"><span data-stu-id="4d711-120">Order</span></span> | <span data-ttu-id="4d711-121">Ruta</span><span class="sxs-lookup"><span data-stu-id="4d711-121">Path</span></span>                     | <span data-ttu-id="4d711-122">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4d711-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4d711-123">1</span><span class="sxs-lookup"><span data-stu-id="4d711-123">1</span></span>     | <span data-ttu-id="4d711-124">/app1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="4d711-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="4d711-125">ushort</span><span class="sxs-lookup"><span data-stu-id="4d711-125">ushort</span></span>      |
| <span data-ttu-id="4d711-126">2</span><span class="sxs-lookup"><span data-stu-id="4d711-126">2</span></span>     | <span data-ttu-id="4d711-127">/XMP/XMP: clasificación</span><span class="sxs-lookup"><span data-stu-id="4d711-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="4d711-128">unicode</span><span class="sxs-lookup"><span data-stu-id="4d711-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4d711-129">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4d711-129">Write Paths</span></span>



| <span data-ttu-id="4d711-130">Pedido</span><span class="sxs-lookup"><span data-stu-id="4d711-130">Order</span></span> | <span data-ttu-id="4d711-131">Ruta</span><span class="sxs-lookup"><span data-stu-id="4d711-131">Path</span></span>                     | <span data-ttu-id="4d711-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4d711-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4d711-133">1</span><span class="sxs-lookup"><span data-stu-id="4d711-133">1</span></span>     | <span data-ttu-id="4d711-134">/app1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="4d711-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="4d711-135">ushort</span><span class="sxs-lookup"><span data-stu-id="4d711-135">ushort</span></span>      |
| <span data-ttu-id="4d711-136">2</span><span class="sxs-lookup"><span data-stu-id="4d711-136">2</span></span>     | <span data-ttu-id="4d711-137">/XMP/XMP: clasificación</span><span class="sxs-lookup"><span data-stu-id="4d711-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="4d711-138">unicode</span><span class="sxs-lookup"><span data-stu-id="4d711-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4d711-139">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4d711-139">Remove Paths</span></span>



| <span data-ttu-id="4d711-140">Pedido</span><span class="sxs-lookup"><span data-stu-id="4d711-140">Order</span></span> | <span data-ttu-id="4d711-141">Ruta</span><span class="sxs-lookup"><span data-stu-id="4d711-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4d711-142">1</span><span class="sxs-lookup"><span data-stu-id="4d711-142">1</span></span>     | <span data-ttu-id="4d711-143">/app1/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="4d711-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="4d711-144">2</span><span class="sxs-lookup"><span data-stu-id="4d711-144">2</span></span>     | <span data-ttu-id="4d711-145">/XMP/XMP: clasificación</span><span class="sxs-lookup"><span data-stu-id="4d711-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="4d711-146">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="4d711-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4d711-147">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4d711-147">Read Paths</span></span>



| <span data-ttu-id="4d711-148">Pedido</span><span class="sxs-lookup"><span data-stu-id="4d711-148">Order</span></span> | <span data-ttu-id="4d711-149">Ruta</span><span class="sxs-lookup"><span data-stu-id="4d711-149">Path</span></span>                | <span data-ttu-id="4d711-150">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4d711-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="4d711-151">1</span><span class="sxs-lookup"><span data-stu-id="4d711-151">1</span></span>     | <span data-ttu-id="4d711-152">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="4d711-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="4d711-153">ushort</span><span class="sxs-lookup"><span data-stu-id="4d711-153">ushort</span></span>      |
| <span data-ttu-id="4d711-154">2</span><span class="sxs-lookup"><span data-stu-id="4d711-154">2</span></span>     | <span data-ttu-id="4d711-155">/IFD/XMP/XMP: clasificación</span><span class="sxs-lookup"><span data-stu-id="4d711-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="4d711-156">unicode</span><span class="sxs-lookup"><span data-stu-id="4d711-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4d711-157">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4d711-157">Write Paths</span></span>



| <span data-ttu-id="4d711-158">Pedido</span><span class="sxs-lookup"><span data-stu-id="4d711-158">Order</span></span> | <span data-ttu-id="4d711-159">Ruta</span><span class="sxs-lookup"><span data-stu-id="4d711-159">Path</span></span>                | <span data-ttu-id="4d711-160">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4d711-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="4d711-161">1</span><span class="sxs-lookup"><span data-stu-id="4d711-161">1</span></span>     | <span data-ttu-id="4d711-162">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="4d711-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="4d711-163">ushort</span><span class="sxs-lookup"><span data-stu-id="4d711-163">ushort</span></span>      |
| <span data-ttu-id="4d711-164">2</span><span class="sxs-lookup"><span data-stu-id="4d711-164">2</span></span>     | <span data-ttu-id="4d711-165">/IFD/XMP/XMP: clasificación</span><span class="sxs-lookup"><span data-stu-id="4d711-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="4d711-166">unicode</span><span class="sxs-lookup"><span data-stu-id="4d711-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4d711-167">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4d711-167">Remove Paths</span></span>



| <span data-ttu-id="4d711-168">Pedido</span><span class="sxs-lookup"><span data-stu-id="4d711-168">Order</span></span> | <span data-ttu-id="4d711-169">Ruta</span><span class="sxs-lookup"><span data-stu-id="4d711-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="4d711-170">1</span><span class="sxs-lookup"><span data-stu-id="4d711-170">1</span></span>     | <span data-ttu-id="4d711-171">/IFD/{ushort = 18246}</span><span class="sxs-lookup"><span data-stu-id="4d711-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="4d711-172">2</span><span class="sxs-lookup"><span data-stu-id="4d711-172">2</span></span>     | <span data-ttu-id="4d711-173">/IFD/XMP/XMP: clasificación</span><span class="sxs-lookup"><span data-stu-id="4d711-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4d711-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d711-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d711-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d711-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d711-176">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="4d711-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
