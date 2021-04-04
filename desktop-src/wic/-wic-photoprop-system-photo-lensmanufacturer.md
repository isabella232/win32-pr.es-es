---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Directiva de metadatos de la foto de System. Photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278188"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="f67fd-103">Directiva de metadatos de la foto de System. Photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="f67fd-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="f67fd-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="f67fd-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f67fd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f67fd-105">PKEY</span></span>

<span data-ttu-id="f67fd-106">PKEY \_ Photo \_ LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="f67fd-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="f67fd-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="f67fd-107">Containers</span></span>

<span data-ttu-id="f67fd-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f67fd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f67fd-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f67fd-109">Read-Only</span></span>

<span data-ttu-id="f67fd-110">No</span><span class="sxs-lookup"><span data-stu-id="f67fd-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f67fd-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="f67fd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f67fd-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="f67fd-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f67fd-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="f67fd-113">Input Type</span></span>

<span data-ttu-id="f67fd-114">String.</span><span class="sxs-lookup"><span data-stu-id="f67fd-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f67fd-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="f67fd-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f67fd-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="f67fd-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f67fd-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="f67fd-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f67fd-118">Si el archivo está en formato JPEG, el controlador usará la siguiente ruta de acceso al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="f67fd-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="f67fd-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="f67fd-119">Order</span></span> | <span data-ttu-id="f67fd-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="f67fd-120">Path</span></span>                                 | <span data-ttu-id="f67fd-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f67fd-121">Disk Format</span></span> | <span data-ttu-id="f67fd-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f67fd-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="f67fd-123">1</span><span class="sxs-lookup"><span data-stu-id="f67fd-123">1</span></span>     | <span data-ttu-id="f67fd-124">/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="f67fd-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="f67fd-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="f67fd-125">Unicode</span></span>     | <span data-ttu-id="f67fd-126">Sí</span><span class="sxs-lookup"><span data-stu-id="f67fd-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f67fd-127">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="f67fd-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f67fd-128">Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="f67fd-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="f67fd-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="f67fd-129">Order</span></span> | <span data-ttu-id="f67fd-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="f67fd-130">Path</span></span>                                     | <span data-ttu-id="f67fd-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f67fd-131">Disk Format</span></span> | <span data-ttu-id="f67fd-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f67fd-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="f67fd-133">1</span><span class="sxs-lookup"><span data-stu-id="f67fd-133">1</span></span>     | <span data-ttu-id="f67fd-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="f67fd-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="f67fd-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="f67fd-135">Unicode</span></span>     | <span data-ttu-id="f67fd-136">Sí</span><span class="sxs-lookup"><span data-stu-id="f67fd-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="f67fd-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f67fd-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f67fd-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f67fd-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f67fd-139">System. Photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="f67fd-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
