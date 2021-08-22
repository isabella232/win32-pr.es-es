---
title: D1111 usar capa cuando el clip es suficiente
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
ms.openlocfilehash: b03a6c2a4806724cd7cfdc97354e29e86dc60e0f1729ee9efeca89d971ca0a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758105"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: Usar la capa cuando el clip es suficiente

PERF: se usa una capa con una máscara de opacidad **NULL,** una opacidad de 1,0 y una máscara geométrica rectangular alineada en el eje. Push/Pop Clip API debe lograr los mismos resultados con un mayor rendimiento.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaz*
</dt> <dd>

Dirección de la interfaz.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Nivel de error | Information |



 

## <a name="examples"></a>Ejemplos

El código siguiente usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) cuando la capa contiene solo un primitivo (un rectángulo) y los campos de la estructura DE PARÁMETROS DE CAPA [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en valores predeterminados. Para obtener los valores predeterminados de la estructura **D2D1 \_ LAYER \_ PARAMETERS,** vea [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


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

 

 