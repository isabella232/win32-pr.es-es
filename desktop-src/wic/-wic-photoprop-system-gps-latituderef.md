---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Directiva de metadatos de la foto System. GPS. LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278324"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a><span data-ttu-id="f7dca-103">Directiva de metadatos de la foto System. GPS. LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7dca-103">System.GPS.LatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="f7dca-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="f7dca-104">The photo metadata policy for the [System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f7dca-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f7dca-105">PKEY</span></span>

<span data-ttu-id="f7dca-106">PKEY \_ GPS \_ LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7dca-106">PKEY\_GPS\_LatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="f7dca-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="f7dca-107">Containers</span></span>

<span data-ttu-id="f7dca-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f7dca-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f7dca-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f7dca-109">Read-Only</span></span>

<span data-ttu-id="f7dca-110">No</span><span class="sxs-lookup"><span data-stu-id="f7dca-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f7dca-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="f7dca-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f7dca-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="f7dca-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f7dca-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="f7dca-113">Input Type</span></span>

<span data-ttu-id="f7dca-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="f7dca-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f7dca-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="f7dca-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f7dca-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="f7dca-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f7dca-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="f7dca-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f7dca-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="f7dca-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f7dca-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="f7dca-119">Order</span></span> | <span data-ttu-id="f7dca-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="f7dca-120">Path</span></span>                         | <span data-ttu-id="f7dca-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f7dca-121">Disk Format</span></span> | <span data-ttu-id="f7dca-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f7dca-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="f7dca-123">1</span><span class="sxs-lookup"><span data-stu-id="f7dca-123">1</span></span>     | <span data-ttu-id="f7dca-124">/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7dca-124">/xmp/exif:GPSLatitudeRef</span></span>     | <span data-ttu-id="f7dca-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="f7dca-125">Unicode</span></span>     | <span data-ttu-id="f7dca-126">Sí</span><span class="sxs-lookup"><span data-stu-id="f7dca-126">Yes</span></span>      |
| <span data-ttu-id="f7dca-127">2</span><span class="sxs-lookup"><span data-stu-id="f7dca-127">2</span></span>     | <span data-ttu-id="f7dca-128">/app1/IFD/GPS/ \\ {ushort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="f7dca-128">/app1/ifd/gps/\\{ushort=1\\}</span></span> | <span data-ttu-id="f7dca-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="f7dca-129">ASCII</span></span>       | <span data-ttu-id="f7dca-130">No</span><span class="sxs-lookup"><span data-stu-id="f7dca-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f7dca-131">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="f7dca-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f7dca-132">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="f7dca-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f7dca-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="f7dca-133">Order</span></span> | <span data-ttu-id="f7dca-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="f7dca-134">Path</span></span>                         | <span data-ttu-id="f7dca-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f7dca-135">Disk Format</span></span> | <span data-ttu-id="f7dca-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f7dca-136">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="f7dca-137">1</span><span class="sxs-lookup"><span data-stu-id="f7dca-137">1</span></span>     | <span data-ttu-id="f7dca-138">/ifd/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7dca-138">/ifd/xmp/exif:GPSLatitudeRef</span></span> | <span data-ttu-id="f7dca-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="f7dca-139">Unicode</span></span>     | <span data-ttu-id="f7dca-140">Sí</span><span class="sxs-lookup"><span data-stu-id="f7dca-140">Yes</span></span>      |
| <span data-ttu-id="f7dca-141">2</span><span class="sxs-lookup"><span data-stu-id="f7dca-141">2</span></span>     | <span data-ttu-id="f7dca-142">/IFD/GPS/ \\ {ushort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="f7dca-142">/ifd/gps/\\{ushort=1\\}</span></span>      | <span data-ttu-id="f7dca-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="f7dca-143">ASCII</span></span>       | <span data-ttu-id="f7dca-144">No</span><span class="sxs-lookup"><span data-stu-id="f7dca-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="f7dca-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7dca-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7dca-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7dca-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7dca-147">System. GPS. LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f7dca-147">System.GPS.LatitudeRef</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
