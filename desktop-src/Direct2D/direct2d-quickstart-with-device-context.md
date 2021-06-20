---
title: Inicio rápido de Direct2D para Windows 8
description: Resume los pasos necesarios para dibujar con Direct2D para Windows 8 y proporciona código de ejemplo. Direct2D es una API de código nativo para crear gráficos 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, ejemplo de código de rectángulo de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406148"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Inicio rápido de Direct2D para Windows 8

Direct2D es una API en modo inmediato de código nativo para crear gráficos 2D. En este tema se muestra cómo usar Direct2D para dibujar en [**windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).

Este tema contiene las siguientes secciones:

-   [Dibujar un rectángulo simple](#drawing-a-simple-rectangle)
-   [Paso 1: Incluir encabezado Direct2D](#step-1-include-direct2d-header)
-   [Paso 2: Crear un id2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Paso 3: Crear un ID2D1Device y un ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Paso 4: Crear un pincel](#step-4-create-a-brush)
-   [Paso 5: Dibujar el rectángulo](#step-5-draw-the-rectangle)
-   [Ejemplo de código](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Dibujar un rectángulo simple

Para dibujar un rectángulo mediante [GDI,](/windows/desktop/gdi/windows-gdi)puede controlar el [**mensaje WM \_ PAINT,**](/windows/desktop/gdi/wm-paint) como se muestra en el código siguiente.


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



El código para dibujar el mismo rectángulo con Direct2D es similar: crea recursos de dibujo, describe una forma para dibujar, dibuja la forma y, a continuación, libera los recursos de dibujo. En las secciones siguientes se describe cada uno de estos pasos con detalle.

## <a name="step-1-include-direct2d-header"></a>Paso 1: Incluir encabezado Direct2D

Además de los encabezados necesarios para la aplicación, incluya los encabezados d2d1.h y d2d1 \_ 1.h.

## <a name="step-2-create-an-id2d1factory1"></a>Paso 2: Crear un id2D1Factory1

Una de las primeras cosas que hace cualquier ejemplo de Direct2D es crear un [**id2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).


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



La [**interfaz ID2D1Factory1 es**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) el punto de partida para usar Direct2D; use un **id2D1Factory1 para** crear recursos de Direct2D.

Al crear un generador, puede especificar si es multiproceso o de subproceso único. (Para obtener más información sobre factorías multiproceso, vea los comentarios en la página de referencia [**de ID2D1Factory).**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) En este ejemplo se crea un generador de un solo subproceso.

En general, la aplicación debe crear el generador una vez y conservarlo durante la vida útil de la aplicación.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Paso 3: Crear un ID2D1Device y un ID2D1DeviceContext

Después de crear un generador, úselo para crear un dispositivo Direct2D y, a continuación, use el dispositivo para crear un contexto de dispositivo Direct2D. Para crear estos objetos de Direct2D, debe tener un dispositivo [**Direct3D 11,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) un dispositivo [**DXGI**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)y una [**cadena de intercambio DXGI**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1). Consulte [Devices and Device Contexts (Dispositivos y contextos de dispositivo)](devices-and-device-contexts.md) para obtener información sobre cómo crear los requisitos previos necesarios.


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



Un contexto de dispositivo es un dispositivo que puede realizar operaciones de dibujo y crear recursos de dibujo dependientes del dispositivo, como pinceles. También se usa el contexto del dispositivo para vincular [**id2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) a una superficie DXGI para usarla como destino de representación. El contexto del dispositivo se puede representar en diferentes tipos de destinos.

El código aquí declara las propiedades del mapa de bits que se vincula a una cadena de intercambio DXGI que se representa en [**una instancia de CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow) El [**método ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) obtiene una superficie direct2D de la superficie DXGI. Esto hace que todo lo que se represente en el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) de destino se represente en la superficie de la cadena de intercambio.

Una vez que tenga la superficie de Direct2D, use el método [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) para establecerla como destino de representación activo.


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



## <a name="step-4-create-a-brush"></a>Paso 4: Crear un pincel

Al igual que un generador, un contexto de dispositivo puede crear recursos de dibujo. En este ejemplo, el contexto del dispositivo crea un pincel.


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

Direct2D también proporciona otros tipos de pinceles: pinceles de [](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) degradado para pintar degradados lineales y radiales, un [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) pincel de mapa de bits para pintar con mapas de bits y patrones, y a partir de Windows 8, un pincel de imagen para pintar con una imagen representado.

Algunas API de dibujo proporcionan lápices para dibujar contornos y pinceles para rellenar formas. Direct2D es diferente: no proporciona un objeto de lápiz, sino que usa un pincel para dibujar contornos y rellenar formas. Al dibujar contornos, use la interfaz [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) o a partir de Windows 8 la interfaz [**ID2D1StrokeStyle1,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) con un pincel para controlar las operaciones de trazado de ruta de acceso.

Solo se puede usar un pincel con el destino de representación que lo creó y con otros destinos de representación en el mismo dominio de recursos. En general, debe crear pinceles una vez y conservarlos durante la vida del destino de representación que los creó. [**ID2D1SolidColorBrush es**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) la única excepción; Dado que es relativamente económico crearlo, puede crear un **objeto ID2D1SolidColorBrush** cada vez que dibuje un marco, sin que se note ningún impacto en el rendimiento. También puede usar un único **ID2D1SolidColorBrush** y cambiar su color u opacidad cada vez que lo use.

## <a name="step-5-draw-the-rectangle"></a>Paso 5: Dibujar el rectángulo

A continuación, use el contexto del dispositivo para dibujar el rectángulo.


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



El [**método DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) toma dos parámetros: el rectángulo que se va a dibujar y el pincel que se va a usar para pintar el contorno del rectángulo. Opcionalmente, también puede especificar el ancho del trazo, el patrón de guiones, la combinación de línea y las opciones de extremo.

Debe llamar al [**método BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) antes de emitir los comandos de dibujo y debe llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) una vez que haya terminado de emitir comandos de dibujo. El **método EndDraw** devuelve **un valor HRESULT** que indica si los comandos de dibujo se han realizado correctamente. Si no se realiza correctamente, la función auxiliar ThrowIfFailed producirá una excepción.

El [**método IDXGISwapChain::P resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) intercambia la superficie del búfer con la superficie en pantalla para mostrar el resultado.

## <a name="example-code"></a>Ejemplo de código

El código de este tema muestra los elementos básicos de una aplicación de Direct2D. Por brevedad, el tema omite el marco de trabajo de la aplicación y el código de control de errores que es característica de una aplicación bien escrita.

 

 