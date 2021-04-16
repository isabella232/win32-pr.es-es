---
title: Inicio rápido de Direct2D para Windows 8
description: Resume los pasos necesarios para dibujar con Direct2D y proporciona código de ejemplo.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Ejemplo de código de rectángulo de Direct2D, dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656371"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Inicio rápido de Direct2D para Windows 8

Direct2D es una API de modo inmediato y de código nativo para crear gráficos 2D. En este tema se muestra cómo usar Direct2D para dibujar en [**Windows:: UI:: Core:: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

Este tema contiene las siguientes secciones:

-   [Dibujar un rectángulo simple](#drawing-a-simple-rectangle)
-   [Paso 1: incluir el encabezado de Direct2D](#step-1-include-direct2d-header)
-   [Paso 2: creación de un ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Paso 3: creación de un ID2D1Device y un ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Paso 4: crear un pincel](#step-4-create-a-brush)
-   [Paso 5: dibujo del rectángulo](#step-5-draw-the-rectangle)
-   [Ejemplo de código](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Dibujar un rectángulo simple

Para dibujar un rectángulo mediante [GDI](/windows/desktop/gdi/windows-gdi), podría controlar el mensaje [**de \_ dibujo de WM**](/windows/desktop/gdi/wm-paint) , tal y como se muestra en el código siguiente.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo. En las secciones siguientes se describe detalladamente cada uno de estos pasos.

## <a name="step-1-include-direct2d-header"></a>Paso 1: incluir el encabezado de Direct2D

Además de los encabezados necesarios para la aplicación, incluya los encabezados d2d1. h y d2d1 \_ 1. h.

## <a name="step-2-create-an-id2d1factory1"></a>Paso 2: creación de un ID2D1Factory1

Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear un [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



La interfaz [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) es el punto de partida para usar Direct2D; Use un **ID2D1Factory1** para crear recursos de Direct2D.

Al crear una factoría, puede especificar si es multiproceso o de un solo subproceso. (Para obtener más información sobre los generadores multiproceso, consulte la sección Comentarios en la [**Página de referencia de ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)). En este ejemplo se crea un generador de un solo subproceso.

En general, la aplicación debe crear el generador una vez y conservarlo durante la vida de la aplicación.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Paso 3: creación de un ID2D1Device y un ID2D1DeviceContext

Después de crear un generador, úselo para crear un dispositivo de Direct2D y, a continuación, use el dispositivo para crear un contexto de dispositivo de Direct2D. Para crear estos objetos de Direct2D, debe tener un [**dispositivo Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , un [**dispositivo dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)y una [**cadena de intercambio de dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1). Consulte [dispositivos y contextos de dispositivos](devices-and-device-contexts.md) para obtener información sobre cómo crear los requisitos previos necesarios.


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Un contexto de dispositivo es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como los pinceles. También se usa el contexto de dispositivo para vincular un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a una superficie de DXGI que se va a usar como destino de representación. El contexto del dispositivo se puede representar en diferentes tipos de destinos.

El código que se muestra aquí declara las propiedades para el mapa de bits que se vincula a una cadena de intercambio de DXGI que se representa en [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow). El método [**ID2D1DeviceContext:: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) obtiene una superficie de Direct2D de la superficie de DXGI. Esto hace que todo lo que se represente en el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de destino se represente en la superficie de la cadena de intercambio.

Una vez que tenga la superficie de Direct2D, use el método [**ID2D1DeviceContext:: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) para establecerla como destino de representación activo.


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>Paso 4: crear un pincel

Al igual que un generador, un contexto de dispositivo puede crear recursos de dibujo. En este ejemplo, el contexto de dispositivo crea un pincel.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Un pincel es un objeto que pinta un área, como el trazo de una forma o el relleno de una geometría. El pincel de este ejemplo pinta un área con un color sólido predefinido, negro.

Direct2D también proporciona otros tipos de pinceles: pinceles de degradado para pintar degradados lineales y radiales, un [**pincel de mapa de bits**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintar con mapas de bits y patrones, y a partir de Windows 8, un pincel de [**imagen**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) para pintar con una imagen representada.

Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas. Direct2D es diferente: no proporciona un objeto Pen, sino que usa un pincel para dibujar contornos y formas de relleno. Al dibujar contornos, utilice la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) o a partir de la interfaz [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) de Windows 8 con un pincel para controlar las operaciones de trazado de trazado.

Un pincel solo se puede usar con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos. En general, debe crear pinceles una vez y conservarlos durante la vida del destino de representación que los creó. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) es la única excepción; Dado que es relativamente económico crearlo, puede crear un **ID2D1SolidColorBrush** cada vez que dibuje un fotograma, sin que se produzca ningún impacto apreciable en el rendimiento. También puede usar una sola **ID2D1SolidColorBrush** y simplemente cambiar su color o opacidad cada vez que la use.

## <a name="step-5-draw-the-rectangle"></a>Paso 5: dibujo del rectángulo

A continuación, use el contexto de dispositivo para dibujar el rectángulo.


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



El método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo. Opcionalmente, también puede especificar las opciones ancho del trazo, patrón de guión, combinación de líneas y límite final.

Debe llamar al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir cualquier comando de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo. El método **EndDraw** devuelve un **valor HRESULT** que indica si los comandos de dibujo se realizaron correctamente. Si no se realiza correctamente, la función auxiliar ThrowIfFailed producirá una excepción.

El método [**IDXGISwapChain::P reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) intercambia la superficie del búfer con la superficie de la pantalla para mostrar el resultado.

## <a name="example-code"></a>Ejemplo de código

En el código de este tema se muestran los elementos básicos de una aplicación de Direct2D. Por motivos de brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característico de una aplicación bien escrita.

 

 