---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Directiva de metadatos de la foto System. GPS. DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687873"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="9ddb1-103">Directiva de metadatos de la foto System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="9ddb1-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="9ddb1-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="9ddb1-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9ddb1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9ddb1-105">PKEY</span></span>

<span data-ttu-id="9ddb1-106">PKEY \_ GPS \_ DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="9ddb1-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="9ddb1-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="9ddb1-107">Containers</span></span>

<span data-ttu-id="9ddb1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9ddb1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9ddb1-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9ddb1-109">Read-Only</span></span>

<span data-ttu-id="9ddb1-110">No</span><span class="sxs-lookup"><span data-stu-id="9ddb1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9ddb1-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="9ddb1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9ddb1-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="9ddb1-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="9ddb1-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="9ddb1-113">Input Type</span></span>

<span data-ttu-id="9ddb1-114">\_Se prefiere VT LPWStr, pero \_ se acepta VT LPSTR.</span><span class="sxs-lookup"><span data-stu-id="9ddb1-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9ddb1-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="9ddb1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9ddb1-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="9ddb1-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="9ddb1-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="9ddb1-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="9ddb1-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="9ddb1-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="9ddb1-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="9ddb1-119">Order</span></span> | <span data-ttu-id="9ddb1-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="9ddb1-120">Path</span></span>                          | <span data-ttu-id="9ddb1-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9ddb1-121">Disk Format</span></span> | <span data-ttu-id="9ddb1-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ddb1-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="9ddb1-123">1</span><span class="sxs-lookup"><span data-stu-id="9ddb1-123">1</span></span>     | <span data-ttu-id="9ddb1-124">/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="9ddb1-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="9ddb1-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="9ddb1-125">Unicode</span></span>     | <span data-ttu-id="9ddb1-126">Sí</span><span class="sxs-lookup"><span data-stu-id="9ddb1-126">Yes</span></span>      |
| <span data-ttu-id="9ddb1-127">2</span><span class="sxs-lookup"><span data-stu-id="9ddb1-127">2</span></span>     | <span data-ttu-id="9ddb1-128">/app1/IFD/GPS/ \\ {ushort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="9ddb1-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="9ddb1-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="9ddb1-129">ASCII</span></span>       | <span data-ttu-id="9ddb1-130">No</span><span class="sxs-lookup"><span data-stu-id="9ddb1-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="9ddb1-131">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="9ddb1-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="9ddb1-132">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="9ddb1-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="9ddb1-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="9ddb1-133">Order</span></span> | <span data-ttu-id="9ddb1-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="9ddb1-134">Path</span></span>                             | <span data-ttu-id="9ddb1-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9ddb1-135">Disk Format</span></span> | <span data-ttu-id="9ddb1-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ddb1-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="9ddb1-137">1</span><span class="sxs-lookup"><span data-stu-id="9ddb1-137">1</span></span>     | <span data-ttu-id="9ddb1-138">/ifd/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="9ddb1-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="9ddb1-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="9ddb1-139">Unicode</span></span>     | <span data-ttu-id="9ddb1-140">Sí</span><span class="sxs-lookup"><span data-stu-id="9ddb1-140">Yes</span></span>      |
| <span data-ttu-id="9ddb1-141">2</span><span class="sxs-lookup"><span data-stu-id="9ddb1-141">2</span></span>     | <span data-ttu-id="9ddb1-142">/IFD/GPS/ \\ {ushort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="9ddb1-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="9ddb1-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="9ddb1-143">ASCII</span></span>       | <span data-ttu-id="9ddb1-144">No</span><span class="sxs-lookup"><span data-stu-id="9ddb1-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="9ddb1-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ddb1-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ddb1-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9ddb1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ddb1-147">System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="9ddb1-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
