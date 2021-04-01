---
title: Interfaz IDWriteFontFallbackBuilder
description: Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reversión de fuente a partir de esas asignaciones.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Interfaz IDWriteFontFallbackBuilder de escritura directa
- IDWriteFontFallbackBuilder interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996628"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="9d87f-105">Interfaz IDWriteFontFallbackBuilder</span><span class="sxs-lookup"><span data-stu-id="9d87f-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="9d87f-106">Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reversión de fuente a partir de esas asignaciones.</span><span class="sxs-lookup"><span data-stu-id="9d87f-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="9d87f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d87f-107">Members</span></span>

<span data-ttu-id="9d87f-108">La interfaz **IDWriteFontFallbackBuilder** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9d87f-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9d87f-109">**IDWriteFontFallbackBuilder** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9d87f-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="9d87f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d87f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9d87f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d87f-111">Methods</span></span>

<span data-ttu-id="9d87f-112">La interfaz **IDWriteFontFallbackBuilder** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9d87f-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="9d87f-113">Método</span><span class="sxs-lookup"><span data-stu-id="9d87f-113">Method</span></span>                                                                      | <span data-ttu-id="9d87f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d87f-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d87f-115">**AddMapping**</span><span class="sxs-lookup"><span data-stu-id="9d87f-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="9d87f-116">Anexa una única asignación a la lista.</span><span class="sxs-lookup"><span data-stu-id="9d87f-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="9d87f-117">Llame a este método una vez por cada asignación adicional.</span><span class="sxs-lookup"><span data-stu-id="9d87f-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="9d87f-118">**AddMappings**</span><span class="sxs-lookup"><span data-stu-id="9d87f-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="9d87f-119">Agregue todas las asignaciones de un objeto de reserva de fuente existente.</span><span class="sxs-lookup"><span data-stu-id="9d87f-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="9d87f-120">**CreateFontFallback**</span><span class="sxs-lookup"><span data-stu-id="9d87f-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="9d87f-121">Crea el objeto de reserva finalizado a partir de las asignaciones agregadas.</span><span class="sxs-lookup"><span data-stu-id="9d87f-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="9d87f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d87f-122">Requirements</span></span>



| <span data-ttu-id="9d87f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d87f-123">Requirement</span></span> | <span data-ttu-id="9d87f-124">Value</span><span class="sxs-lookup"><span data-stu-id="9d87f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d87f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d87f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d87f-126">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="9d87f-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="9d87f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d87f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d87f-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9d87f-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="9d87f-129">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d87f-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="9d87f-130">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="9d87f-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="9d87f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d87f-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d87f-132"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d87f-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9d87f-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d87f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d87f-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d87f-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

