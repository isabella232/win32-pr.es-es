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
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a>IDWriteFontFace:: GetGdiCompatibleGlyphMetrics (método)

Obtiene las métricas del glifo en unidades de diseño de fuentes con los valores devueltos compatibles con lo que generará GDI.

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

Tipo: **float**

Tamaño de lógic de la fuente en unidades DIP.

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

*glyphIndices* \[ de\]
</dt> <dd>

Tipo: **const UINT16 \***

Matriz de índices de glifo para la que se van a calcular las métricas.

</dd> <dt>

*glyphCount* 
</dt> <dd>

Tipo: **UINT32**

Número de elementos de la matriz *glyphIndices* .

</dd> <dt>

*glyphMetrics* \[ enuncia\]
</dt> <dd>

Tipo: **[ **\_ \_ métricas del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***

Matriz de las estructuras de [**\_ \_ métricas del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) rellenadas por esta función. Las métricas están en unidades de diseño de fuentes.

</dd> <dt>

*isSideways* 
</dt> <dd>

Tipo: **bool**

Un valor BOOLEANO que indica si la fuente se usa en una ejecución lateral. Esto puede afectar a las métricas del glifo si la fuente tiene una simulación oblicuo porque la simulación oblicuo lateral difiere de la simulación oblicuo no lateral.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Código de error **HRESULT** estándar. Si alguno de los índices de glifos de entrada está fuera del intervalo de índices de glifo válido para la fuente actual, se devolverá **E \_ INVALIDARG** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

