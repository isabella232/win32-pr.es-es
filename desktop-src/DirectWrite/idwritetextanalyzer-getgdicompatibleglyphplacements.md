---
title: IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements, método
description: Coloque los glifos de salida del método GetGlyphs según la fuente y las reglas de representación del sistema de escritura.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Método GetGdiCompatibleGlyphPlacements de escritura directa
- Método GetGdiCompatibleGlyphPlacements de escritura directa, interfaz IDWriteTextAnalyzer
- Interfaz IDWriteTextAnalyzer Direct Write, método GetGdiCompatibleGlyphPlacements
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670526"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="77e54-106">IDWriteTextAnalyzer:: GetGdiCompatibleGlyphPlacements (método)</span><span class="sxs-lookup"><span data-stu-id="77e54-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="77e54-107">Coloque los glifos de salida del método [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) según la fuente y las reglas de representación del sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="77e54-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e54-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77e54-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="77e54-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77e54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e54-110">*textString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-111">Tipo: **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="77e54-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="77e54-112">Matriz de caracteres que contiene la cadena original de la que proceden los glifos.</span><span class="sxs-lookup"><span data-stu-id="77e54-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="77e54-113">*clusterMap* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-114">Tipo: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="77e54-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="77e54-115">Puntero a la asignación de intervalos de caracteres a intervalos de glifo.</span><span class="sxs-lookup"><span data-stu-id="77e54-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="77e54-116">Lo devuelve [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="77e54-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="77e54-117">*textProps* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-118">Tipo: **[ **\_ \_ \_ propiedades de texto** de forma DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="77e54-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="77e54-119">Puntero a una matriz de estructuras que contiene las propiedades de forma de cada carácter.</span><span class="sxs-lookup"><span data-stu-id="77e54-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="77e54-120">[**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)devuelve esta estructura.</span><span class="sxs-lookup"><span data-stu-id="77e54-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="77e54-121">*textLength*</span><span class="sxs-lookup"><span data-stu-id="77e54-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-122">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="77e54-122">Type: **UINT32**</span></span>

<span data-ttu-id="77e54-123">La longitud del texto de *textString*.</span><span class="sxs-lookup"><span data-stu-id="77e54-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="77e54-124">*glyphIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-125">Tipo: **const UINT16 \***</span><span class="sxs-lookup"><span data-stu-id="77e54-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="77e54-126">Matriz de índices de glifo devuelta por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="77e54-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="77e54-127">*glyphProps* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-128">Tipo: **\* const [**DWRITE \_ propiedades del \_ glifo \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)** de forma</span><span class="sxs-lookup"><span data-stu-id="77e54-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="77e54-129">Puntero a una matriz de estructuras que contienen propiedades de forma para cada glifo devuelto por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="77e54-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="77e54-130">*glyphCount*</span><span class="sxs-lookup"><span data-stu-id="77e54-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-131">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="77e54-131">Type: **UINT32**</span></span>

<span data-ttu-id="77e54-132">El número de glifos devueltos desde [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span><span class="sxs-lookup"><span data-stu-id="77e54-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="77e54-133">*fontFace* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-134">Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="77e54-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="77e54-135">Puntero al tipo de fuente que es el origen de los glifos de salida.</span><span class="sxs-lookup"><span data-stu-id="77e54-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="77e54-136">*fontEmSize*</span><span class="sxs-lookup"><span data-stu-id="77e54-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-137">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="77e54-137">Type: **FLOAT**</span></span>

<span data-ttu-id="77e54-138">Tamaño de fuente lógico en DIP.</span><span class="sxs-lookup"><span data-stu-id="77e54-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="77e54-139">*pixelsPerDip*</span><span class="sxs-lookup"><span data-stu-id="77e54-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-140">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="77e54-140">Type: **FLOAT**</span></span>

<span data-ttu-id="77e54-141">Número de píxeles físicos por DIP.</span><span class="sxs-lookup"><span data-stu-id="77e54-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="77e54-142">*transformación* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77e54-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-143">Tipo: **\* [**\_ matriz de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**</span><span class="sxs-lookup"><span data-stu-id="77e54-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="77e54-144">Transformación opcional que se aplica a los glifos y sus posiciones.</span><span class="sxs-lookup"><span data-stu-id="77e54-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="77e54-145">Esta transformación se aplica después del ajuste de escala especificado por el tamaño de fuente y *pixelsPerDip*.</span><span class="sxs-lookup"><span data-stu-id="77e54-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="77e54-146">*useGdiNatural*</span><span class="sxs-lookup"><span data-stu-id="77e54-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-147">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="77e54-147">Type: **BOOL**</span></span>

<span data-ttu-id="77e54-148">Cuando se establece en **false**, las métricas son las mismas que las métricas del texto con alias de GDI.</span><span class="sxs-lookup"><span data-stu-id="77e54-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="77e54-149">Cuando se establece en **true**, las métricas son las mismas que las métricas de texto que la GDI mide usando una fuente creada con **\_ \_ calidad natural de CLEARTYPE**.</span><span class="sxs-lookup"><span data-stu-id="77e54-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-150">*isSideways*</span><span class="sxs-lookup"><span data-stu-id="77e54-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-151">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="77e54-151">Type: **BOOL**</span></span>

<span data-ttu-id="77e54-152">Marca booleana establecida en **true** si el texto está diseñado para dibujarse verticalmente.</span><span class="sxs-lookup"><span data-stu-id="77e54-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-153">*isRightToLeft*</span><span class="sxs-lookup"><span data-stu-id="77e54-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-154">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="77e54-154">Type: **BOOL**</span></span>

<span data-ttu-id="77e54-155">Una marca booleana establecida en **true** para el texto de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="77e54-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-156">*scriptAnalysis* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e54-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-157">Tipo: **\* [**DWRITE \_ \_ análisis de script**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) const**</span><span class="sxs-lookup"><span data-stu-id="77e54-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="77e54-158">Un puntero a un resultado de análisis de script de una llamada a [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .</span><span class="sxs-lookup"><span data-stu-id="77e54-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-159">*localeName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77e54-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-160">Tipo: **const WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="77e54-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="77e54-161">Matriz de caracteres que contiene la configuración regional que se va a usar al seleccionar los glifos.</span><span class="sxs-lookup"><span data-stu-id="77e54-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="77e54-162">Por ejemplo, el mismo carácter puede asignarse a glifos diferentes de ja-JP en comparación con ZH-CHS.</span><span class="sxs-lookup"><span data-stu-id="77e54-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="77e54-163">Si es **null**, se utiliza la asignación predeterminada basada en el script.</span><span class="sxs-lookup"><span data-stu-id="77e54-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-164">*características* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77e54-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-165">Tipo: **\* \* const [**DWRITE \_ \_ características tipográficas**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**</span><span class="sxs-lookup"><span data-stu-id="77e54-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="77e54-166">Matriz de punteros a los conjuntos de características tipográficas que se van a usar en cada intervalo de características.</span><span class="sxs-lookup"><span data-stu-id="77e54-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-167">*featureRangeLengths* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="77e54-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-168">Tipo: **const UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="77e54-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="77e54-169">La longitud de cada intervalo de características, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="77e54-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="77e54-170">La suma de todas las longitudes debe ser igual a *textLength*.</span><span class="sxs-lookup"><span data-stu-id="77e54-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-171">*featureRanges*</span><span class="sxs-lookup"><span data-stu-id="77e54-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="77e54-172">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="77e54-172">Type: **UINT32**</span></span>

<span data-ttu-id="77e54-173">El número de intervalos de características.</span><span class="sxs-lookup"><span data-stu-id="77e54-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-174">*glyphAdvances* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77e54-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-175">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="77e54-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="77e54-176">Cuando este método finaliza, contiene el ancho de avance de cada glifo.</span><span class="sxs-lookup"><span data-stu-id="77e54-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="77e54-177">*glyphOffsets* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77e54-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77e54-178">Tipo: **[ **DWRITE \_ glifo \_ offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="77e54-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="77e54-179">Cuando este método finaliza, contiene el desplazamiento del origen de cada glifo.</span><span class="sxs-lookup"><span data-stu-id="77e54-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e54-180">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77e54-180">Return value</span></span>

<span data-ttu-id="77e54-181">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="77e54-181">Type: **HRESULT**</span></span>

<span data-ttu-id="77e54-182">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="77e54-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77e54-183">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77e54-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e54-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77e54-184">Requirements</span></span>



| <span data-ttu-id="77e54-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e54-185">Requirement</span></span> | <span data-ttu-id="77e54-186">Value</span><span class="sxs-lookup"><span data-stu-id="77e54-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77e54-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77e54-187">Library</span></span><br/> | <dl> <span data-ttu-id="77e54-188"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77e54-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="77e54-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77e54-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="77e54-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e54-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e54-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="77e54-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e54-192">**IDWriteTextAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="77e54-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

