---
title: Efecto de detección perimetral
description: Filtra el contenido de una imagen, manteniendo las líneas en los bordes de las secciones de contraste de la imagen.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079773"
---
# <a name="edge-detection-effect"></a>Efecto de detección perimetral

Filtra el contenido de una imagen, manteniendo las líneas en los bordes de las secciones de contraste de la imagen.

El CLSID para este efecto es CLSID \_ D2D1EdgeDetection.

-   [Imagen de ejemplo](#example-image)
-   [Código de ejemplo](#sample-code)
-   [Propiedades del efecto](#effect-properties)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

![ejemplo de resultado de efecto](images/edge-detection-effect.png)

## <a name="sample-code"></a>Código de ejemplo

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propiedades del efecto

Las propiedades del efecto de detección perimetral se definen mediante la enumeración [**\_ \_ prop de D2D1 EDGEDETECTION**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Servidor mínimo compatible | Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\] |
| Encabezado                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Temas relacionados

* [Interfaz ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
