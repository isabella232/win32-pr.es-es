---
title: IDWriteFontFace GetGdiCompatibleMetrics, método
description: Obtiene las unidades de diseño y las métricas comunes para el tipo de fuente. Estas métricas se aplican a todos los glifos dentro de un fontface y las usan las aplicaciones para realizar cálculos de diseño.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Método GetGdiCompatibleMetrics de escritura directa
- Método GetGdiCompatibleMetrics de escritura directa, interfaz IDWriteFontFace
- Interfaz IDWriteFontFace Direct Write, método GetGdiCompatibleMetrics
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
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690138"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a>IDWriteFontFace:: GetGdiCompatibleMetrics (método)

Obtiene las unidades de diseño y las métricas comunes para el tipo de fuente. Estas métricas se aplican a todos los glifos dentro de un fontface y las usan las aplicaciones para realizar cálculos de diseño.

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

Tipo: **float**

Tamaño lógico de la fuente en unidades DIP.

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

*fontFaceMetrics* \[ enuncia\]
</dt> <dd>

Tipo: **[ **\_ \_ métricas de fuente DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***

Puntero a una estructura [**de \_ \_ métricas de fuente DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)para rellenar. Las métricas devueltas por esta función están en unidades de diseño de fuentes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Código de error HRESULT estándar.

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

 

