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
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="2662e-103">Cómo recortar a una máscara geométrica</span><span class="sxs-lookup"><span data-stu-id="2662e-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="2662e-104">En este tema se describe cómo usar una máscara geométrica para recortar una región de una capa.</span><span class="sxs-lookup"><span data-stu-id="2662e-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="2662e-105">**Para recortar una región con una máscara geométrica**</span><span class="sxs-lookup"><span data-stu-id="2662e-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="2662e-106">Cree el [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) que se usará para recortar la región.</span><span class="sxs-lookup"><span data-stu-id="2662e-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="2662e-107">Llame a [**ID2D1RenderTarget:: CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear una capa.</span><span class="sxs-lookup"><span data-stu-id="2662e-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="2662e-108">Llame a [**ID2D1RenderTarget::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) y pase la máscara geométrica que definió en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="2662e-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="2662e-109">Dibuje el contenido en clip.</span><span class="sxs-lookup"><span data-stu-id="2662e-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="2662e-110">Llame a [**ID2D1RenderTarget::P OPlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para quitar la capa del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="2662e-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="2662e-111">En el ejemplo siguiente se usa una máscara geométrica para recortar una imagen y varios rectángulos.</span><span class="sxs-lookup"><span data-stu-id="2662e-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="2662e-112">En la ilustración siguiente se muestra el mapa de bits original de la izquierda y el mapa de bits recortado a la máscara geométrica de la derecha.</span><span class="sxs-lookup"><span data-stu-id="2662e-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![Ilustración de un mapa de bits de pez antes y después de que el mapa de bits se recorte a una máscara en forma de estrella](images/cliparegion-layers.png)

<span data-ttu-id="2662e-114">Para recortar el dibujo como se muestra en la ilustración anterior, cree un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) y úselo para definir una estrella.</span><span class="sxs-lookup"><span data-stu-id="2662e-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="2662e-115">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="2662e-115">The following code shows how to do this.</span></span>


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



<span data-ttu-id="2662e-116">Llame a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear una capa.</span><span class="sxs-lookup"><span data-stu-id="2662e-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="2662e-117">A partir de Windows 8, no es necesario llamar a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="2662e-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="2662e-118">En la mayoría de los casos, el rendimiento es mejor si no se llama a este método y Direct2D administra los recursos de la capa.</span><span class="sxs-lookup"><span data-stu-id="2662e-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="2662e-119">Llame a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) con la máscara de geometría para extender la capa.</span><span class="sxs-lookup"><span data-stu-id="2662e-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="2662e-120">Dibuje el contenido en clip y, a continuación, llame a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para extraer la capa.</span><span class="sxs-lookup"><span data-stu-id="2662e-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="2662e-121">Esto produce el dibujo en forma de estrella.</span><span class="sxs-lookup"><span data-stu-id="2662e-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="2662e-122">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="2662e-122">The following code shows how to do this.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2662e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2662e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2662e-124">Información general sobre capas</span><span class="sxs-lookup"><span data-stu-id="2662e-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="2662e-125">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="2662e-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 