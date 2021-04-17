---
title: Cómo dibujar texto
description: Muestra cómo representar texto con Direct2D.
ms.assetid: 914dd9d0-78c8-44a3-8504-837faf3201d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30f15704673c63c4bf44a31c64843250cceafd4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421200"
---
# <a name="how-to-draw-text"></a>Cómo dibujar texto

Para dibujar texto con Direct2D, use el método [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) para el texto que tiene un único formato. O bien, use el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para varios formatos, características OpenType avanzadas o pruebas de posicionamiento. Estos métodos usan la API de DirectWrite para proporcionar una presentación de texto de alta calidad.

## <a name="the-drawtext-method"></a>El método DrawText

Para dibujar texto con un solo formato, use el método [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) . Para usar este método, use primero un [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) para crear una instancia de [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) .

El siguiente código crea un objeto [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y lo almacena en la *variable \_ pTextFormat m* .


```C++
// Create resources which are not bound
// to any device. Their lifetime effectively extends for the
// duration of the app. These resources include the Direct2D and
// DirectWrite factories,  and a DirectWrite Text Format object
// (used for identifying particular font characteristics).
//
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    static const WCHAR msc_fontName[] = L"Verdana";
    static const FLOAT msc_fontSize = 50;
    HRESULT hr;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pD2DFactory);

    if (SUCCEEDED(hr))
    {
        
        // Create a DirectWrite factory.
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(m_pDWriteFactory),
            reinterpret_cast<IUnknown **>(&m_pDWriteFactory)
            );
    }
    if (SUCCEEDED(hr))
    {
        // Create a DirectWrite text format object.
        hr = m_pDWriteFactory->CreateTextFormat(
            msc_fontName,
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            msc_fontSize,
            L"", //locale
            &m_pTextFormat
            );
    }
    if (SUCCEEDED(hr))
    {
        // Center the text horizontally and vertically.
        m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        m_pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
       

    }

    return hr;
}
```



Dado que los objetos [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) y [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) son [recursos independientes del dispositivo](resources-and-resource-domains.md), puede mejorar el rendimiento de una aplicación creando solo una vez, en lugar de volver a crearlos cada vez que se representa un fotograma.

Después de crear el objeto de formato de texto, puede utilizarlo con un destino de representación. El código siguiente dibuja el texto mediante el método [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) del destino de representación (la variable *m \_ pRenderTarget* ).


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="the-drawtextlayout-method"></a>El método DrawTextLayout

El método [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) representa un objeto [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Utilice este método para aplicar varios formatos a un bloque de texto (como el subrayado de una parte del texto), para usar las características OpenType avanzadas o para realizar la prueba de posicionamiento.

El método [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) también proporciona ventajas de rendimiento para dibujar el mismo texto varias veces. El objeto [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) mide y coloca el texto al crearlo. Si crea un objeto **IDWriteTextLayout** solo una vez y lo vuelve a usar cada vez que tiene que volver a dibujar el texto, el rendimiento mejora porque el sistema no tiene que medir y diseñar el texto de nuevo.

Antes de poder usar el método [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , debe usar un [**IDWriteFactory**](/windows/desktop/api/dwrite/nn-dwrite-idwritefactory) para crear objetos [**IDWriteTextFormat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Una vez creados estos objetos, llame al método **DrawTextLayout** .

Para obtener más información y ejemplos, vea información general sobre el [diseño y el formato de texto](/windows/desktop/DirectWrite/text-formatting-and-layout) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))
</dt> <dt>

[**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[Formato y diseño de texto](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

 