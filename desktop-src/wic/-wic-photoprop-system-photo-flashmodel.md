---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Directiva de metadatos de la foto de System. Photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716395"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a><span data-ttu-id="e1050-103">Directiva de metadatos de la foto de System. Photo. FlashModel</span><span class="sxs-lookup"><span data-stu-id="e1050-103">System.Photo.FlashModel Photo Metadata Policy</span></span>

<span data-ttu-id="e1050-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="e1050-104">The photo metadata policy for the [System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e1050-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e1050-105">PKEY</span></span>

<span data-ttu-id="e1050-106">PKEY \_ Photo \_ FlashModel</span><span class="sxs-lookup"><span data-stu-id="e1050-106">PKEY\_Photo\_FlashModel</span></span>

### <a name="containers"></a><span data-ttu-id="e1050-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="e1050-107">Containers</span></span>

<span data-ttu-id="e1050-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e1050-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e1050-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1050-109">Read-Only</span></span>

<span data-ttu-id="e1050-110">No</span><span class="sxs-lookup"><span data-stu-id="e1050-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e1050-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="e1050-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e1050-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="e1050-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="e1050-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="e1050-113">Input Type</span></span>

<span data-ttu-id="e1050-114">String.</span><span class="sxs-lookup"><span data-stu-id="e1050-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e1050-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="e1050-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e1050-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="e1050-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="e1050-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="e1050-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="e1050-118">Si el archivo está en formato JPEG, el controlador usará la siguiente ruta de acceso al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="e1050-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="e1050-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="e1050-119">Order</span></span> | <span data-ttu-id="e1050-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="e1050-120">Path</span></span>                           | <span data-ttu-id="e1050-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e1050-121">Disk Format</span></span> | <span data-ttu-id="e1050-122">Formato de datos</span><span class="sxs-lookup"><span data-stu-id="e1050-122">Data Format</span></span> | <span data-ttu-id="e1050-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e1050-123">Required</span></span> |
|-------|--------------------------------|-------------|-------------|----------|
| <span data-ttu-id="e1050-124">1</span><span class="sxs-lookup"><span data-stu-id="e1050-124">1</span></span>     | <span data-ttu-id="e1050-125">/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="e1050-125">/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="e1050-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="e1050-126">Unicode</span></span>     |             | <span data-ttu-id="e1050-127">Sí</span><span class="sxs-lookup"><span data-stu-id="e1050-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="e1050-128">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="e1050-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="e1050-129">Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="e1050-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="e1050-130">Pedido</span><span class="sxs-lookup"><span data-stu-id="e1050-130">Order</span></span> | <span data-ttu-id="e1050-131">Ruta</span><span class="sxs-lookup"><span data-stu-id="e1050-131">Path</span></span>                               | <span data-ttu-id="e1050-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e1050-132">Disk Format</span></span> | <span data-ttu-id="e1050-133">Formato de datos</span><span class="sxs-lookup"><span data-stu-id="e1050-133">Data Format</span></span> | <span data-ttu-id="e1050-134">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e1050-134">Required</span></span> |
|-------|------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="e1050-135">1</span><span class="sxs-lookup"><span data-stu-id="e1050-135">1</span></span>     | <span data-ttu-id="e1050-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="e1050-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="e1050-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="e1050-137">Unicode</span></span>     |             | <span data-ttu-id="e1050-138">Sí</span><span class="sxs-lookup"><span data-stu-id="e1050-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="e1050-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1050-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1050-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1050-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1050-141">System. Photo. FlashModel</span><span class="sxs-lookup"><span data-stu-id="e1050-141">System.Photo.FlashModel</span></span>](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
