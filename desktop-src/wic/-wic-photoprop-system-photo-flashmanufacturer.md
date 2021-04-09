---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Directiva de metadatos de la foto de System. Photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083307"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="d806d-103">Directiva de metadatos de la foto de System. Photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="d806d-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="d806d-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="d806d-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d806d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d806d-105">PKEY</span></span>

<span data-ttu-id="d806d-106">PKEY \_ Photo \_ FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="d806d-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="d806d-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="d806d-107">Containers</span></span>

<span data-ttu-id="d806d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d806d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d806d-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d806d-109">Read-Only</span></span>

<span data-ttu-id="d806d-110">No</span><span class="sxs-lookup"><span data-stu-id="d806d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d806d-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="d806d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d806d-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="d806d-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="d806d-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="d806d-113">Input Type</span></span>

<span data-ttu-id="d806d-114">String.</span><span class="sxs-lookup"><span data-stu-id="d806d-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d806d-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="d806d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d806d-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="d806d-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="d806d-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="d806d-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="d806d-118">Si el archivo está en formato JPEG, el controlador usará la siguiente ruta de acceso al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="d806d-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="d806d-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="d806d-119">Order</span></span> | <span data-ttu-id="d806d-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="d806d-120">Path</span></span>                                  | <span data-ttu-id="d806d-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d806d-121">Disk Format</span></span> | <span data-ttu-id="d806d-122">Formato de datos</span><span class="sxs-lookup"><span data-stu-id="d806d-122">Data Format</span></span> | <span data-ttu-id="d806d-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d806d-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="d806d-124">1</span><span class="sxs-lookup"><span data-stu-id="d806d-124">1</span></span>     | <span data-ttu-id="d806d-125">/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="d806d-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="d806d-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="d806d-126">Unicode</span></span>     |             | <span data-ttu-id="d806d-127">Sí</span><span class="sxs-lookup"><span data-stu-id="d806d-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="d806d-128">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="d806d-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="d806d-129">Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="d806d-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="d806d-130">Pedido</span><span class="sxs-lookup"><span data-stu-id="d806d-130">Order</span></span> | <span data-ttu-id="d806d-131">Ruta</span><span class="sxs-lookup"><span data-stu-id="d806d-131">Path</span></span>                                      | <span data-ttu-id="d806d-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d806d-132">Disk Format</span></span> | <span data-ttu-id="d806d-133">Formato de datos</span><span class="sxs-lookup"><span data-stu-id="d806d-133">Data Format</span></span> | <span data-ttu-id="d806d-134">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d806d-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="d806d-135">1</span><span class="sxs-lookup"><span data-stu-id="d806d-135">1</span></span>     | <span data-ttu-id="d806d-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="d806d-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="d806d-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="d806d-137">Unicode</span></span>     |             | <span data-ttu-id="d806d-138">Sí</span><span class="sxs-lookup"><span data-stu-id="d806d-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="d806d-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d806d-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d806d-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d806d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d806d-141">System. Photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="d806d-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
