---
description: La Directiva de metadatos de la fotografía para la propiedad System. Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Directiva de metadatos de la foto System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361034"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="7dfae-103">Directiva de metadatos de la foto System. Rating</span><span class="sxs-lookup"><span data-stu-id="7dfae-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="7dfae-104">La Directiva de metadatos de la fotografía para la propiedad [System. Rating](../properties/props-system-rating.md) .</span><span class="sxs-lookup"><span data-stu-id="7dfae-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7dfae-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7dfae-105">PKEY</span></span>

<span data-ttu-id="7dfae-106">\_Clasificación PKEY</span><span class="sxs-lookup"><span data-stu-id="7dfae-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="7dfae-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="7dfae-107">Containers</span></span>

<span data-ttu-id="7dfae-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7dfae-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7dfae-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7dfae-109">Read-Only</span></span>

<span data-ttu-id="7dfae-110">No</span><span class="sxs-lookup"><span data-stu-id="7dfae-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7dfae-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="7dfae-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7dfae-112">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="7dfae-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="7dfae-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="7dfae-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="7dfae-114">Puede ser VT \_ UI1, VT \_ UI2 o VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="7dfae-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="7dfae-115">El valor puede oscilar entre 0 y 99.</span><span class="sxs-lookup"><span data-stu-id="7dfae-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7dfae-116">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="7dfae-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="7dfae-117">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="7dfae-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7dfae-118">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="7dfae-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7dfae-119">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7dfae-119">Read Paths</span></span>



| <span data-ttu-id="7dfae-120">Pedido</span><span class="sxs-lookup"><span data-stu-id="7dfae-120">Order</span></span> | <span data-ttu-id="7dfae-121">Ruta</span><span class="sxs-lookup"><span data-stu-id="7dfae-121">Path</span></span>                       | <span data-ttu-id="7dfae-122">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7dfae-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="7dfae-123">1</span><span class="sxs-lookup"><span data-stu-id="7dfae-123">1</span></span>     | <span data-ttu-id="7dfae-124">/app1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="7dfae-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="7dfae-125">ushort</span><span class="sxs-lookup"><span data-stu-id="7dfae-125">ushort</span></span>      |
| <span data-ttu-id="7dfae-126">2</span><span class="sxs-lookup"><span data-stu-id="7dfae-126">2</span></span>     | <span data-ttu-id="7dfae-127">/xmp/MicrosoftPhoto: clasificación</span><span class="sxs-lookup"><span data-stu-id="7dfae-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="7dfae-128">unicode</span><span class="sxs-lookup"><span data-stu-id="7dfae-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7dfae-129">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7dfae-129">Write Paths</span></span>



| <span data-ttu-id="7dfae-130">Pedido</span><span class="sxs-lookup"><span data-stu-id="7dfae-130">Order</span></span> | <span data-ttu-id="7dfae-131">Ruta</span><span class="sxs-lookup"><span data-stu-id="7dfae-131">Path</span></span>                       | <span data-ttu-id="7dfae-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7dfae-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="7dfae-133">1</span><span class="sxs-lookup"><span data-stu-id="7dfae-133">1</span></span>     | <span data-ttu-id="7dfae-134">/app1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="7dfae-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="7dfae-135">ushort</span><span class="sxs-lookup"><span data-stu-id="7dfae-135">ushort</span></span>      |
| <span data-ttu-id="7dfae-136">2</span><span class="sxs-lookup"><span data-stu-id="7dfae-136">2</span></span>     | <span data-ttu-id="7dfae-137">/xmp/MicrosoftPhoto: clasificación</span><span class="sxs-lookup"><span data-stu-id="7dfae-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="7dfae-138">unicode</span><span class="sxs-lookup"><span data-stu-id="7dfae-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7dfae-139">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7dfae-139">Remove Paths</span></span>



| <span data-ttu-id="7dfae-140">Pedido</span><span class="sxs-lookup"><span data-stu-id="7dfae-140">Order</span></span> | <span data-ttu-id="7dfae-141">Ruta</span><span class="sxs-lookup"><span data-stu-id="7dfae-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="7dfae-142">1</span><span class="sxs-lookup"><span data-stu-id="7dfae-142">1</span></span>     | <span data-ttu-id="7dfae-143">/app1/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="7dfae-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="7dfae-144">2</span><span class="sxs-lookup"><span data-stu-id="7dfae-144">2</span></span>     | <span data-ttu-id="7dfae-145">/XMP/microsoftphoto: clasificación</span><span class="sxs-lookup"><span data-stu-id="7dfae-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="7dfae-146">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="7dfae-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7dfae-147">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7dfae-147">Read Paths</span></span>



| <span data-ttu-id="7dfae-148">Pedido</span><span class="sxs-lookup"><span data-stu-id="7dfae-148">Order</span></span> | <span data-ttu-id="7dfae-149">Ruta</span><span class="sxs-lookup"><span data-stu-id="7dfae-149">Path</span></span>                           | <span data-ttu-id="7dfae-150">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7dfae-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="7dfae-151">1</span><span class="sxs-lookup"><span data-stu-id="7dfae-151">1</span></span>     | <span data-ttu-id="7dfae-152">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="7dfae-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="7dfae-153">ushort</span><span class="sxs-lookup"><span data-stu-id="7dfae-153">ushort</span></span>      |
| <span data-ttu-id="7dfae-154">2</span><span class="sxs-lookup"><span data-stu-id="7dfae-154">2</span></span>     | <span data-ttu-id="7dfae-155">/ifd/xmp/MicrosoftPhoto: clasificación</span><span class="sxs-lookup"><span data-stu-id="7dfae-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="7dfae-156">unicode</span><span class="sxs-lookup"><span data-stu-id="7dfae-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7dfae-157">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7dfae-157">Write Paths</span></span>



| <span data-ttu-id="7dfae-158">Pedido</span><span class="sxs-lookup"><span data-stu-id="7dfae-158">Order</span></span> | <span data-ttu-id="7dfae-159">Ruta</span><span class="sxs-lookup"><span data-stu-id="7dfae-159">Path</span></span>                           | <span data-ttu-id="7dfae-160">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7dfae-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="7dfae-161">1</span><span class="sxs-lookup"><span data-stu-id="7dfae-161">1</span></span>     | <span data-ttu-id="7dfae-162">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="7dfae-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="7dfae-163">ushort</span><span class="sxs-lookup"><span data-stu-id="7dfae-163">ushort</span></span>      |
| <span data-ttu-id="7dfae-164">2</span><span class="sxs-lookup"><span data-stu-id="7dfae-164">2</span></span>     | <span data-ttu-id="7dfae-165">/ifd/xmp/MicrosoftPhoto: clasificación</span><span class="sxs-lookup"><span data-stu-id="7dfae-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="7dfae-166">unicode</span><span class="sxs-lookup"><span data-stu-id="7dfae-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7dfae-167">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="7dfae-167">Remove Paths</span></span>



| <span data-ttu-id="7dfae-168">Pedido</span><span class="sxs-lookup"><span data-stu-id="7dfae-168">Order</span></span> | <span data-ttu-id="7dfae-169">Ruta</span><span class="sxs-lookup"><span data-stu-id="7dfae-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="7dfae-170">1</span><span class="sxs-lookup"><span data-stu-id="7dfae-170">1</span></span>     | <span data-ttu-id="7dfae-171">/IFD/{ushort = 18249}</span><span class="sxs-lookup"><span data-stu-id="7dfae-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="7dfae-172">2</span><span class="sxs-lookup"><span data-stu-id="7dfae-172">2</span></span>     | <span data-ttu-id="7dfae-173">/IFD/XMP/microsoftphoto: clasificación</span><span class="sxs-lookup"><span data-stu-id="7dfae-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7dfae-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7dfae-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dfae-175">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7dfae-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dfae-176">System. Rating</span><span class="sxs-lookup"><span data-stu-id="7dfae-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
