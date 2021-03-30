---
title: Crear una aplicación de Direct2D simple
description: Le guía por el proceso de creación de una ventana que representa el contenido de Direct2D.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, tutorial
- Direct2D, tutorial
- Direct2D, creación de aplicaciones
- Direct2D, aplicaciones
- aplicaciones para Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104554081"
---
# <a name="creating-a-simple-direct2d-application"></a>Crear una aplicación de Direct2D simple

Este tema le guía por el proceso de creación de la clase DemoApp, que crea una ventana y utiliza Direct2D para dibujar una cuadrícula y dos rectángulos. En este tutorial, aprenderá a crear recursos de Direct2D y a dibujar formas básicas. También aprenderá a estructurar la aplicación para mejorar el rendimiento al minimizar la creación de recursos.

Para seguir el tutorial, puede usar Microsoft Visual Studio 2008 para crear un proyecto de Win32 y, a continuación, reemplazar el código del encabezado de la aplicación principal y del archivo CPP por el código descrito en este tutorial.

> [!Note]  
> Si quiere crear una aplicación de la tienda Windows que use Direct2D, vea el tema [de inicio rápido de direct2d para Windows 8](direct2d-quickstart-with-device-context.md) .

 

Para obtener información general sobre las interfaces que puede usar para crear contenido de Direct2D, consulte [información general](the-direct2d-api.md)de la API de direct2d.

Este tutorial contiene las siguientes partes:

-   [Parte 1: creación del encabezado DemoApp](#part-1-create-the-demoapp-header)
-   [Parte 2: implementación de la infraestructura de clase](#part-2-implement-the-class-infrastructure)
-   [Parte 3: creación de recursos de Direct2D](#part-3-create-direct2d-resources)
-   [Parte 4: representación de contenido de Direct2D](#part-4-render-direct2d-content)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

Al finalizar, la clase DemoApp genera el resultado que se muestra en la siguiente ilustración.

![Ilustración de dos rectángulos en un fondo de cuadrícula](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>Parte 1: creación del encabezado DemoApp

En este paso, se configura la aplicación para usar Direct2D agregando los encabezados y macros necesarios. También se declaran los métodos y miembros de datos que se van a usar en partes posteriores de este tutorial.

1.  En el archivo de encabezado de la aplicación, incluya los siguientes encabezados usados con frecuencia.
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  Declare funciones adicionales para liberar interfaces y macros para el control de errores y la recuperación de la dirección base del módulo.
```C++
    template<class Interface>
    inline void SafeRelease(
        Interface **ppInterfaceToRelease
        )
    {
        if (*ppInterfaceToRelease != NULL)
        {
            (*ppInterfaceToRelease)->Release();

            (*ppInterfaceToRelease) = NULL;
        }
    }


    #ifndef Assert
    #if defined( DEBUG ) || defined( _DEBUG )
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  Declare los métodos para inicializar la clase, crear y descartar recursos, controlar el bucle de mensajes, representar el contenido y el procedimiento de Windows.
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  Declare punteros para un objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , un objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) y dos objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) como miembros de clase.
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>Parte 2: implementación de la infraestructura de clase

En esta parte, se implementa el constructor y el destructor de DemoApp, sus métodos de inicialización y bucle de mensajes, y la función WinMain. La mayoría de estos métodos tienen el mismo aspecto que los que se encuentran en cualquier otra aplicación de Win32. La única excepción es el método Initialize, que llama al método CreateDeviceIndependentResources (que se define en la siguiente parte) que crea varios recursos de Direct2D.

1.  En el archivo de implementación de clase, implemente el constructor y el destructor de clase. El constructor debe inicializar sus miembros en **null**. El destructor debe liberar todas las interfaces almacenadas como miembros de clase.
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  Implemente el método DemoApp:: RunMessageLoop que traduce y envía mensajes.
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  Implemente el método Initialize que crea la ventana, la muestra y llama al método DemoApp:: CreateDeviceIndependentResources. Implemente el método CreateDeviceIndependentResources en la sección siguiente.
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
                WS_OVERLAPPEDWINDOW,
                CW_USEDEFAULT,
                CW_USEDEFAULT,
                static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
                static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
                NULL,
                NULL,
                HINST_THISCOMPONENT,
                this
                );
            hr = m_hwnd ? S_OK : E_FAIL;
            if (SUCCEEDED(hr))
            {
                ShowWindow(m_hwnd, SW_SHOWNORMAL);
                UpdateWindow(m_hwnd);
            }
        }

        return hr;
    }
```

    

4.  Cree el método WinMain que actúa como punto de entrada de la aplicación. Inicialice una instancia de la clase DemoApp y comience su bucle de mensajes.
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
        // unlikely event that HeapSetInformation fails.
        HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

        if (SUCCEEDED(CoInitialize(NULL)))
        {
            {
                DemoApp app;

                if (SUCCEEDED(app.Initialize()))
                {
                    app.RunMessageLoop();
                }
            }
            CoUninitialize();
        }

        return 0;
    }
```

    

## <a name="part-3-create-direct2d-resources"></a>Parte 3: creación de recursos de Direct2D

En esta parte, se crean los recursos de Direct2D que se usan para dibujar. Direct2D proporciona dos tipos de recursos: recursos independientes del dispositivo que pueden durar la duración de la aplicación y recursos dependientes del dispositivo. Los recursos dependientes del dispositivo se asocian a un dispositivo de representación determinado y dejarán de funcionar si se quita ese dispositivo.

1.  Implemente el método DemoApp:: CreateDeviceIndependentResources. En el método, cree un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), un recurso independiente del dispositivo, para crear otros recursos de Direct2D. Use el miembro de clase **m \_ pDirect2DdFactory** para almacenar el generador.
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  Implemente el método DemoApp:: CreateDeviceResources. Este método crea los recursos dependientes del dispositivo de la ventana, un destino de representación y dos pinceles. Recupere el tamaño del área cliente y cree un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) del mismo tamaño que se representa en el **hWnd** de la ventana. Almacene el destino de representación en el miembro de clase **m \_ pRenderTarget** .
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  Use el destino de presentación para crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) gris y un **ID2D1SolidColorBrush** azul azul aciano.
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  Dado que se llamará a este método repetidamente, agregue una instrucción if para comprobar si el destino de representación (**m \_ pRenderTarget** ) ya existe. En el código siguiente se muestra el método CreateDeviceResources completo.
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  Implemente el método DemoApp::D iscardDeviceResources. En este método, libere el destino de representación y los dos pinceles que creó en el método DemoApp:: CreateDeviceResources.
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>Parte 4: representación de contenido de Direct2D

En esta parte, se implementa el procedimiento de Windows, el método OnRender que pinta el contenido y el método OnResize que ajusta el tamaño del destino de representación cuando se cambia el tamaño de la ventana.

1.  Implemente el método DemoApp:: WndProc para controlar los mensajes de ventana. Para el mensaje de [**\_ tamaño de WM**](../winmsg/wm-size.md) , llame al método demoApp:: OnResize y páselo al nuevo ancho y alto. En el caso de los mensajes de [**WM \_**](/windows/desktop/gdi/wm-paint) y [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , llame al método demoApp:: OnRender para pintar la ventana. Los métodos OnRender y OnResize se implementan en los pasos siguientes.
```C++
    LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
    {
        LRESULT result = 0;

        if (message == WM_CREATE)
        {
            LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
            DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

            ::SetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA,
                reinterpret_cast<LONG_PTR>(pDemoApp)
                );

            result = 1;
        }
        else
        {
            DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
                ::GetWindowLongPtrW(
                    hwnd,
                    GWLP_USERDATA
                    )));

            bool wasHandled = false;

            if (pDemoApp)
            {
                switch (message)
                {
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
                    break;
                }
            }

            if (!wasHandled)
            {
                result = DefWindowProc(hwnd, message, wParam, lParam);
            }
        }

        return result;
    }
    
```

    

2.  Implemente el método DemoApp:: OnRender. En primer lugar, cree un **valor HRESULT**. A continuación, llame al método CreateDeviceResource. Se llama a este método cada vez que se pinta la ventana. Recuerde que, en el paso 4 de la parte 3, ha agregado una instrucción **If** para evitar que el método realice cualquier trabajo si el destino de representación ya existe.
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  Compruebe que el método CreateDeviceResource se ha realizado correctamente. En caso contrario, no realice ningún dibujo.
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  Dentro de la instrucción **If** que acaba de crear, inicie el dibujo llamando al método BeginDraw del destino de representación. Establezca la transformación del destino de representación en la matriz de identidades y borre la ventana.
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  Recupera el tamaño del área de dibujo.
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  Dibuje un fondo de cuadrícula mediante un bucle **for** y el método [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) del destino de representación para dibujar una serie de líneas.
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  Cree dos primitivas de rectángulo que están centradas en la pantalla.
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  Use el método [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) del destino de representación para pintar el interior del primer rectángulo con el pincel gris.
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  Use el método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) del destino de representación para pintar el contorno del segundo rectángulo con el pincel azul azul aciano.
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. Llame al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) del destino de representación. El método **EndDraw** devuelve un **valor HRESULT** para indicar si las operaciones de dibujo se realizaron correctamente. Cierre la instrucción **If** que inició en el paso 3.
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. Compruebe el **HRESULT** devuelto por [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Si indica que el destino de representación debe volver a crearse, llame al método DemoApp::D iscardDeviceResources para liberarlo; se volverá a crear la próxima vez que la ventana reciba un mensaje [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) o [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. Devuelva el **valor HRESULT** y cierre el método.
```C++
        return hr;
    }
```

    

13. Implemente el método DemoApp:: OnResize para que cambie el tamaño del destino de representación al nuevo tamaño de la ventana.
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

Ha completado el tutorial.

> [!Note]  
> Para usar Direct2D, asegúrese de que la aplicación incluye el archivo de encabezado d2d1. h y se compila con la biblioteca d2d1. lib. Puede encontrar d2d1. h y d2d1. lib en el [Kit de desarrollo de software (SDK) de Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

 

## <a name="summary"></a>Resumen

En este tutorial, aprendió a crear recursos de Direct2D y dibujar formas básicas. También aprendió a estructurar la aplicación para mejorar el rendimiento al minimizar la creación de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la API de Direct2D](the-direct2d-api.md)
</dt> <dt>

[Mejorar el rendimiento de Direct2D](improving-direct2d-performance.md)
</dt> </dl>

 

 