---
title: Método IDWriteFontFace GetGdiCompatibleMetrics
description: Obtiene unidades de diseño y métricas comunes para la cara de fuente. Estas métricas son aplicables a todos los glifos dentro de un tipo de fuente y las usan las aplicaciones para los cálculos de diseño.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Método GetGdiCompatibleMetrics de escritura directa
- Método GetGdiCompatibleMetrics de escritura directa, interfaz IDWriteFontFace
- IdWriteFontFace interface Direct Write , GetGdiCompatibleMetrics (método GetGdiCompatibleMetrics)
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce5080edc44501290672bf0db0ebac69ef4856ec0b7163821cf60ac63d384ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290715"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>Método IDWriteFontFace::GetGdiCompatibleMetrics

Obtiene unidades de diseño y métricas comunes para la cara de fuente. Estas métricas son aplicables a todos los glifos dentro de un tipo de fuente y las usan las aplicaciones para los cálculos de diseño.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*emSize* 
</dt> <dd>

Tipo: **FLOAT**

Tamaño lógico de la fuente en unidades DIP.

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

*fontFaceMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **MÉTRICAS DE \_ FUENTES DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Puntero a una estructura [**\_ DWRITE FONT \_ METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S que se va a rellenar. Las métricas devueltas por esta función están en unidades de diseño de fuentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Código de error HRESULT estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

