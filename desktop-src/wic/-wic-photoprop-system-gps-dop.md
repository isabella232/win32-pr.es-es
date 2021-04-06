---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Directiva de metadatos de foto de System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002874"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="3cbdd-103">Directiva de metadatos de foto de System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="3cbdd-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="3cbdd-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DOP](../properties/props-system-gps-dop.md) .</span><span class="sxs-lookup"><span data-stu-id="3cbdd-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3cbdd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3cbdd-105">PKEY</span></span>

<span data-ttu-id="3cbdd-106">PKEY \_ GPS \_ DOP</span><span class="sxs-lookup"><span data-stu-id="3cbdd-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="3cbdd-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="3cbdd-107">Containers</span></span>

<span data-ttu-id="3cbdd-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3cbdd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3cbdd-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cbdd-109">Read-Only</span></span>

<span data-ttu-id="3cbdd-110">Sí</span><span class="sxs-lookup"><span data-stu-id="3cbdd-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3cbdd-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="3cbdd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3cbdd-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="3cbdd-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3cbdd-113">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="3cbdd-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="3cbdd-114">Este valor se puede escribir escribiendo en System. GPS. DOPNumerator y System. GPS. DOPDenominator.</span><span class="sxs-lookup"><span data-stu-id="3cbdd-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="3cbdd-115">No se puede escribir directamente.</span><span class="sxs-lookup"><span data-stu-id="3cbdd-115">It cannot be written directly.</span></span> <span data-ttu-id="3cbdd-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="3cbdd-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="3cbdd-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="3cbdd-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="3cbdd-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="3cbdd-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="3cbdd-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="3cbdd-119">Order</span></span> | <span data-ttu-id="3cbdd-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="3cbdd-120">Path</span></span>                          | <span data-ttu-id="3cbdd-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3cbdd-121">Disk Format</span></span>   | <span data-ttu-id="3cbdd-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3cbdd-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="3cbdd-123">1</span><span class="sxs-lookup"><span data-stu-id="3cbdd-123">1</span></span>     | <span data-ttu-id="3cbdd-124">/xmp/exif:GPSDOP</span><span class="sxs-lookup"><span data-stu-id="3cbdd-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="3cbdd-125">XMP Rational</span><span class="sxs-lookup"><span data-stu-id="3cbdd-125">XMP rational</span></span>  | <span data-ttu-id="3cbdd-126">Sí</span><span class="sxs-lookup"><span data-stu-id="3cbdd-126">Yes</span></span>      |
| <span data-ttu-id="3cbdd-127">2</span><span class="sxs-lookup"><span data-stu-id="3cbdd-127">2</span></span>     | <span data-ttu-id="3cbdd-128">/app1/IFD/GPS/ \\ {ushort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="3cbdd-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="3cbdd-129">Racional EXIF</span><span class="sxs-lookup"><span data-stu-id="3cbdd-129">EXIF rational</span></span> | <span data-ttu-id="3cbdd-130">No</span><span class="sxs-lookup"><span data-stu-id="3cbdd-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="3cbdd-131">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="3cbdd-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="3cbdd-132">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="3cbdd-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="3cbdd-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="3cbdd-133">Order</span></span> | <span data-ttu-id="3cbdd-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="3cbdd-134">Path</span></span>                     | <span data-ttu-id="3cbdd-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3cbdd-135">Disk Format</span></span>   | <span data-ttu-id="3cbdd-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3cbdd-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="3cbdd-137">1</span><span class="sxs-lookup"><span data-stu-id="3cbdd-137">1</span></span>     | <span data-ttu-id="3cbdd-138">/ifd/xmp/exif:GPSDop</span><span class="sxs-lookup"><span data-stu-id="3cbdd-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="3cbdd-139">XMP Rational</span><span class="sxs-lookup"><span data-stu-id="3cbdd-139">XMP rational</span></span>  | <span data-ttu-id="3cbdd-140">Sí</span><span class="sxs-lookup"><span data-stu-id="3cbdd-140">Yes</span></span>      |
| <span data-ttu-id="3cbdd-141">2</span><span class="sxs-lookup"><span data-stu-id="3cbdd-141">2</span></span>     | <span data-ttu-id="3cbdd-142">/IFD/GPS/ \\ {ushort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="3cbdd-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="3cbdd-143">Racional EXIF</span><span class="sxs-lookup"><span data-stu-id="3cbdd-143">EXIF rational</span></span> | <span data-ttu-id="3cbdd-144">No</span><span class="sxs-lookup"><span data-stu-id="3cbdd-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="3cbdd-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cbdd-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cbdd-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cbdd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbdd-147">System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="3cbdd-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
