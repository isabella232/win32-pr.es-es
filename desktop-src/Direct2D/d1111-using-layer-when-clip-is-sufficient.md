---
title: D1111 usar capa cuando el recorte es suficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Se usa una capa con una máscara de opacidad NULL, una opacidad de 1,0 y una máscara geométrica rectangular alineada en el eje. Push/Pop Clip API debe lograr los mismos resultados con un mayor rendimiento.
keywords:
- D1111 usar capa cuando clip es suficiente con Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164110"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: Usar la capa cuando el recorte es suficiente

PERF: se usa una capa con una máscara de opacidad **NULL,** una opacidad de 1,0 y una máscara geométrica rectangular alineada en el eje. Push/Pop Clip API debe lograr los mismos resultados con un mayor rendimiento.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Dirección de la interfaz.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Nivel de error | Información |



 

## <a name="examples"></a>Ejemplos

El código siguiente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) cuando la capa contiene solo un primitivo (un rectángulo) y los campos de la estructura DE PARÁMETROS DE CAPA [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en valores predeterminados. Para obtener los valores predeterminados de la estructura DE PARÁMETROS **\_ DE CAPA \_ D2D1,** vea [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



En este ejemplo se genera el siguiente mensaje de depuración:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Causas posibles

Se usó una capa cuando los [**métodos PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) hubieran bastado.

 

 