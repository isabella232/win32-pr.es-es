---
title: IDWriteFontFace GetGdiCompatibleGlyphMetrics, método
description: Obtiene las métricas del glifo en unidades de diseño de fuentes con los valores devueltos compatibles con lo que generará GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Método GetGdiCompatibleGlyphMetrics de escritura directa
- Método GetGdiCompatibleGlyphMetrics de escritura directa, interfaz IDWriteFontFace
- Interfaz IDWriteFontFace Direct Write, método GetGdiCompatibleGlyphMetrics
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671191"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="3c496-106">IDWriteFontFace:: GetGdiCompatibleGlyphMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="3c496-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="3c496-107">Obtiene las métricas del glifo en unidades de diseño de fuentes con los valores devueltos compatibles con lo que generará GDI.</span><span class="sxs-lookup"><span data-stu-id="3c496-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c496-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c496-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3c496-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c496-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c496-110">*emSize*</span><span class="sxs-lookup"><span data-stu-id="3c496-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="3c496-111">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3c496-111">Type: **FLOAT**</span></span>

<span data-ttu-id="3c496-112">Tamaño de lógic de la fuente en unidades DIP.</span><span class="sxs-lookup"><span data-stu-id="3c496-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-113">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="3c496-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="3c496-114">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="3c496-114">Type: **FLOAT**</span></span>

<span data-ttu-id="3c496-115">Número de píxeles físicos por DIP.</span><span class="sxs-lookup"><span data-stu-id="3c496-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-116">*transformación* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3c496-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c496-117">Tipo: **\* [**\_ matriz de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**</span><span class="sxs-lookup"><span data-stu-id="3c496-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="3c496-118">Transformación opcional que se aplica a los glifos y sus posiciones.</span><span class="sxs-lookup"><span data-stu-id="3c496-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="3c496-119">Esta transformación se aplica después del ajuste de escala especificado por el tamaño de fuente y *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="3c496-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-120">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="3c496-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="3c496-121">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3c496-121">Type: **BOOL**</span></span>

<span data-ttu-id="3c496-122">Cuando se establece en **false**, las métricas son las mismas que las métricas del texto con alias de GDI.</span><span class="sxs-lookup"><span data-stu-id="3c496-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="3c496-123">Cuando se establece en **true**, las métricas son las mismas que las métricas de texto que la GDI mide usando una fuente creada con **\_ \_ calidad natural de CLEARTYPE**.</span><span class="sxs-lookup"><span data-stu-id="3c496-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-124">*glyphIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c496-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c496-125">Tipo: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="3c496-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="3c496-126">Matriz de índices de glifo para la que se van a calcular las métricas.</span><span class="sxs-lookup"><span data-stu-id="3c496-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-127">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="3c496-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3c496-128">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c496-128">Type: **UINT32**</span></span>

<span data-ttu-id="3c496-129">Número de elementos de la matriz *glyphIndices* .</span><span class="sxs-lookup"><span data-stu-id="3c496-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-130">*glyphMetrics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c496-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c496-131">Tipo: **[ **\_ \_ métricas del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="3c496-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="3c496-132">Matriz de las estructuras de [**\_ \_ métricas del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) rellenadas por esta función.</span><span class="sxs-lookup"><span data-stu-id="3c496-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="3c496-133">Las métricas están en unidades de diseño de fuentes.</span><span class="sxs-lookup"><span data-stu-id="3c496-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="3c496-134">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="3c496-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="3c496-135">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="3c496-135">Type: **BOOL**</span></span>

<span data-ttu-id="3c496-136">Un valor BOOLEANO que indica si la fuente se usa en una ejecución lateral.</span><span class="sxs-lookup"><span data-stu-id="3c496-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="3c496-137">Esto puede afectar a las métricas del glifo si la fuente tiene una simulación oblicuo porque la simulación oblicuo lateral difiere de la simulación oblicuo no lateral.</span><span class="sxs-lookup"><span data-stu-id="3c496-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c496-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c496-138">Return value</span></span>

<span data-ttu-id="3c496-139">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3c496-139">Type: **HRESULT**</span></span>

<span data-ttu-id="3c496-140">Código de error **HRESULT** estándar.</span><span class="sxs-lookup"><span data-stu-id="3c496-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="3c496-141">Si alguno de los índices de glifos de entrada está fuera del intervalo de índices de glifo válido para la fuente actual, se devolverá **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="3c496-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c496-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c496-142">Requirements</span></span>



| <span data-ttu-id="3c496-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c496-143">Requirement</span></span> | <span data-ttu-id="3c496-144">Value</span><span class="sxs-lookup"><span data-stu-id="3c496-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c496-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c496-145">Library</span></span><br/> | <dl> <span data-ttu-id="3c496-146"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c496-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c496-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c496-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c496-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c496-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c496-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c496-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c496-150">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="3c496-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="3c496-151">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="3c496-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

