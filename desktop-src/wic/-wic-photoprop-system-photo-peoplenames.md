---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Directiva de metadatos de la foto de System. Photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678225"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a><span data-ttu-id="4bcd4-103">Directiva de metadatos de la foto de System. Photo. PeopleNames</span><span class="sxs-lookup"><span data-stu-id="4bcd4-103">System.Photo.PeopleNames Photo Metadata Policy</span></span>

<span data-ttu-id="4bcd4-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="4bcd4-104">The photo metadata policy for the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4bcd4-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4bcd4-105">PKEY</span></span>

<span data-ttu-id="4bcd4-106">PKEY \_ Photo \_ PeopleNames</span><span class="sxs-lookup"><span data-stu-id="4bcd4-106">PKEY\_Photo\_PeopleNames</span></span>

### <a name="containers"></a><span data-ttu-id="4bcd4-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="4bcd4-107">Containers</span></span>

<span data-ttu-id="4bcd4-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4bcd4-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4bcd4-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4bcd4-109">Read-Only</span></span>

<span data-ttu-id="4bcd4-110">No</span><span class="sxs-lookup"><span data-stu-id="4bcd4-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4bcd4-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="4bcd4-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4bcd4-112">VT \_ Vector \| VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="4bcd4-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4bcd4-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="4bcd4-113">Input Type</span></span>

<span data-ttu-id="4bcd4-114">StringMulti</span><span class="sxs-lookup"><span data-stu-id="4bcd4-114">StringMulti</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4bcd4-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="4bcd4-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4bcd4-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="4bcd4-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="4bcd4-117">Directiva JPEG</span><span class="sxs-lookup"><span data-stu-id="4bcd4-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="4bcd4-118">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bcd4-118">Read Paths</span></span>



| <span data-ttu-id="4bcd4-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bcd4-119">Order</span></span> | <span data-ttu-id="4bcd4-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bcd4-120">Path</span></span>                                                           | <span data-ttu-id="4bcd4-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4bcd4-121">Disk Format</span></span> |
|-------|----------------------------------------------------------------|-------------|
| <span data-ttu-id="4bcd4-122">1</span><span class="sxs-lookup"><span data-stu-id="4bcd4-122">1</span></span>     | <span data-ttu-id="4bcd4-123">módulo de administración de/XMP/ <xmpstruct> : RegionInfo/ <xmpbag> mpri: regiones</span><span class="sxs-lookup"><span data-stu-id="4bcd4-123">/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="4bcd4-124">ushort</span><span class="sxs-lookup"><span data-stu-id="4bcd4-124">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="4bcd4-125">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bcd4-125">Write Paths</span></span>

<span data-ttu-id="4bcd4-126">Esta propiedad no se puede escribir con la Directiva de metadatos.</span><span class="sxs-lookup"><span data-stu-id="4bcd4-126">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="4bcd4-127">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bcd4-127">Remove Paths</span></span>



| <span data-ttu-id="4bcd4-128">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bcd4-128">Order</span></span> | <span data-ttu-id="4bcd4-129">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bcd4-129">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="4bcd4-130">1</span><span class="sxs-lookup"><span data-stu-id="4bcd4-130">1</span></span>     | <span data-ttu-id="4bcd4-131">módulo de administración de/XMP/ <xmpstruct> : RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4bcd4-131">/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="4bcd4-132">Directivas TIFF</span><span class="sxs-lookup"><span data-stu-id="4bcd4-132">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4bcd4-133">Leer rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bcd4-133">Read Paths</span></span>



| <span data-ttu-id="4bcd4-134">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bcd4-134">Order</span></span> | <span data-ttu-id="4bcd4-135">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bcd4-135">Path</span></span>                                                               | <span data-ttu-id="4bcd4-136">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4bcd4-136">Disk Format</span></span> |
|-------|--------------------------------------------------------------------|-------------|
| <span data-ttu-id="4bcd4-137">1</span><span class="sxs-lookup"><span data-stu-id="4bcd4-137">1</span></span>     | <span data-ttu-id="4bcd4-138">módulo de administración de/IFD/XMP/ <xmpstruct> : RegionInfo/ <xmpbag> mpri: regiones</span><span class="sxs-lookup"><span data-stu-id="4bcd4-138">/ifd/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="4bcd4-139">ushort</span><span class="sxs-lookup"><span data-stu-id="4bcd4-139">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="4bcd4-140">Escribir rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bcd4-140">Write Paths</span></span>

<span data-ttu-id="4bcd4-141">Esta propiedad no se puede escribir con la Directiva de metadatos.</span><span class="sxs-lookup"><span data-stu-id="4bcd4-141">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="4bcd4-142">Quitar rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="4bcd4-142">Remove Paths</span></span>



| <span data-ttu-id="4bcd4-143">Pedido</span><span class="sxs-lookup"><span data-stu-id="4bcd4-143">Order</span></span> | <span data-ttu-id="4bcd4-144">Ruta</span><span class="sxs-lookup"><span data-stu-id="4bcd4-144">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="4bcd4-145">1</span><span class="sxs-lookup"><span data-stu-id="4bcd4-145">1</span></span>     | <span data-ttu-id="4bcd4-146">módulo de administración de/IFD/XMP/ <xmpstruct> : RegionInfo</span><span class="sxs-lookup"><span data-stu-id="4bcd4-146">/ifd/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4bcd4-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bcd4-147">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bcd4-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4bcd4-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bcd4-149">System. Photo. ProgramMode</span><span class="sxs-lookup"><span data-stu-id="4bcd4-149">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
