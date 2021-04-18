---
title: Métodos de ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1. h)
description: Crea un ID2D1GradientStopCollection a partir de la matriz especificada de \_ estructuras de detención de degradado de D2D1 \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Métodos de CreateGradientStopCollection Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4a298414d1a84b03d81c80e308113d8731369040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690164"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>ID2D1RenderTarget:: CreateGradientStopCollection (métodos)

Crea un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de la matriz especificada de estructuras de [**\_ \_ detención de degradado de D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateGradientStopCollection ( \_ detención de degradado \_ de D2D1 \* , gamma de D2D1 \_ , \_ \_ modo de extensión de D2D1, ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx) | Crea un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de los delimitadores de degradado, gamma de interpolación de color y modo de extensión especificados. <br/>                                                              |
| [**CreateGradientStopCollection ( \_ \_ detención de degradado de D2D1 \* , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)                                                            | Crea un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de los delimitadores de degradado especificados que utiliza la gamma de interpolación de color gamma de [**D2D1 \_ \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) y el modo de extensión de la abrazadera.<br/> |



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una matriz de delimitadores de degradado y, a continuación, se usan para crear un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



En el siguiente ejemplo de código se usa [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para crear un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D2d1 \_ 1. h (incluir D2d1. h)</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| Archivo DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**D2D1 delimitador de \_ degradado \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[Cómo crear un pincel de degradado lineal](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Cómo crear un pincel de degradado radial](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> </dl>
