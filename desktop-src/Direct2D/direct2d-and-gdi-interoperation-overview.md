---
title: Introducción a la interoperabilidad de Direct2D y GDI
description: Describe cómo usar Direct2D y GDI juntos.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, interoperación GDI
- Direct2D, interoperabilidad
- interoperabilidad, Direct2D
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- Direct3D, interoperabilidad
- Interoperación de Direct3D,Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf75f68278bdead5f3806eefd1cda251bfbea4a
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122787401"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Introducción a la interoperabilidad de Direct2D y GDI

En este tema se describe cómo usar Direct2D y [GDI juntos.](/windows/desktop/gdi/windows-gdi) Hay dos maneras de combinar Direct2D con GDI: puede escribir contenido GDI en un destino de representación compatible con GDI de Direct2D o escribir contenido de Direct2D en un contexto de dispositivo [GDI (DC).](/windows/desktop/gdi/device-contexts)

En este tema se incluyen las siguientes secciones.

-   [Requisitos previos](#prerequisites)
-   [Dibujar contenido direct2D en un contexto de dispositivo GDI](#draw-direct2d-content-to-a-gdi-device-context)
-   [ID2D1DCRenderTargets, transformaciones GDI y compilaciones de lenguaje de derecha a izquierda de Windows](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [Dibujar contenido GDI en un destino de representación GDI-Compatible Direct2D](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En esta introducción se supone que está familiarizado con las operaciones básicas de dibujo de Direct2D. Para ver un tutorial, consulte la [guía de inicio rápido de Direct2D.](direct2d-quickstart.md) También se supone que está familiarizado con las operaciones de dibujo de GDI.

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>Dibujar contenido direct2D en un contexto de dispositivo GDI

Para dibujar contenido de Direct2D en un controlador de dominio de GDI, use un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget). Para crear un destino de representación de controlador de dominio, use el [**método ID2D1Factory::CreateDCRenderTarget.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) Este método toma dos parámetros.

El primer parámetro, una estructura [**\_ RENDER TARGET \_ \_ PROPERTIES de D2D1,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) especifica la representación, comunicación remota, PPP, formato de píxel e información de uso. Para permitir que el destino de representación de controlador de dominio funcione con GDI, establezca el formato DXGI en [DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) y el modo alfa en [**D2D1 \_ ALPHA MODE \_ \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o **D2D1 \_ ALPHA MODE \_ \_ IGNORE**.

El segundo parámetro es la dirección del puntero que recibe la referencia de destino de representación del controlador de dominio.

El código siguiente crea un destino de representación de controlador de dominio.


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



En el código anterior, *m \_ pD2DFactory* es un puntero a [**id2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)y *m \_ pDCRT* es un puntero a [**id2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).

Para poder representar con el destino de representación del controlador de dominio, debe usar su [**método BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) para asociarlo a un controlador de dominio de GDI. Esto se hace cada vez que se usa un controlador de dominio diferente o el tamaño del área que se quiere dibujar en los cambios.

El [**método BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) toma dos parámetros, *hDC* y *pSubRect.* El *parámetro hDC* proporciona un identificador al contexto del dispositivo que recibe la salida del destino de representación. El *parámetro pSubRect* es un rectángulo que describe la parte del contexto del dispositivo en el que se representa el contenido. El destino de representación del controlador de dominio actualiza su tamaño para que coincida con el área de contexto del dispositivo descrita por *pSubRect,* en caso de que cambie de tamaño.

El código siguiente enlaza un controlador de dominio a un destino de representación de controlador de dominio.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
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
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



Después de asociar el destino de representación del controlador de dominio a un controlador de dominio, puede usarlo para dibujar. El código siguiente dibuja contenido de Direct2D y GDI mediante un controlador de dominio.


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Este código genera salidas como se muestra en la ilustración siguiente (se han agregado llamadas para resaltar la diferencia entre la representación de Direct2D y GDI).

![ilustración de dos gráficos circulares representados con direct2d y gdi](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>ID2D1DCRenderTargets, transformaciones GDI y compilaciones de lenguaje de derecha a izquierda de Windows

Cuando se usa [**un ID2D1DCRenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)representa el contenido de Direct2D en un mapa de bits interno y, a continuación, representa el mapa de bits en el controlador de dominio con GDI.

Es posible que GDI aplique una transformación GDI (a través del método [**SetWorldTransform)**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) u otro efecto al mismo controlador de dominio que usa el destino de representación, en cuyo caso GDI transforma el mapa de bits generado por Direct2D. El uso de una transformación GDI para transformar el contenido de Direct2D tiene la posibilidad de degradar la calidad visual de la salida, ya que se está transformando un mapa de bits para el que ya se han calculado el suavizado de contorno y el posicionamiento de subpixel.

Por ejemplo, supongamos que usa el destino de representación para dibujar una escena que contiene geometrías suavizadas y texto. Si usa una transformación GDI para aplicar una transformación de escala al controlador de dominio y escalar la escena para que sea 10 veces mayor, verá la pixelización y los bordes irregulares. (Sin embargo, si aplicara una transformación similar mediante Direct2D, la calidad visual de la escena no se degradaría).

En algunos casos, es posible que no sea obvio que GDI está realizando un procesamiento adicional que podría degradar la calidad del contenido de Direct2D. Por ejemplo, en una compilación de derecha a izquierda (RTL) de Windows, el contenido representado por [**un ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) podría invertirse horizontalmente cuando GDI lo copia en su destino. Si el contenido se invierte realmente depende de la configuración actual del controlador de dominio.

En función del tipo de contenido que se represente, es posible que desee evitar la inversión. Si el contenido de Direct2D incluye texto ClearType, esta inversión degradará la calidad del texto.

Puede controlar el comportamiento de representación de RTL mediante la [**función SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI. Para evitar la creación de reflejo, llame a la función **GDI SetLayout** y especifique **LAYOUT \_ BITMAPORIENTATIONPRESERVED como** único valor para el segundo parámetro (no lo combine con LAYOUT **\_ RTL),** como se muestra en el ejemplo siguiente:


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>Dibujar contenido GDI en un destino de representación GDI-Compatible Direct2D

En la sección anterior se describe cómo escribir contenido de Direct2D en un controlador de dominio de GDI. También puede escribir contenido GDI en un destino de representación compatible con GDI de Direct2D. Este enfoque es útil para las aplicaciones que se representan principalmente con Direct2D pero tienen un modelo de extensibilidad u otro contenido heredado que requiere la capacidad de representar con GDI.

Para representar contenido GDI en un destino de representación compatible con GDI de Direct2D, use un [**id2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), que proporciona acceso a un contexto de dispositivo que puede aceptar llamadas a draw de GDI. A diferencia de otras interfaces, **un objeto ID2D1GdiInteropRenderTarget** no se crea directamente. En su lugar, use [**el método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de una instancia de destino de representación existente. El código siguiente muestra cómo hacerlo:


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



En el código anterior, *m \_ pD2DFactory* es un puntero a [**id2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)y *m \_ pGDIRT* es un puntero a [**id2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).

Tenga en cuenta que se especifica la marca [**\_ COMPATIBLE con \_ \_ \_ GDI \_ RENDER TARGET USAGE de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) al crear el destino de representación compatible con Hwnd GDI. Si se requiere un formato de píxel, use [DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format). Si se requiere un modo alfa, use [**D2D1 \_ ALPHA \_ MODE \_ PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) o **D2D1 \_ ALPHA MODE \_ \_ IGNORE**.

Tenga en cuenta que [**el método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) siempre se realiza correctamente. Para probar si los métodos de la interfaz [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) funcionarán para un destino de representación determinado, cree una clase [**RENDER TARGET \_ \_ \_ PROPERTIES de D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que especifique la compatibilidad con GDI y el formato de píxel adecuado y, a continuación, llame al método [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) del destino de representación para ver si el destino de representación es compatible con GDI.

En el ejemplo siguiente se muestra cómo dibujar un gráfico circular (contenido GDI) en el destino de representación compatible con Hwnd GDI.


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



El código genera gráficos como se muestra en la ilustración siguiente con llamadas para resaltar la diferencia de calidad de la representación. El gráfico circular derecho (contenido GDI) tiene una calidad de representación inferior a la del gráfico circular izquierdo (contenido de Direct2D). Esto se debe a que Direct2D es capaz de representarse con suavizado de contorno

![ilustración de dos gráficos circulares representados en un destino de representación compatible con gdi de Direct2d](images/gdicontentind2d.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**PROPIEDADES DE DESTINO DE REPRESENTACIÓN D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[Contextos de dispositivo GDI](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[GDI SDK](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 
