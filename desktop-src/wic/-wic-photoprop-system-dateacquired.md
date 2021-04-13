---
description: La Directiva de metadatos de la fotografía para la propiedad System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Directiva de metadatos de la foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278840"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="e38cd-103">Directiva de metadatos de la foto System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="e38cd-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="e38cd-104">La Directiva de metadatos de la fotografía para la propiedad [System. DateAcquired](../properties/props-system-dateacquired.md) .</span><span class="sxs-lookup"><span data-stu-id="e38cd-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e38cd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e38cd-105">PKEY</span></span>

<span data-ttu-id="e38cd-106">PKEY \_ DateAcquired</span><span class="sxs-lookup"><span data-stu-id="e38cd-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="e38cd-107">Contenedores</span><span class="sxs-lookup"><span data-stu-id="e38cd-107">Containers</span></span>

<span data-ttu-id="e38cd-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e38cd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e38cd-109">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e38cd-109">Read-Only</span></span>

<span data-ttu-id="e38cd-110">No</span><span class="sxs-lookup"><span data-stu-id="e38cd-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e38cd-111">Tipo de PROPVARIANT de salida</span><span class="sxs-lookup"><span data-stu-id="e38cd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e38cd-112">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="e38cd-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="e38cd-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="e38cd-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="e38cd-114">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="e38cd-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e38cd-115">Directiva de resolución de conflictos</span><span class="sxs-lookup"><span data-stu-id="e38cd-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e38cd-116">Se reconcilian los valores de los distintos esquemas.</span><span class="sxs-lookup"><span data-stu-id="e38cd-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="e38cd-117">Prioridad de las rutas de acceso (JPEG)</span><span class="sxs-lookup"><span data-stu-id="e38cd-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="e38cd-118">Si el archivo está en formato JPEG, el controlador busca los datos en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="e38cd-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="e38cd-119">Pedido</span><span class="sxs-lookup"><span data-stu-id="e38cd-119">Order</span></span> | <span data-ttu-id="e38cd-120">Ruta</span><span class="sxs-lookup"><span data-stu-id="e38cd-120">Path</span></span>                             | <span data-ttu-id="e38cd-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e38cd-121">Disk Format</span></span>                        | <span data-ttu-id="e38cd-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e38cd-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="e38cd-123">1</span><span class="sxs-lookup"><span data-stu-id="e38cd-123">1</span></span>     | <span data-ttu-id="e38cd-124">/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="e38cd-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="e38cd-125">Cadena Unicode en formato de fecha XMP.</span><span class="sxs-lookup"><span data-stu-id="e38cd-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="e38cd-126">Sí</span><span class="sxs-lookup"><span data-stu-id="e38cd-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="e38cd-127">Prioridad de las rutas de acceso (TIFF)</span><span class="sxs-lookup"><span data-stu-id="e38cd-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="e38cd-128">Si el archivo está en formato TIFF, el controlador busca los datos en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="e38cd-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="e38cd-129">Pedido</span><span class="sxs-lookup"><span data-stu-id="e38cd-129">Order</span></span> | <span data-ttu-id="e38cd-130">Ruta</span><span class="sxs-lookup"><span data-stu-id="e38cd-130">Path</span></span>                                 | <span data-ttu-id="e38cd-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e38cd-131">Disk Format</span></span>                        | <span data-ttu-id="e38cd-132">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e38cd-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="e38cd-133">1</span><span class="sxs-lookup"><span data-stu-id="e38cd-133">1</span></span>     | <span data-ttu-id="e38cd-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="e38cd-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="e38cd-135">Cadena Unicode en formato de fecha XMP.</span><span class="sxs-lookup"><span data-stu-id="e38cd-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="e38cd-136">Sí</span><span class="sxs-lookup"><span data-stu-id="e38cd-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="e38cd-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e38cd-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e38cd-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e38cd-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e38cd-139">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="e38cd-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
