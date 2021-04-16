---
title: Interfaz IDWriteFactory2
description: La interfaz de fábrica raíz para todos los objetos de DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Interfaz IDWriteFactory1 de escritura directa
- IDWriteFactory1 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686048"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="9eee0-105">Interfaz IDWriteFactory2</span><span class="sxs-lookup"><span data-stu-id="9eee0-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="9eee0-106">La interfaz de fábrica raíz para todos los objetos de [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9eee0-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="9eee0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9eee0-107">Members</span></span>

<span data-ttu-id="9eee0-108">La interfaz **IDWriteFactory1** hereda de [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span><span class="sxs-lookup"><span data-stu-id="9eee0-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="9eee0-109">**IDWriteFactory2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9eee0-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="9eee0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9eee0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9eee0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9eee0-111">Methods</span></span>

<span data-ttu-id="9eee0-112">La interfaz **IDWriteFactory1** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9eee0-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="9eee0-113">Método</span><span class="sxs-lookup"><span data-stu-id="9eee0-113">Method</span></span>                                                                             | <span data-ttu-id="9eee0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9eee0-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eee0-115">**CreateCustomRenderingParams**</span><span class="sxs-lookup"><span data-stu-id="9eee0-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="9eee0-116">Crea un objeto de parámetros de representación con las propiedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="9eee0-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="9eee0-117">**CreateFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="9eee0-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="9eee0-118">Crea un objeto de generador de reserva de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9eee0-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="9eee0-119">**CreateGlyphRunAnalysis**</span><span class="sxs-lookup"><span data-stu-id="9eee0-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="9eee0-120">Crea un objeto de análisis de ejecución de glifos, que encapsula la información utilizada para representar una ejecución de glifo.</span><span class="sxs-lookup"><span data-stu-id="9eee0-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="9eee0-121">**GetSystemFontFallback**</span><span class="sxs-lookup"><span data-stu-id="9eee0-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="9eee0-122">Crea un objeto de reserva de fuente a partir de la lista de reserva del sistema.</span><span class="sxs-lookup"><span data-stu-id="9eee0-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="9eee0-123">**TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="9eee0-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="9eee0-124">Se llama a este método en una ejecución de glifo para convertirlo en ejecuciones de glifo de varios colores.</span><span class="sxs-lookup"><span data-stu-id="9eee0-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="9eee0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eee0-125">Requirements</span></span>



| <span data-ttu-id="9eee0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eee0-126">Requirement</span></span> | <span data-ttu-id="9eee0-127">Value</span><span class="sxs-lookup"><span data-stu-id="9eee0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eee0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9eee0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9eee0-129">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="9eee0-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="9eee0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9eee0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9eee0-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9eee0-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="9eee0-132">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9eee0-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="9eee0-133">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="9eee0-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="9eee0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9eee0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9eee0-135"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eee0-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9eee0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9eee0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eee0-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eee0-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9eee0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9eee0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eee0-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="9eee0-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="9eee0-140">**IDWriteFactory**</span><span class="sxs-lookup"><span data-stu-id="9eee0-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

