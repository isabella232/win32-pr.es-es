---
title: Método IDWriteFontFace GetGdiCompatibleGlyphMetrics
description: Obtiene métricas de glifo en unidades de diseño de fuentes con los valores devueltos compatibles con lo que generaría GDI.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Método GetGdiCompatibleGlyphMetrics de escritura directa
- Método GetGdiCompatibleGlyphMetrics direct write , interfaz IDWriteFontFace
- Método GetGdiCompatibleGlyphMetrics de la interfaz IDWriteFontFace
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
ms.openlocfilehash: bd36fc09ff8161ba8fb72d3b55b9351b0a7d2a6bd3f3f11a71c15a8d9422f6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816505"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>Método IDWriteFontFace::GetGdiCompatibleGlyphMetrics

Obtiene métricas de glifo en unidades de diseño de fuentes con los valores devueltos compatibles con lo que generaría GDI.

## <a name="syntax"></a>Sintaxis


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



## <a name="parameters"></a>Parámetros

<dl> <dt>

*emSize* 
</dt> <dd>

Tipo: **FLOAT**

Tamaño de la fuente en unidades DIP.

</dd> <dt>

*pixelsPerDip* 
</dt> <dd>

Tipo: **FLOAT**

Número de píxeles físicos por DIP.

</dd> <dt>

*transformación* \[ en, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Una transformación opcional aplicada a los glifos y sus posiciones. Esta transformación se aplica después del escalado especificado por el tamaño de fuente y *pixelsPerDip*.

</dd> <dt>

*useGdiAtura* 
</dt> <dd>

Tipo: **BOOL**

Cuando se establece en **FALSE,** las métricas son las mismas que las métricas del texto con alias GDI. Cuando se establece en **TRUE,** las métricas son las mismas que las métricas de texto medidas por GDI mediante una fuente creada con **CLEARTYPE \_ NATURAL \_ QUALITY**.

</dd> <dt>

*glyphIndices* \[ En\]
</dt> <dd>

Tipo: **const UINT16 \***

Matriz de índices de glifo para los que se calculan las métricas.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

Número de elementos de la matriz *glyphIndices.*

</dd> <dt>

*glyphMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **MÉTRICAS DE \_ GLIFO DE \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Matriz de estructuras [**DWRITE \_ GLYPH \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) rellenadas por esta función. Las métricas están en unidades de diseño de fuentes.

</dd> <dt>

*isSideways* 
</dt> <dd>

Tipo: **BOOL**

Valor BOOL que indica si la fuente se usa en una ejecución lateral. Esto puede afectar a las métricas de glifo si la fuente tiene simulación oblicuo porque la simulación oblicua lateral difiere de la simulación oblicua no lateral.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Código de error **HRESULT** estándar. Si alguno de los índices de glifo de entrada está fuera del intervalo de índice de glifo válido para la cara de fuente actual, se devolverá **E \_ INVALIDARG.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

