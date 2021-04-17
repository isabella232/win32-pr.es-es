---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. MakerNote.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Directiva de metadatos de la foto de System. Photo. MakerNote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677967"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a><span data-ttu-id="52835-103">Directiva de metadatos de la foto de System. Photo. MakerNote</span><span class="sxs-lookup"><span data-stu-id="52835-103">System.Photo.MakerNote Photo Metadata Policy</span></span>

<span data-ttu-id="52835-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. MakerNote](../properties/props-system-photo-makernote.md) .</span><span class="sxs-lookup"><span data-stu-id="52835-104">The photo metadata policy for the [System.Photo.MakerNote](../properties/props-system-photo-makernote.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="52835-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="52835-105">PKEY</span></span>

<span data-ttu-id="52835-106">PKEY \_ Photo \_ MakerNote</span><span class="sxs-lookup"><span data-stu-id="52835-106">PKEY\_Photo\_MakerNote</span></span>

### <a name="containers"></a><span data-ttu-id="52835-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="52835-107">Containers</span></span>

<span data-ttu-id="52835-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="52835-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="52835-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="52835-109">Read-Only</span></span>

<span data-ttu-id="52835-110">No</span><span class="sxs-lookup"><span data-stu-id="52835-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="52835-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="52835-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="52835-112">\_VTUI1 de vector de VT \|</span><span class="sxs-lookup"><span data-stu-id="52835-112">VT\_VECTOR \| VTUI1</span></span>

### <a name="input-type"></a><span data-ttu-id="52835-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="52835-113">Input Type</span></span>

<span data-ttu-id="52835-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="52835-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="52835-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="52835-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="52835-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="52835-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="52835-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="52835-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="52835-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="52835-118">Read Paths</span></span>



| <span data-ttu-id="52835-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="52835-119">Order</span></span> | <span data-ttu-id="52835-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="52835-120">Path</span></span>                          | <span data-ttu-id="52835-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="52835-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="52835-122">1</span><span class="sxs-lookup"><span data-stu-id="52835-122">1</span></span>     | <span data-ttu-id="52835-123">/app1/IFD/Exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="52835-123">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="52835-124">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="52835-124">Write Paths</span></span>



| <span data-ttu-id="52835-125">Pedido</span><span class="sxs-lookup"><span data-stu-id="52835-125">Order</span></span> | <span data-ttu-id="52835-126">Ruta</span><span class="sxs-lookup"><span data-stu-id="52835-126">Path</span></span>                          | <span data-ttu-id="52835-127">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="52835-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="52835-128">1</span><span class="sxs-lookup"><span data-stu-id="52835-128">1</span></span>     | <span data-ttu-id="52835-129">/app1/IFD/Exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="52835-129">/app1/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="52835-130">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="52835-130">Remove Paths</span></span>



| <span data-ttu-id="52835-131">Pedido</span><span class="sxs-lookup"><span data-stu-id="52835-131">Order</span></span> | <span data-ttu-id="52835-132">Ruta</span><span class="sxs-lookup"><span data-stu-id="52835-132">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="52835-133">1</span><span class="sxs-lookup"><span data-stu-id="52835-133">1</span></span>     | <span data-ttu-id="52835-134">/app1/IFD/Exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="52835-134">/app1/ifd/exif/{ushort=37500}</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="52835-135">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="52835-135">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="52835-136">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="52835-136">Read Paths</span></span>



| <span data-ttu-id="52835-137">Pedido</span><span class="sxs-lookup"><span data-stu-id="52835-137">Order</span></span> | <span data-ttu-id="52835-138">Ruta</span><span class="sxs-lookup"><span data-stu-id="52835-138">Path</span></span>                     | <span data-ttu-id="52835-139">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="52835-139">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="52835-140">1</span><span class="sxs-lookup"><span data-stu-id="52835-140">1</span></span>     | <span data-ttu-id="52835-141">/IFD/Exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="52835-141">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="52835-142">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="52835-142">Write Paths</span></span>



| <span data-ttu-id="52835-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="52835-143">Order</span></span> | <span data-ttu-id="52835-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="52835-144">Path</span></span>                     | <span data-ttu-id="52835-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="52835-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="52835-146">1</span><span class="sxs-lookup"><span data-stu-id="52835-146">1</span></span>     | <span data-ttu-id="52835-147">/IFD/Exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="52835-147">/ifd/exif/{ushort=37500}</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="52835-148">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="52835-148">Remove Paths</span></span>



| <span data-ttu-id="52835-149">Pedido</span><span class="sxs-lookup"><span data-stu-id="52835-149">Order</span></span> | <span data-ttu-id="52835-150">Ruta</span><span class="sxs-lookup"><span data-stu-id="52835-150">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="52835-151">1</span><span class="sxs-lookup"><span data-stu-id="52835-151">1</span></span>     | <span data-ttu-id="52835-152">/IFD/Exif/{ushort = 37500}</span><span class="sxs-lookup"><span data-stu-id="52835-152">/ifd/exif/{ushort=37500}</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="52835-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52835-153">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="52835-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="52835-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52835-155">System. Photo. MakerNote</span><span class="sxs-lookup"><span data-stu-id="52835-155">System.Photo.MakerNote</span></span>](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
