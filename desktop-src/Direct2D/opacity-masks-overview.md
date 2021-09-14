---
title: Información general sobre las máscaras de opacidad
description: 'En este tema se describe cómo usar mapas de bits y pinceles para definir máscaras de opacidad. Contiene las siguientes secciones:'
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513365474ed6b1f6f42d34f9b876226e00ba6e85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162669"
---
# <a name="opacity-masks-overview"></a>Información general sobre las máscaras de opacidad

En este tema se describe cómo usar mapas de bits y pinceles para definir máscaras de opacidad. Contiene las siguientes secciones:

-   [Requisitos previos](#prerequisites)
-   [¿Qué es una máscara de opacidad?](#what-is-an-opacity-mask)
-   [Usar un mapa de bits como máscara de opacidad con el método FillOpacityMask](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Usar un pincel como máscara de opacidad con el método FillGeometry](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Usar un pincel de degradado lineal como máscara de opacidad](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Usar un pincel de degradado radial como máscara de opacidad](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Aplicar una máscara de opacidad a una capa](#apply-an-opacity-mask-to-a-layer)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En esta introducción se da por supuesto que está familiarizado con las operaciones básicas de dibujo de Direct2D, como se describe en el tutorial Creación de una aplicación [direct2D](direct2d-quickstart.md) simple. También debe estar familiarizado con los distintos tipos de pinceles, como se describe en Información general [sobre pinceles.](direct2d-brushes-overview.md)

## <a name="what-is-an-opacity-mask"></a>¿Qué es una máscara de opacidad?

Una máscara de opacidad es una máscara, descrita por un pincel o mapa de bits, que se aplica a otro objeto para que ese objeto sea parcial o completamente transparente. Una máscara de opacidad usa información de canal alfa para especificar cómo se combinan los píxeles de origen del objeto en el destino final. Las partes transparentes de la máscara indican las áreas donde está oculta la imagen subyacente, mientras que las partes opacas de la máscara indican dónde está visible el objeto enmascarado.

Hay varias maneras de aplicar una máscara de opacidad:

-   Use el [**método ID2D1RenderTarget::FillOpacityMask.**](id2d1rendertarget-fillopacitymask.md) El **método FillOpacityMask** pinta una región rectangular de un destino de representación y, a continuación, aplica una máscara de opacidad, definida por un mapa de bits. Use este método cuando la máscara de opacidad sea un mapa de bits y desee rellenar una región rectangular.
-   Use el [**método ID2D1RenderTarget::FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) El **método FillGeometry** pinta el interior de geometry con el [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)especificado y, a continuación, aplica una máscara de opacidad, definida por un pincel. Use este método cuando desee aplicar una máscara de opacidad a una geometría o desee usar un pincel como máscara de opacidad.
-   Use [**id2D1Layer para**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) aplicar una máscara de opacidad. Use este enfoque cuando desee aplicar una máscara de opacidad a un grupo de contenido de dibujo, no solo una sola forma o imagen. Para más información, consulte Información general [sobre capas.](direct2d-layers-overview.md)

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Usar un mapa de bits como máscara de opacidad con el método FillOpacityMask

El [**método FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) pinta una región rectangular de un destino de representación y, a continuación, aplica una máscara de opacidad, definida por [**un ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap). Use este método cuando tenga un mapa de bits que desee usar como máscara de opacidad para una región rectangular.

En el diagrama siguiente se muestra un efecto de aplicar la máscara de opacidad [**(id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con una imagen de una flor) a un [**objeto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con una imagen de una planta de plantas. La imagen resultante es un mapa de bits de una planta recortada a la forma de la flor.

![diagrama de un mapa de bits de flor usado como máscara de opacidad en una imagen de una planta de flores](images/brushes-ovw-bitmapopacity.png)

En los ejemplos de código siguientes se muestra cómo se logra esto.

En el primer ejemplo se carga el siguiente mapa de bits, *m \_ pBitmapMask,* para su uso como máscara de mapa de bits. En la ilustración siguiente se muestra la salida que se genera. Tenga en cuenta que, aunque la parte opaca del mapa de bits aparece en negro, la información de color del mapa de bits no tiene ningún efecto en la máscara de opacidad; solo se usa la información de opacidad de cada píxel del mapa de bits. Los píxeles totalmente opacos de este mapa de bits se han coloreado en negro solo con fines ilustrativos.

![ilustración de la máscara de mapa de bits de flor](images/bitmapmask.png)

En este ejemplo, [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) se carga mediante un método auxiliar, LoadResourceBitmap, definido en otra parte del ejemplo.


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



En el ejemplo siguiente se define el *pincel, m \_ pFernBitmapBrush*, al que se aplica la máscara de opacidad. En este ejemplo se usa [**un objeto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que contiene una imagen de un árbol, pero podría usar [**id2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)o [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) en su lugar. En la ilustración siguiente se muestra la salida que se genera.

![ilustración del mapa de bits utilizado por el pincel de mapa de bits](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





Ahora que la máscara de opacidad y el pincel están definidos, puede usar el [**método FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) en el método de representación de la aplicación. Al llamar al método **FillOpacityMask,** debe especificar el tipo de máscara de opacidad que usa: **D2D1 \_ OPACITY \_ MASK CONTENT \_ \_ GRAPHICS,** **D2D1 \_ OPACITY MASK CONTENT \_ TEXT \_ \_ \_ NATURAL** y **D2D1 \_ OPACITY MASK CONTENT TEXT \_ \_ \_ \_ GDI \_ COMPATIBLE.** Para obtener los significados de estos tres tipos, vea [**D2D1 \_ OPACITY \_ MASK \_ CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> A partir Windows 8, el contenido de [**la máscara de opacidad D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) no es necesario. Vea el [**método ID2D1DeviceContext::FillOpacityMask,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) que no tiene ningún parámetro **\_ OPACITY \_ MASK \_ CONTENT de D2D1.**

 

En el ejemplo siguiente se establece el modo de suavizado de contorno del destino de representación en [**D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) para que la máscara de opacidad funcione correctamente. A continuación, llama al método [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) y le pasa la máscara de opacidad *(m \_ pBitmapMask),* el pincel al que se aplica la máscara de opacidad *(m \_ pFernBitmapBrush),* el tipo de contenido dentro de la máscara de opacidad [**(D2D1 \_ OPACITY \_ MASK CONTENT \_ \_ GRAPHICS)**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)y el área que se va a pintar. En la ilustración siguiente se muestra la salida que se genera.

![ilustración de la imagen de la planta de plant con una máscara de opacidad aplicada](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





El código se ha omitido en este ejemplo.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Usar un pincel como máscara de opacidad con el método FillGeometry

En la sección anterior se describe cómo usar [**id2D1Bitmap como**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) máscara de opacidad. Direct2D también proporciona el método [**ID2D1RenderTarget::FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) que permite especificar opcionalmente el pincel como máscara de opacidad al rellenar un [**id2D1Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) Esto le permite crear máscaras de opacidad a partir de degradados (mediante [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) o [**ID2D1RadialGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)y mapas de bits (mediante **ID2D1Bitmap).**

El [**método FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) toma tres parámetros:

-   El primer parámetro, [**id2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)define la forma que se debe pintar.
-   El segundo parámetro, [**id2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)especifica el pincel que se usa para pintar la geometría. Este parámetro debe ser [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) que tenga sus modos de extensión x e y establecidos en [**D2D1 \_ EXTEND MODE \_ \_ CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).
-   El tercer parámetro, [**id2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)especifica un pincel que se usará como máscara de opacidad. Este pincel puede ser [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)o [**ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (Técnicamente, puede usar [**id2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)pero el uso de un pincel de color sólido como máscara de opacidad no genera resultados interesantes).

En las secciones siguientes se describe cómo usar los objetos [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) e [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) como máscaras de opacidad.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Usar un pincel de degradado lineal como máscara de opacidad

En el diagrama siguiente se muestra el efecto de aplicar un pincel de degradado lineal a un rectángulo que se rellena con un mapa de bits de flores.

![diagrama de un mapa de bits de flor con un pincel de degradado lineal aplicado](images/brushes-ovw-lineargradient-opacitymask.png)

Los pasos siguientes describen cómo volver a crear este efecto.

1.  Defina el contenido que se va a enmascarar. En el ejemplo siguiente se crea [**un objeto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap*. El modo de extensión x- e y- para *m \_ pLinearFadeFlowersBitmap* se establece en [**D2D1 \_ EXTEND MODE \_ \_ CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) para que el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) pueda usarlo con una máscara de opacidad.

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    
    <table>
    <colgroup>
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    
    <table>
    <colgroup>
    <col  />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  Defina la máscara de opacidad. En el ejemplo de código siguiente se crea un pincel de degradado lineal diagonal *(m \_ pLinearGradientBrush)* que se atenua de negro totalmente opaco en la posición 0 a blanco completamente transparente en la posición 1.
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  Use el [**método FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) En el ejemplo final se usa el método **FillGeometry** al pincel de contenido para rellenar un [**id2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) con [**un id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) y se aplica una máscara de opacidad (*m \_ pLinearGradientBrush*).
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

El código se ha omitido en este ejemplo.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Usar un pincel de degradado radial como máscara de opacidad

En el diagrama siguiente se muestra el efecto visual de aplicar un pincel de degradado radial a un rectángulo que se rellena con un mapa de bits de foliage.

![diagrama de un mapa de bits de foliage con un pincel de degradado radial aplicado](images/brushes-ovw-radialgradient-opacitymask.png)

En el primer ejemplo se [**crea un objeto ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush*. Para que se pueda usar con una máscara de opacidad mediante el método [**FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) el modo de extensión x- e y- para *m \_ pRadialFadeFlowersBitmapBrush* se establece en [**D2D1 \_ EXTEND MODE \_ \_ CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```





<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



En el ejemplo siguiente se define el pincel de degradado radial que se usará como máscara de opacidad.


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





En el ejemplo de código final se usa [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) y la máscara de opacidad (*m \_ pRadialGradientBrush*) para rellenar [**un id2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*).


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



El código se ha omitido en este ejemplo.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Aplicar una máscara de opacidad a una capa

Al llamar a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) para insertar un [**elemento ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) en un destino de representación, puede usar la estructura DE PARÁMETROS DE CAPA [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para aplicar un pincel como máscara de opacidad. En el ejemplo de código siguiente se [**usa id2D1RadialGradientBrush como**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) máscara de opacidad.


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



Para obtener más información sobre el uso de capas, vea Información general [sobre capas.](direct2d-layers-overview.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre los pinceles](direct2d-brushes-overview.md)
</dt> <dt>

[Información general sobre capas](direct2d-layers-overview.md)
</dt> </dl>

 

 
