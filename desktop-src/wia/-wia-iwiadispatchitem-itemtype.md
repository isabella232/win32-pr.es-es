---
description: Tipo de este elemento. Solo lectura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Propiedad Item. ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720534"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="fd3f0-104">Propiedad Item. ItemType</span><span class="sxs-lookup"><span data-stu-id="fd3f0-104">Item.ItemType property</span></span>

<span data-ttu-id="fd3f0-105">Tipo de este elemento.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-105">The type of this item.</span></span> <span data-ttu-id="fd3f0-106">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-106">Read-only.</span></span>

<span data-ttu-id="fd3f0-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3f0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd3f0-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="fd3f0-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fd3f0-109">Property value</span></span>

<span data-ttu-id="fd3f0-110">Los valores siguientes son posibles:</span><span class="sxs-lookup"><span data-stu-id="fd3f0-110">The following values are possible:</span></span>



| <span data-ttu-id="fd3f0-111">Value</span><span class="sxs-lookup"><span data-stu-id="fd3f0-111">Value</span></span>  | <span data-ttu-id="fd3f0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd3f0-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="fd3f0-113">device</span><span class="sxs-lookup"><span data-stu-id="fd3f0-113">device</span></span> | <span data-ttu-id="fd3f0-114">El elemento es un dispositivo de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="fd3f0-115">folder</span><span class="sxs-lookup"><span data-stu-id="fd3f0-115">folder</span></span> | <span data-ttu-id="fd3f0-116">El elemento es una carpeta que contiene otros elementos.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="fd3f0-117">archivo</span><span class="sxs-lookup"><span data-stu-id="fd3f0-117">file</span></span>   | <span data-ttu-id="fd3f0-118">El elemento es un archivo de imagen o de audio.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="fd3f0-119">audio</span><span class="sxs-lookup"><span data-stu-id="fd3f0-119">audio</span></span>  | <span data-ttu-id="fd3f0-120">El elemento es un clip de audio.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="fd3f0-121">imagen</span><span class="sxs-lookup"><span data-stu-id="fd3f0-121">image</span></span>  | <span data-ttu-id="fd3f0-122">El elemento es una imagen.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="fd3f0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd3f0-123">Remarks</span></span>

<span data-ttu-id="fd3f0-124">Un elemento puede tener más de un tipo.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-124">An item can have more than one type.</span></span> <span data-ttu-id="fd3f0-125">Por ejemplo, cada imagen tiene los tipos "imagen" y "archivo".</span><span class="sxs-lookup"><span data-stu-id="fd3f0-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="fd3f0-126">**ItemType** devuelve una cadena que incluye todos los tipos válidos para el elemento, separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="fd3f0-127">Por ejemplo, "Image; File".</span><span class="sxs-lookup"><span data-stu-id="fd3f0-127">For example, "image;file".</span></span> <span data-ttu-id="fd3f0-128">No hay espacios en esta cadena y no hay un punto y coma al final.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3f0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd3f0-129">Requirements</span></span>



| <span data-ttu-id="fd3f0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3f0-130">Requirement</span></span> | <span data-ttu-id="fd3f0-131">Value</span><span class="sxs-lookup"><span data-stu-id="fd3f0-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3f0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3f0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fd3f0-133">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fd3f0-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd3f0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd3f0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fd3f0-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd3f0-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd3f0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd3f0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd3f0-137"><dt>Wiascr.dll (versión 4,90 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fd3f0-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




