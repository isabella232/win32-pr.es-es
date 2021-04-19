---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Directiva de metadatos de la foto System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678367"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="f826a-103">Directiva de metadatos de la foto System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="f826a-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="f826a-104">La Directiva de metadatos de la fotografía para la propiedad [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .</span><span class="sxs-lookup"><span data-stu-id="f826a-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f826a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f826a-105">PKEY</span></span>

<span data-ttu-id="f826a-106">PKEY \_ GPS \_ MapDatum</span><span class="sxs-lookup"><span data-stu-id="f826a-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="f826a-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="f826a-107">Containers</span></span>

<span data-ttu-id="f826a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f826a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f826a-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f826a-109">Read-Only</span></span>

<span data-ttu-id="f826a-110">No</span><span class="sxs-lookup"><span data-stu-id="f826a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f826a-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="f826a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f826a-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="f826a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f826a-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="f826a-113">Input Type</span></span>

<span data-ttu-id="f826a-114">\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR</span><span class="sxs-lookup"><span data-stu-id="f826a-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f826a-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="f826a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f826a-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="f826a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f826a-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="f826a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f826a-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="f826a-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f826a-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="f826a-119">Order</span></span> | <span data-ttu-id="f826a-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="f826a-120">Path</span></span>                          | <span data-ttu-id="f826a-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f826a-121">Disk Format</span></span> | <span data-ttu-id="f826a-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f826a-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="f826a-123">1</span><span class="sxs-lookup"><span data-stu-id="f826a-123">1</span></span>     | <span data-ttu-id="f826a-124">/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="f826a-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="f826a-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="f826a-125">Unicode</span></span>     | <span data-ttu-id="f826a-126">Sí</span><span class="sxs-lookup"><span data-stu-id="f826a-126">Yes</span></span>      |
| <span data-ttu-id="f826a-127">2</span><span class="sxs-lookup"><span data-stu-id="f826a-127">2</span></span>     | <span data-ttu-id="f826a-128">/app1/IFD/GPS/ \\ {ushort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="f826a-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="f826a-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="f826a-129">ASCII</span></span>       | <span data-ttu-id="f826a-130">No</span><span class="sxs-lookup"><span data-stu-id="f826a-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f826a-131">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="f826a-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f826a-132">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="f826a-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f826a-133">Pedido</span><span class="sxs-lookup"><span data-stu-id="f826a-133">Order</span></span> | <span data-ttu-id="f826a-134">Ruta</span><span class="sxs-lookup"><span data-stu-id="f826a-134">Path</span></span>                      | <span data-ttu-id="f826a-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f826a-135">Disk Format</span></span> | <span data-ttu-id="f826a-136">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f826a-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="f826a-137">1</span><span class="sxs-lookup"><span data-stu-id="f826a-137">1</span></span>     | <span data-ttu-id="f826a-138">/ifd/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="f826a-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="f826a-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="f826a-139">Unicode</span></span>     | <span data-ttu-id="f826a-140">Sí</span><span class="sxs-lookup"><span data-stu-id="f826a-140">Yes</span></span>      |
| <span data-ttu-id="f826a-141">2</span><span class="sxs-lookup"><span data-stu-id="f826a-141">2</span></span>     | <span data-ttu-id="f826a-142">/IFD/GPS/ \\ {ushort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="f826a-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="f826a-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="f826a-143">ASCII</span></span>       | <span data-ttu-id="f826a-144">No</span><span class="sxs-lookup"><span data-stu-id="f826a-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="f826a-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f826a-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f826a-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f826a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f826a-147">System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="f826a-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
