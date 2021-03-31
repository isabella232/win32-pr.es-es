---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Directiva de metadatos de la foto de System. Photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911945"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="6e543-103">Directiva de metadatos de la foto de System. Photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="6e543-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .</span><span class="sxs-lookup"><span data-stu-id="6e543-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6e543-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6e543-105">PKEY</span></span>

<span data-ttu-id="6e543-106">PKEY \_ Photo \_ TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="6e543-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="6e543-107">Containers</span></span>

<span data-ttu-id="6e543-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6e543-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6e543-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e543-109">Read-Only</span></span>

<span data-ttu-id="6e543-110">No</span><span class="sxs-lookup"><span data-stu-id="6e543-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6e543-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="6e543-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6e543-112">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="6e543-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="6e543-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="6e543-113">Input Type</span></span>

<span data-ttu-id="6e543-114">booleano.</span><span class="sxs-lookup"><span data-stu-id="6e543-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6e543-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="6e543-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6e543-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="6e543-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6e543-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="6e543-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6e543-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6e543-118">Read Paths</span></span>



| <span data-ttu-id="6e543-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="6e543-119">Order</span></span> | <span data-ttu-id="6e543-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="6e543-120">Path</span></span>                                  | <span data-ttu-id="6e543-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6e543-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="6e543-122">1</span><span class="sxs-lookup"><span data-stu-id="6e543-122">1</span></span>     | <span data-ttu-id="6e543-123">/app1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="6e543-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="6e543-124">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="6e543-124">bool\_ushort</span></span> |
| <span data-ttu-id="6e543-125">2</span><span class="sxs-lookup"><span data-stu-id="6e543-125">2</span></span>     | <span data-ttu-id="6e543-126">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="6e543-127">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6e543-127">Write Paths</span></span>



| <span data-ttu-id="6e543-128">Pedido</span><span class="sxs-lookup"><span data-stu-id="6e543-128">Order</span></span> | <span data-ttu-id="6e543-129">Ruta</span><span class="sxs-lookup"><span data-stu-id="6e543-129">Path</span></span>                                  | <span data-ttu-id="6e543-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6e543-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="6e543-131">1</span><span class="sxs-lookup"><span data-stu-id="6e543-131">1</span></span>     | <span data-ttu-id="6e543-132">/app1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="6e543-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="6e543-133">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="6e543-133">bool\_ushort</span></span> |
| <span data-ttu-id="6e543-134">2</span><span class="sxs-lookup"><span data-stu-id="6e543-134">2</span></span>     | <span data-ttu-id="6e543-135">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="6e543-136">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6e543-136">Remove Paths</span></span>



| <span data-ttu-id="6e543-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="6e543-137">Order</span></span> | <span data-ttu-id="6e543-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="6e543-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="6e543-139">1</span><span class="sxs-lookup"><span data-stu-id="6e543-139">1</span></span>     | <span data-ttu-id="6e543-140">/app1/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="6e543-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="6e543-141">2</span><span class="sxs-lookup"><span data-stu-id="6e543-141">2</span></span>     | <span data-ttu-id="6e543-142">/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="6e543-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="6e543-143">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="6e543-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6e543-144">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6e543-144">Read Paths</span></span>



| <span data-ttu-id="6e543-145">Pedido</span><span class="sxs-lookup"><span data-stu-id="6e543-145">Order</span></span> | <span data-ttu-id="6e543-146">Ruta</span><span class="sxs-lookup"><span data-stu-id="6e543-146">Path</span></span>                                      | <span data-ttu-id="6e543-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6e543-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="6e543-148">1</span><span class="sxs-lookup"><span data-stu-id="6e543-148">1</span></span>     | <span data-ttu-id="6e543-149">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="6e543-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="6e543-150">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="6e543-150">bool\_ushort</span></span> |
| <span data-ttu-id="6e543-151">2</span><span class="sxs-lookup"><span data-stu-id="6e543-151">2</span></span>     | <span data-ttu-id="6e543-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="6e543-153">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6e543-153">Write Paths</span></span>



| <span data-ttu-id="6e543-154">Pedido</span><span class="sxs-lookup"><span data-stu-id="6e543-154">Order</span></span> | <span data-ttu-id="6e543-155">Ruta</span><span class="sxs-lookup"><span data-stu-id="6e543-155">Path</span></span>                                      | <span data-ttu-id="6e543-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6e543-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="6e543-157">1</span><span class="sxs-lookup"><span data-stu-id="6e543-157">1</span></span>     | <span data-ttu-id="6e543-158">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="6e543-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="6e543-159">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="6e543-159">bool\_ushort</span></span> |
| <span data-ttu-id="6e543-160">2</span><span class="sxs-lookup"><span data-stu-id="6e543-160">2</span></span>     | <span data-ttu-id="6e543-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="6e543-162">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="6e543-162">Remove Paths</span></span>



| <span data-ttu-id="6e543-163">Pedido</span><span class="sxs-lookup"><span data-stu-id="6e543-163">Order</span></span> | <span data-ttu-id="6e543-164">Ruta</span><span class="sxs-lookup"><span data-stu-id="6e543-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="6e543-165">1</span><span class="sxs-lookup"><span data-stu-id="6e543-165">1</span></span>     | <span data-ttu-id="6e543-166">/IFD/{ushort = 18248}</span><span class="sxs-lookup"><span data-stu-id="6e543-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="6e543-167">2</span><span class="sxs-lookup"><span data-stu-id="6e543-167">2</span></span>     | <span data-ttu-id="6e543-168">/ifd/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="6e543-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6e543-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e543-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e543-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e543-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e543-171">System. Photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="6e543-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
