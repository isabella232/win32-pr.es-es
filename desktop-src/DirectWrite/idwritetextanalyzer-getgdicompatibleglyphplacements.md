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
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a>IDWriteTextAnalyzer:: GetGdiCompatibleGlyphPlacements (método)

Coloque los glifos de salida del método [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) según la fuente y las reglas de representación del sistema de escritura.

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

*textString* \[ de\]
</dt> <dd>

Tipo: **const WCHAR \***

Matriz de caracteres que contiene la cadena original de la que proceden los glifos.

</dd> <dt>

*clusterMap* \[ de\]
</dt> <dd>

Tipo: **const UINT16 \***

Puntero a la asignación de intervalos de caracteres a intervalos de glifo. Lo devuelve [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*textProps* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ \_ propiedades de texto** de forma DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***

Puntero a una matriz de estructuras que contiene las propiedades de forma de cada carácter. [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)devuelve esta estructura.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

La longitud del texto de *textString*.

</dd> <dt>

*glyphIndices* \[ de\]
</dt> <dd>

Tipo: **const UINT16 \***

Matriz de índices de glifo devuelta por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphProps* \[ de\]
</dt> <dd>

Tipo: **\* const [**DWRITE \_ propiedades del \_ glifo \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)** de forma

Puntero a una matriz de estructuras que contienen propiedades de forma para cada glifo devuelto por [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

El número de glifos devueltos desde [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).

</dd> <dt>

*fontFace* \[ de\]
</dt> <dd>

Tipo: **[ **IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

Puntero al tipo de fuente que es el origen de los glifos de salida.

</dd> <dt>

*fontEmSize* 
</dt> <dd>

Tipo: **float**

Tamaño de fuente lógico en DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **float**

Número de píxeles físicos por DIP.

</dd> <dt>

*transformación* \[ de en, opcional\]
</dt> <dd>

Tipo: **\* [**\_ matriz de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) const**

Transformación opcional que se aplica a los glifos y sus posiciones. Esta transformación se aplica después del ajuste de escala especificado por el tamaño de fuente y *pixelsPerDip*.

</dd> <dt>

*useGdiNatural* 
</dt> <dd>

Tipo: **bool**

Cuando se establece en **false**, las métricas son las mismas que las métricas del texto con alias de GDI. Cuando se establece en **true**, las métricas son las mismas que las métricas de texto que la GDI mide usando una fuente creada con **\_ \_ calidad natural de CLEARTYPE**.

</dd> <dt>

 *isSideways* 
</dt> <dd>

Tipo: **bool**

Marca booleana establecida en **true** si el texto está diseñado para dibujarse verticalmente.

</dd> <dt>

 *isRightToLeft* 
</dt> <dd>

Tipo: **bool**

Una marca booleana establecida en **true** para el texto de derecha a izquierda.

</dd> <dt>

 *scriptAnalysis* \[ de\]
</dt> <dd>

Tipo: **\* [**DWRITE \_ \_ análisis de script**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) const**

Un puntero a un resultado de análisis de script de una llamada a [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) .

</dd> <dt>

 *localeName* \[ en, opcional\]
</dt> <dd>

Tipo: **const WCHAR \***

Matriz de caracteres que contiene la configuración regional que se va a usar al seleccionar los glifos. Por ejemplo, el mismo carácter puede asignarse a glifos diferentes de ja-JP en comparación con ZH-CHS. Si es **null**, se utiliza la asignación predeterminada basada en el script.

</dd> <dt>

 *características* \[ de en, opcional\]
</dt> <dd>

Tipo: **\* \* const [**DWRITE \_ \_ características tipográficas**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)**

Matriz de punteros a los conjuntos de características tipográficas que se van a usar en cada intervalo de características.

</dd> <dt>

 *featureRangeLengths* \[ en, opcional\]
</dt> <dd>

Tipo: **const UINT32 \***

La longitud de cada intervalo de características, en caracteres. La suma de todas las longitudes debe ser igual a *textLength*.

</dd> <dt>

 *featureRanges* 
</dt> <dd>

Tipo: **UINT32**

El número de intervalos de características.

</dd> <dt>

 *glyphAdvances* \[ enuncia\]
</dt> <dd>

Tipo: **float \***

Cuando este método finaliza, contiene el ancho de avance de cada glifo.

</dd> <dt>

 *glyphOffsets* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWRITE \_ glifo \_ offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***

Cuando este método finaliza, contiene el desplazamiento del origen de cada glifo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

