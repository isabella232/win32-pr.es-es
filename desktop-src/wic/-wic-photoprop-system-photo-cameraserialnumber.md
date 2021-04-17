---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Directiva de metadatos de la foto de System. Photo. CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688384"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="a578a-103">Directiva de metadatos de la foto de System. Photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a578a-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="a578a-104">La Directiva de metadatos de fotos para la propiedad [System. Photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="a578a-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a578a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a578a-105">PKEY</span></span>

<span data-ttu-id="a578a-106">PKEY \_ Photo \_ CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a578a-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="a578a-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="a578a-107">Containers</span></span>

<span data-ttu-id="a578a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a578a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a578a-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a578a-109">Read-Only</span></span>

<span data-ttu-id="a578a-110">No</span><span class="sxs-lookup"><span data-stu-id="a578a-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a578a-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="a578a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a578a-112">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="a578a-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a578a-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a578a-113">Input Type</span></span>

<span data-ttu-id="a578a-114">String.</span><span class="sxs-lookup"><span data-stu-id="a578a-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a578a-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="a578a-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a578a-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="a578a-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="a578a-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="a578a-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="a578a-118">Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos de la siguiente ruta de acceso:</span><span class="sxs-lookup"><span data-stu-id="a578a-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="a578a-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="a578a-119">Order</span></span> | <span data-ttu-id="a578a-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="a578a-120">Path</span></span>                                   | <span data-ttu-id="a578a-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a578a-121">Disk Format</span></span> | <span data-ttu-id="a578a-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a578a-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="a578a-123">1</span><span class="sxs-lookup"><span data-stu-id="a578a-123">1</span></span>     | <span data-ttu-id="a578a-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a578a-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="a578a-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="a578a-125">Unicode</span></span>     | <span data-ttu-id="a578a-126">Sí</span><span class="sxs-lookup"><span data-stu-id="a578a-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="a578a-127">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="a578a-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="a578a-128">Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos de la siguiente ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a578a-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="a578a-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="a578a-129">Order</span></span> | <span data-ttu-id="a578a-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="a578a-130">Path</span></span>                                       | <span data-ttu-id="a578a-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a578a-131">Disk Format</span></span> | <span data-ttu-id="a578a-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a578a-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="a578a-133">1</span><span class="sxs-lookup"><span data-stu-id="a578a-133">1</span></span>     | <span data-ttu-id="a578a-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a578a-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="a578a-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="a578a-135">Unicode</span></span>     | <span data-ttu-id="a578a-136">Sí</span><span class="sxs-lookup"><span data-stu-id="a578a-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="a578a-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a578a-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a578a-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a578a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a578a-139">System. Photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="a578a-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
