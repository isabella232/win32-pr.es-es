---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Directiva de metadatos de la foto System. GPS. LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678368"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="bfb12-103">Directiva de metadatos de la foto System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="bfb12-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="bfb12-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb12-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bfb12-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bfb12-105">PKEY</span></span>

<span data-ttu-id="bfb12-106">PKEY \_ GPS \_ LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="bfb12-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="bfb12-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="bfb12-107">Containers</span></span>

<span data-ttu-id="bfb12-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bfb12-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bfb12-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfb12-109">Read-Only</span></span>

<span data-ttu-id="bfb12-110">No</span><span class="sxs-lookup"><span data-stu-id="bfb12-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="bfb12-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="bfb12-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="bfb12-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="bfb12-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="bfb12-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="bfb12-113">Input Type</span></span>

<span data-ttu-id="bfb12-114">String.</span><span class="sxs-lookup"><span data-stu-id="bfb12-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bfb12-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="bfb12-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="bfb12-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="bfb12-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="bfb12-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="bfb12-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="bfb12-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="bfb12-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="bfb12-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="bfb12-119">Order</span></span> | <span data-ttu-id="bfb12-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="bfb12-120">Path</span></span>                         | <span data-ttu-id="bfb12-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="bfb12-121">Disk Format</span></span> | <span data-ttu-id="bfb12-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfb12-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="bfb12-123">1</span><span class="sxs-lookup"><span data-stu-id="bfb12-123">1</span></span>     | <span data-ttu-id="bfb12-124">/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="bfb12-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="bfb12-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="bfb12-125">Unicode</span></span>     | <span data-ttu-id="bfb12-126">Sí</span><span class="sxs-lookup"><span data-stu-id="bfb12-126">Yes</span></span>      |
| <span data-ttu-id="bfb12-127">2</span><span class="sxs-lookup"><span data-stu-id="bfb12-127">2</span></span>     | <span data-ttu-id="bfb12-128">/app1/IFD/GPS/ \\ {ushort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="bfb12-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="bfb12-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="bfb12-129">ASCII</span></span>       | <span data-ttu-id="bfb12-130">No</span><span class="sxs-lookup"><span data-stu-id="bfb12-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="bfb12-131">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="bfb12-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="bfb12-132">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="bfb12-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="bfb12-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="bfb12-133">Order</span></span> | <span data-ttu-id="bfb12-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="bfb12-134">Path</span></span>                          | <span data-ttu-id="bfb12-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="bfb12-135">Disk Format</span></span> | <span data-ttu-id="bfb12-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bfb12-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="bfb12-137">1</span><span class="sxs-lookup"><span data-stu-id="bfb12-137">1</span></span>     | <span data-ttu-id="bfb12-138">/ifd/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="bfb12-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="bfb12-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="bfb12-139">Unicode</span></span>     | <span data-ttu-id="bfb12-140">Sí</span><span class="sxs-lookup"><span data-stu-id="bfb12-140">Yes</span></span>      |
| <span data-ttu-id="bfb12-141">2</span><span class="sxs-lookup"><span data-stu-id="bfb12-141">2</span></span>     | <span data-ttu-id="bfb12-142">/IFD/GPS/ \\ {ushort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="bfb12-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="bfb12-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="bfb12-143">ASCII</span></span>       | <span data-ttu-id="bfb12-144">No</span><span class="sxs-lookup"><span data-stu-id="bfb12-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="bfb12-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfb12-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfb12-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfb12-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfb12-147">System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="bfb12-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
