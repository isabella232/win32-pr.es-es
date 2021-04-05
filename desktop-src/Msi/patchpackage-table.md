---
description: La tabla PatchPackage describe todos los paquetes de revisiones que se han aplicado a este producto. Para cada paquete de revisión, se proporciona el identificador único de la revisión junto con información sobre la imagen multimedia en la que se encuentra la revisión.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabla PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279328"
---
# <a name="patchpackage-table"></a><span data-ttu-id="5eccb-104">Tabla PatchPackage</span><span class="sxs-lookup"><span data-stu-id="5eccb-104">PatchPackage Table</span></span>

<span data-ttu-id="5eccb-105">La tabla PatchPackage describe todos los paquetes de revisiones que se han aplicado a este producto.</span><span class="sxs-lookup"><span data-stu-id="5eccb-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="5eccb-106">Para cada paquete de revisión, se proporciona el identificador único de la revisión junto con información sobre la imagen multimedia en la que se encuentra la revisión.</span><span class="sxs-lookup"><span data-stu-id="5eccb-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="5eccb-107">La tabla PatchPackage tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="5eccb-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="5eccb-108">Columna</span><span class="sxs-lookup"><span data-stu-id="5eccb-108">Column</span></span>  | <span data-ttu-id="5eccb-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5eccb-109">Type</span></span>                   | <span data-ttu-id="5eccb-110">Clave</span><span class="sxs-lookup"><span data-stu-id="5eccb-110">Key</span></span> | <span data-ttu-id="5eccb-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5eccb-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="5eccb-112">PatchId</span><span class="sxs-lookup"><span data-stu-id="5eccb-112">PatchId</span></span> | [<span data-ttu-id="5eccb-113">GUID</span><span class="sxs-lookup"><span data-stu-id="5eccb-113">GUID</span></span>](guid.md)       | <span data-ttu-id="5eccb-114">Y</span><span class="sxs-lookup"><span data-stu-id="5eccb-114">Y</span></span>   | <span data-ttu-id="5eccb-115">N</span><span class="sxs-lookup"><span data-stu-id="5eccb-115">N</span></span>        |
| <span data-ttu-id="5eccb-116">Medios\_</span><span class="sxs-lookup"><span data-stu-id="5eccb-116">Media\_</span></span> | [<span data-ttu-id="5eccb-117">Entero</span><span class="sxs-lookup"><span data-stu-id="5eccb-117">Integer</span></span>](integer.md) | <span data-ttu-id="5eccb-118">N</span><span class="sxs-lookup"><span data-stu-id="5eccb-118">N</span></span>   | <span data-ttu-id="5eccb-119">N</span><span class="sxs-lookup"><span data-stu-id="5eccb-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5eccb-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="5eccb-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5eccb-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span><span class="sxs-lookup"><span data-stu-id="5eccb-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="5eccb-122">Esta columna contiene un identificador único para esta revisión en particular.</span><span class="sxs-lookup"><span data-stu-id="5eccb-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="5eccb-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Soporte\_</span><span class="sxs-lookup"><span data-stu-id="5eccb-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="5eccb-124">Esta columna es una clave externa de la columna de dipatine de la [tabla de medios](media-table.md) e indica el disco que contiene el paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="5eccb-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5eccb-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5eccb-125">Remarks</span></span>

<span data-ttu-id="5eccb-126">La tabla PatchPackage es necesaria en cada paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="5eccb-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="5eccb-127">Si falta la tabla, se producirá un error en los intentos de instalación de la revisión con el mensaje "error 2768: la transformación del paquete de revisión no es válida".</span><span class="sxs-lookup"><span data-stu-id="5eccb-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="5eccb-128">Esta tabla normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión.</span><span class="sxs-lookup"><span data-stu-id="5eccb-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="5eccb-129">Normalmente no se crea directamente en un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="5eccb-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="5eccb-130">Validación</span><span class="sxs-lookup"><span data-stu-id="5eccb-130">Validation</span></span>

<dl>

[<span data-ttu-id="5eccb-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="5eccb-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5eccb-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="5eccb-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



