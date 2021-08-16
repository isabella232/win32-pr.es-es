---
title: Método IDWriteTextAnalyzer GetGdiCompatibleGlyphPlacements
description: Coloque la salida de glifos del método GetGlyphs según la fuente y las reglas de representación del sistema de escritura.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Método GetGdiCompatibleGlyphPlacements Escritura directa
- Método GetGdiCompatibleGlyphPlacements Direct Write , interfaz IDWriteTextAnalyzer
- IdWriteTextAnalyzer interface Direct Write , Método GetGdiCompatibleGlyphPlacements
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
ms.openlocfilehash: 8d05fcf5595500f34730a720e4a4c2e80d68922929d8055b754a26a1dc92f63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650015"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>Método IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements

Coloque la salida de glifos del [**método GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) según la fuente y las reglas de representación del sistema de escritura.

## <a name="syntax"></a>Sintaxis


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



## <a name="parameters"></a>Parámetros

<dl> <dt>

*textString* \[ En\]
</dt> <dd>

Tipo: **const \* WCHAR**

Matriz de caracteres que contiene la cadena original de la que han llegado los glifos.

</dd> <dt>

*clusterMap* \[ En\]
</dt> <dd>

Tipo: **const UINT16 \***

Puntero a la asignación de intervalos de caracteres a intervalos de glifos. [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)devuelve este valor.

</dd> <dt>

*textProps* \[ En\]
</dt> <dd>

Tipo: **[ **DWRITE \_ SHAPING \_ TEXT \_ PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Puntero a una matriz de estructuras que contiene propiedades de forma para cada carácter. [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)devuelve esta estructura.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

Longitud de texto de *textString.*

</dd> <dt>

*glyphIndices* \[ En\]
</dt> <dd>

Tipo: **const UINT16 \***

Matriz de índices de glifo devueltos por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphProps* \[ En\]
</dt> <dd>

Tipo: **const [**DWRITE \_ SHAPING GLYPH \_ \_ PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***

Puntero a una matriz de estructuras que contienen propiedades de forma para cada glifo devuelto por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

Número de glifos devueltos de [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*fontFace* \[ En\]
</dt> <dd>

Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Puntero a la cara de fuente que es el origen de los glifos de salida.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Tipo: **FLOAT**

Tamaño de fuente lógico en DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **FLOAT**

Número de píxeles físicos por DIP.

</dd> <dt>

*transform* \[ in, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Transformación opcional aplicada a los glifos y sus posiciones. Esta transformación se aplica después del escalado especificado por el tamaño de fuente y *pixelsPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **BOOL**

Cuando se establece en **FALSE,** las métricas son las mismas que las métricas del texto con alias GDI. Cuando se establece en **TRUE**, las métricas son las mismas que las métricas de texto medidas por GDI mediante una fuente creada con **CLEARTYPE \_ NATURAL \_ QUALITY**.

</dd> <dt>

 *isSideways* 
</dt> <dd>

Tipo: **BOOL**

Marca booleana establecida en **TRUE** si el texto está pensado para dibujarse verticalmente.

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

Tipo: **BOOL**

Marca booleana establecida en **TRUE para** texto de derecha a izquierda.

</dd> <dt>

 *scriptAnalysis* \[ En\]
</dt> <dd>

Tipo: **const [**DWRITE \_ SCRIPT \_ ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***

Puntero a un resultado de análisis de script de [**una llamada a AnalyzeScript.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript)

</dd> <dt>

 *localeName* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Matriz de caracteres que contiene la configuración regional que se usará al seleccionar glifos. Por ejemplo, el mismo carácter puede asignarse a glifos diferentes para ja-jp frente a zh-chs. Si es **NULL,** se usa la asignación predeterminada basada en el script.

</dd> <dt>

 *características* \[ in, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ \_ TYPOGRAPHIC FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***

Matriz de punteros a los conjuntos de características tipográficos que se van a usar en cada intervalo de características.

</dd> <dt>

 *featureRangeLengths* \[ in, opcional\]
</dt> <dd>

Tipo: **const UINT32 \***

Longitud de cada intervalo de características, en caracteres. La suma de todas las longitudes debe ser igual a *textLength.*

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Tipo: **UINT32**

Número de intervalos de características.

</dd> <dt>

 *glyphAdvances* \[ out\]
</dt> <dd>

Tipo: **\* FLOAT**

Cuando este método devuelve un resultado, contiene el ancho de avance de cada glifo.

</dd> <dt>

 *glyphOffsets* \[ out\]
</dt> <dd>

Tipo: **[ **DWRITE \_ GLYPH \_ OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Cuando este método devuelve un resultado, contiene el desplazamiento del origen de cada glifo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

