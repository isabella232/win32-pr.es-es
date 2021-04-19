---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Directiva de metadatos de la foto System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716785"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="a9243-103">Directiva de metadatos de la foto System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="a9243-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="a9243-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="a9243-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a9243-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a9243-105">PKEY</span></span>

<span data-ttu-id="a9243-106">PKEY \_ GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="a9243-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="a9243-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a9243-107">Containers</span></span>

<span data-ttu-id="a9243-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a9243-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a9243-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9243-109">Read-Only</span></span>

<span data-ttu-id="a9243-110">No</span><span class="sxs-lookup"><span data-stu-id="a9243-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a9243-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="a9243-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a9243-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="a9243-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="a9243-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="a9243-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="a9243-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="a9243-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a9243-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="a9243-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a9243-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="a9243-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="a9243-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="a9243-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="a9243-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="a9243-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="a9243-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="a9243-119">Order</span></span> | <span data-ttu-id="a9243-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="a9243-120">Path</span></span>                          | <span data-ttu-id="a9243-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a9243-121">Disk Format</span></span> | <span data-ttu-id="a9243-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a9243-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="a9243-123">1</span><span class="sxs-lookup"><span data-stu-id="a9243-123">1</span></span>     | <span data-ttu-id="a9243-124">/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="a9243-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="a9243-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="a9243-125">Unicode</span></span>     | <span data-ttu-id="a9243-126">Sí</span><span class="sxs-lookup"><span data-stu-id="a9243-126">Yes</span></span>      |
| <span data-ttu-id="a9243-127">2</span><span class="sxs-lookup"><span data-stu-id="a9243-127">2</span></span>     | <span data-ttu-id="a9243-128">/app1/IFD/GPS/ \\ {ushort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="a9243-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="a9243-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="a9243-129">ASCII</span></span>       | <span data-ttu-id="a9243-130">No</span><span class="sxs-lookup"><span data-stu-id="a9243-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="a9243-131">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="a9243-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="a9243-132">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="a9243-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="a9243-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="a9243-133">Order</span></span> | <span data-ttu-id="a9243-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="a9243-134">Path</span></span>                              | <span data-ttu-id="a9243-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a9243-135">Disk Format</span></span> | <span data-ttu-id="a9243-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a9243-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="a9243-137">1</span><span class="sxs-lookup"><span data-stu-id="a9243-137">1</span></span>     | <span data-ttu-id="a9243-138">/ifd/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="a9243-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="a9243-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="a9243-139">Unicode</span></span>     | <span data-ttu-id="a9243-140">Sí</span><span class="sxs-lookup"><span data-stu-id="a9243-140">Yes</span></span>      |
| <span data-ttu-id="a9243-141">2</span><span class="sxs-lookup"><span data-stu-id="a9243-141">2</span></span>     | <span data-ttu-id="a9243-142">/IFD/GPS/ \\ {ushort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="a9243-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="a9243-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="a9243-143">ASCII</span></span>       | <span data-ttu-id="a9243-144">No</span><span class="sxs-lookup"><span data-stu-id="a9243-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="a9243-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9243-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9243-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9243-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9243-147">System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="a9243-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
