---
title: Dibujar y rellenar una forma básica
description: En este tema se describe cómo dibujar una forma básica.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 93d8f3a3ddeb06c9168971789dff3ac8c9222d22
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827004"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Dibujar y rellenar una forma básica

En este tema se describe cómo dibujar una forma básica. La [**interfaz ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) proporciona métodos para delinear y rellenar elipses, rectángulos y líneas. En los ejemplos siguientes se muestra cómo crear y dibujar una elipse.

Este tema contiene las siguientes secciones:

-   [Dibujar el contorno de una elipse con un trazo sólido](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Dibujar una elipse con un trazo discontinuo](#draw-an-ellipse-with-a-dashed-stroke)
-   [Dibujar y rellenar una elipse](#draw-and-fill-an-ellipse)
-   [Dibujar formas más complejas](#drawing-more-complex-shapes)
-   [Temas relacionados](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Dibujar el contorno de una elipse con un trazo sólido

Para dibujar el contorno de una elipse, defina un pincel (por [**ejemplo, ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o [**ID2D1LinearGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)para pintar el contorno y una [**\_ elipse D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) para describir la posición y las dimensiones de la elipse y, a continuación, pasar estos objetos al método [**ID2D1RenderTarget::D raw Insertpse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) En el ejemplo siguiente se crea un pincel de color sólido negro y se almacena en el miembro de clase m \_ spBlackBrush.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



En el ejemplo siguiente se define [**una \_ elipse D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) y se usa con el pincel definido en el ejemplo anterior para dibujar el contorno de una elipse. En este ejemplo se genera la salida que se muestra en la ilustración siguiente.

![ilustración de una elipse con un trazo sólido](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Dibujar una elipse con un trazo discontinuo

En el ejemplo anterior se usó un trazo sin formato. Puede modificar el aspecto de un trazo de varias maneras mediante la creación de [**un ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle). **ID2D1StrokeStyle** permite especificar la forma al principio y al final de un trazo, si tiene un patrón de guion, y así sucesivamente. En el ejemplo siguiente se **crea un id2D1StrokeStyle** que describe un trazo discontinuo. En este ejemplo se usa un patrón de guion predefinido, [**D2D1 \_ DASH STYLE DASH DOT \_ \_ \_ \_ DOT,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)pero también puede especificar el suyo propio.


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



En el ejemplo siguiente se usa el estilo de trazo con el [**método DrawVelopse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) En este ejemplo se genera la salida que se muestra en la ilustración siguiente.

![ilustración de una elipse con un trazo discontinuo](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Dibujar y rellenar una elipse

Para pintar el interior de una elipse, use el [**método FillVelopse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) En el ejemplo siguiente se usa [**el método DrawVelopse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) para esquematear la elipse y, a continuación, se usa el **método FillVelopse** para pintar su interior. En este ejemplo se genera la salida que se muestra en la ilustración siguiente.

![ilustración de una elipse con un trazo discontinuo y, a continuación, rellena con un color gris sólido](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



En el ejemplo siguiente se rellena primero la elipse y, a continuación, se dibuja su contorno. En este ejemplo se genera la salida que se muestra en la ilustración siguiente.

![ilustración de una elipse rellena con un color gris sólido y, a continuación, con un trazo discontinuo](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



En estos ejemplos se ha omitido el código.

## <a name="drawing-more-complex-shapes"></a>Dibujar formas más complejas

Para dibujar formas más complejas, defina objetos ID2D1Geometry y úsenlos con los métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) [**y FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Para obtener más información, vea Información general [sobre geometrías.](direct2d-geometries-overview.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre las geometrías](direct2d-geometries-overview.md)
</dt> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> </dl>

 

 
