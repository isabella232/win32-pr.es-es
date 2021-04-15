---
title: Interfaz IDWriteTextAnalyzer2
description: Analiza varias propiedades de texto para el procesamiento complejo de scripts.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Interfaz IDWriteTextAnalyzer2 de escritura directa
- IDWriteTextAnalyzer2 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534492"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="4b00f-105">Interfaz IDWriteTextAnalyzer2</span><span class="sxs-lookup"><span data-stu-id="4b00f-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="4b00f-106">Analiza varias propiedades de texto para el procesamiento complejo de scripts.</span><span class="sxs-lookup"><span data-stu-id="4b00f-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="4b00f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b00f-107">Members</span></span>

<span data-ttu-id="4b00f-108">La interfaz **IDWriteTextAnalyzer2** hereda de [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span><span class="sxs-lookup"><span data-stu-id="4b00f-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="4b00f-109">**IDWriteTextAnalyzer2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4b00f-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="4b00f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b00f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b00f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b00f-111">Methods</span></span>

<span data-ttu-id="4b00f-112">La interfaz **IDWriteTextAnalyzer2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4b00f-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="4b00f-113">Método</span><span class="sxs-lookup"><span data-stu-id="4b00f-113">Method</span></span>                                                                                    | <span data-ttu-id="4b00f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b00f-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b00f-115">**CheckTypographicFeature**</span><span class="sxs-lookup"><span data-stu-id="4b00f-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="4b00f-116">Comprueba si una característica tipográfica está disponible para un glifo o un conjunto de glifos.</span><span class="sxs-lookup"><span data-stu-id="4b00f-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="4b00f-117">**GetGlyphOrientationTransform**</span><span class="sxs-lookup"><span data-stu-id="4b00f-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="4b00f-118">Devuelve la matriz de transformación de 2x3 para el ángulo respectivo para dibujar la ejecución del glifo.</span><span class="sxs-lookup"><span data-stu-id="4b00f-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="4b00f-119">**GetTypographicFeatures**</span><span class="sxs-lookup"><span data-stu-id="4b00f-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="4b00f-120">Devuelve una lista completa de las características OpenType disponibles para un script o una fuente.</span><span class="sxs-lookup"><span data-stu-id="4b00f-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b00f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b00f-121">Requirements</span></span>



| <span data-ttu-id="4b00f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b00f-122">Requirement</span></span> | <span data-ttu-id="4b00f-123">Value</span><span class="sxs-lookup"><span data-stu-id="4b00f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b00f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b00f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b00f-125">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4b00f-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="4b00f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b00f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b00f-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="4b00f-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="4b00f-128">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b00f-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4b00f-129">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="4b00f-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="4b00f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b00f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b00f-131"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b00f-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4b00f-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b00f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b00f-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b00f-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4b00f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b00f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b00f-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="4b00f-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

