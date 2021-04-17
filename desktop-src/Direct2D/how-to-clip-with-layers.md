---
title: Cómo recortar a una máscara geométrica
description: Muestra cómo recortar una región con capas.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488026"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>Cómo recortar a una máscara geométrica

En este tema se describe cómo usar una máscara geométrica para recortar una región de una capa.

**Para recortar una región con una máscara geométrica**

1.  Cree el [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) que se usará para recortar la región.
2.  Llame a [**ID2D1RenderTarget:: CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear una capa.
3.  Llame a [**ID2D1RenderTarget::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y pase la máscara geométrica que definió en el paso 1.
4.  Dibuje el contenido en clip.
5.  Llame a [**ID2D1RenderTarget::P OPlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para quitar la capa del destino de representación.

En el ejemplo siguiente se usa una máscara geométrica para recortar una imagen y varios rectángulos. En la ilustración siguiente se muestra el mapa de bits original de la izquierda y el mapa de bits recortado a la máscara geométrica de la derecha.

![Ilustración de un mapa de bits de pez antes y después de que el mapa de bits se recorte a una máscara en forma de estrella](images/cliparegion-layers.png)

Para recortar el dibujo como se muestra en la ilustración anterior, cree un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y úselo para definir una estrella. El código siguiente muestra cómo hacerlo.


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



Llame a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear una capa.

> [!Note]  
> A partir de Windows 8, no es necesario llamar a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)). En la mayoría de los casos, el rendimiento es mejor si no se llama a este método y Direct2D administra los recursos de la capa.

 

Llame a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) con la máscara de geometría para extender la capa. Dibuje el contenido en clip y, a continuación, llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para extraer la capa. Esto produce el dibujo en forma de estrella. El código siguiente muestra cómo hacerlo.


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre capas](direct2d-layers-overview.md)
</dt> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 