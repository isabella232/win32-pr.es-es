---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Directiva de metadatos de la foto de System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083168"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="dff17-103">Directiva de metadatos de la foto de System. Photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="dff17-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="dff17-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="dff17-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="dff17-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="dff17-105">PKEY</span></span>

<span data-ttu-id="dff17-106">PKEY \_ Photo \_ LensModel</span><span class="sxs-lookup"><span data-stu-id="dff17-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="dff17-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="dff17-107">Containers</span></span>

<span data-ttu-id="dff17-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="dff17-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="dff17-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dff17-109">Read-Only</span></span>

<span data-ttu-id="dff17-110">No</span><span class="sxs-lookup"><span data-stu-id="dff17-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="dff17-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="dff17-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="dff17-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="dff17-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="dff17-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="dff17-113">Input Type</span></span>

<span data-ttu-id="dff17-114">String.</span><span class="sxs-lookup"><span data-stu-id="dff17-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="dff17-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="dff17-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="dff17-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="dff17-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="dff17-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="dff17-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="dff17-118">Si el archivo está en formato JPEG, el controlador usará la siguiente ruta de acceso al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="dff17-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="dff17-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="dff17-119">Order</span></span> | <span data-ttu-id="dff17-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="dff17-120">Path</span></span>                          | <span data-ttu-id="dff17-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="dff17-121">Disk Format</span></span> | <span data-ttu-id="dff17-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dff17-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="dff17-123">1</span><span class="sxs-lookup"><span data-stu-id="dff17-123">1</span></span>     | <span data-ttu-id="dff17-124">/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="dff17-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="dff17-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="dff17-125">Unicode</span></span>     | <span data-ttu-id="dff17-126">Sí</span><span class="sxs-lookup"><span data-stu-id="dff17-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="dff17-127">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="dff17-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="dff17-128">Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="dff17-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="dff17-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="dff17-129">Order</span></span> | <span data-ttu-id="dff17-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="dff17-130">Path</span></span>                              | <span data-ttu-id="dff17-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="dff17-131">Disk Format</span></span> | <span data-ttu-id="dff17-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dff17-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="dff17-133">1</span><span class="sxs-lookup"><span data-stu-id="dff17-133">1</span></span>     | <span data-ttu-id="dff17-134">/ifd/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="dff17-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="dff17-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="dff17-135">Unicode</span></span>     | <span data-ttu-id="dff17-136">Sí</span><span class="sxs-lookup"><span data-stu-id="dff17-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="dff17-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dff17-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="dff17-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dff17-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dff17-139">System. Photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="dff17-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
