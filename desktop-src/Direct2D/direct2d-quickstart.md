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
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="49389-108">Crear una aplicación de Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="49389-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="49389-109">Este tema le guía por el proceso de creación de la clase DemoApp, que crea una ventana y utiliza Direct2D para dibujar una cuadrícula y dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="49389-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="49389-110">En este tutorial, aprenderá a crear recursos de Direct2D y a dibujar formas básicas.</span><span class="sxs-lookup"><span data-stu-id="49389-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="49389-111">También aprenderá a estructurar la aplicación para mejorar el rendimiento al minimizar la creación de recursos.</span><span class="sxs-lookup"><span data-stu-id="49389-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="49389-112">Para seguir el tutorial, puede usar Microsoft Visual Studio 2008 para crear un proyecto de Win32 y, a continuación, reemplazar el código del encabezado de la aplicación principal y del archivo CPP por el código descrito en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="49389-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="49389-113">Si quiere crear una aplicación de la tienda Windows que use Direct2D, vea el tema [de inicio rápido de direct2d para Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="49389-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="49389-114">Para obtener información general sobre las interfaces que puede usar para crear contenido de Direct2D, consulte [información general](the-direct2d-api.md)de la API de direct2d.</span><span class="sxs-lookup"><span data-stu-id="49389-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="49389-115">Este tutorial contiene las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="49389-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="49389-116">Parte 1: creación del encabezado DemoApp</span><span class="sxs-lookup"><span data-stu-id="49389-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="49389-117">Parte 2: implementación de la infraestructura de clase</span><span class="sxs-lookup"><span data-stu-id="49389-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="49389-118">Parte 3: creación de recursos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="49389-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="49389-119">Parte 4: representación de contenido de Direct2D</span><span class="sxs-lookup"><span data-stu-id="49389-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="49389-120">Resumen</span><span class="sxs-lookup"><span data-stu-id="49389-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="49389-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49389-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="49389-122">Al finalizar, la clase DemoApp genera el resultado que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="49389-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![Ilustración de dos rectángulos en un fondo de cuadrícula](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="49389-124">Parte 1: creación del encabezado DemoApp</span><span class="sxs-lookup"><span data-stu-id="49389-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="49389-125">En este paso, se configura la aplicación para usar Direct2D agregando los encabezados y macros necesarios.</span><span class="sxs-lookup"><span data-stu-id="49389-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="49389-126">También se declaran los métodos y miembros de datos que se van a usar en partes posteriores de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="49389-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="49389-127">En el archivo de encabezado de la aplicación, incluya los siguientes encabezados usados con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="49389-127">In your application header file, include the following frequently used headers.</span></span>
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

    

2.  <span data-ttu-id="49389-128">Declare funciones adicionales para liberar interfaces y macros para el control de errores y la recuperación de la dirección base del módulo.</span><span class="sxs-lookup"><span data-stu-id="49389-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
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

    

3.  <span data-ttu-id="49389-129">Declare los métodos para inicializar la clase, crear y descartar recursos, controlar el bucle de mensajes, representar el contenido y el procedimiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="49389-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
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



    

4.  <span data-ttu-id="49389-130">Declare punteros para un objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , un objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) y dos objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) como miembros de clase.</span><span class="sxs-lookup"><span data-stu-id="49389-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="49389-131">Parte 2: implementación de la infraestructura de clase</span><span class="sxs-lookup"><span data-stu-id="49389-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="49389-132">En esta parte, se implementa el constructor y el destructor de DemoApp, sus métodos de inicialización y bucle de mensajes, y la función WinMain.</span><span class="sxs-lookup"><span data-stu-id="49389-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="49389-133">La mayoría de estos métodos tienen el mismo aspecto que los que se encuentran en cualquier otra aplicación de Win32.</span><span class="sxs-lookup"><span data-stu-id="49389-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="49389-134">La única excepción es el método Initialize, que llama al método CreateDeviceIndependentResources (que se define en la siguiente parte) que crea varios recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="49389-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="49389-135">En el archivo de implementación de clase, implemente el constructor y el destructor de clase.</span><span class="sxs-lookup"><span data-stu-id="49389-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="49389-136">El constructor debe inicializar sus miembros en **null**.</span><span class="sxs-lookup"><span data-stu-id="49389-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="49389-137">El destructor debe liberar todas las interfaces almacenadas como miembros de clase.</span><span class="sxs-lookup"><span data-stu-id="49389-137">The destructor should release any interfaces stored as class members.</span></span>
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



    

2.  <span data-ttu-id="49389-138">Implemente el método DemoApp:: RunMessageLoop que traduce y envía mensajes.</span><span class="sxs-lookup"><span data-stu-id="49389-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
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

    

3.  <span data-ttu-id="49389-139">Implemente el método Initialize que crea la ventana, la muestra y llama al método DemoApp:: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="49389-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="49389-140">Implemente el método CreateDeviceIndependentResources en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="49389-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
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

    

4.  <span data-ttu-id="49389-141">Cree el método WinMain que actúa como punto de entrada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49389-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="49389-142">Inicialice una instancia de la clase DemoApp y comience su bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="49389-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
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

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="49389-143">Parte 3: creación de recursos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="49389-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="49389-144">En esta parte, se crean los recursos de Direct2D que se usan para dibujar.</span><span class="sxs-lookup"><span data-stu-id="49389-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="49389-145">Direct2D proporciona dos tipos de recursos: recursos independientes del dispositivo que pueden durar la duración de la aplicación y recursos dependientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49389-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="49389-146">Los recursos dependientes del dispositivo se asocian a un dispositivo de representación determinado y dejarán de funcionar si se quita ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49389-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="49389-147">Implemente el método DemoApp:: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="49389-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="49389-148">En el método, cree un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), un recurso independiente del dispositivo, para crear otros recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="49389-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="49389-149">Use el miembro de clase **m \_ pDirect2DdFactory** para almacenar el generador.</span><span class="sxs-lookup"><span data-stu-id="49389-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="49389-150">Implemente el método DemoApp:: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="49389-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="49389-151">Este método crea los recursos dependientes del dispositivo de la ventana, un destino de representación y dos pinceles.</span><span class="sxs-lookup"><span data-stu-id="49389-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="49389-152">Recupere el tamaño del área cliente y cree un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) del mismo tamaño que se representa en el **hWnd** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="49389-153">Almacene el destino de representación en el miembro de clase **m \_ pRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="49389-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
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

    

3.  <span data-ttu-id="49389-154">Use el destino de presentación para crear un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) gris y un **ID2D1SolidColorBrush** azul azul aciano.</span><span class="sxs-lookup"><span data-stu-id="49389-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
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

    

4.  <span data-ttu-id="49389-155">Dado que se llamará a este método repetidamente, agregue una instrucción if para comprobar si el destino de representación (**m \_ pRenderTarget** ) ya existe.</span><span class="sxs-lookup"><span data-stu-id="49389-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="49389-156">En el código siguiente se muestra el método CreateDeviceResources completo.</span><span class="sxs-lookup"><span data-stu-id="49389-156">The following code shows the complete CreateDeviceResources method.</span></span>
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

    

5.  <span data-ttu-id="49389-157">Implemente el método DemoApp::D iscardDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="49389-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="49389-158">En este método, libere el destino de representación y los dos pinceles que creó en el método DemoApp:: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="49389-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="49389-159">Parte 4: representación de contenido de Direct2D</span><span class="sxs-lookup"><span data-stu-id="49389-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="49389-160">En esta parte, se implementa el procedimiento de Windows, el método OnRender que pinta el contenido y el método OnResize que ajusta el tamaño del destino de representación cuando se cambia el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="49389-161">Implemente el método DemoApp:: WndProc para controlar los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="49389-162">Para el mensaje de [**\_ tamaño de WM**](../winmsg/wm-size.md) , llame al método demoApp:: OnResize y páselo al nuevo ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="49389-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="49389-163">En el caso de los mensajes de [**WM \_**](/windows/desktop/gdi/wm-paint) y [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , llame al método demoApp:: OnRender para pintar la ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="49389-164">Los métodos OnRender y OnResize se implementan en los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="49389-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
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

    

2.  <span data-ttu-id="49389-165">Implemente el método DemoApp:: OnRender.</span><span class="sxs-lookup"><span data-stu-id="49389-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="49389-166">En primer lugar, cree un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="49389-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="49389-167">A continuación, llame al método CreateDeviceResource.</span><span class="sxs-lookup"><span data-stu-id="49389-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="49389-168">Se llama a este método cada vez que se pinta la ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="49389-169">Recuerde que, en el paso 4 de la parte 3, ha agregado una instrucción **If** para evitar que el método realice cualquier trabajo si el destino de representación ya existe.</span><span class="sxs-lookup"><span data-stu-id="49389-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="49389-170">Compruebe que el método CreateDeviceResource se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="49389-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="49389-171">En caso contrario, no realice ningún dibujo.</span><span class="sxs-lookup"><span data-stu-id="49389-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="49389-172">Dentro de la instrucción **If** que acaba de crear, inicie el dibujo llamando al método BeginDraw del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="49389-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="49389-173">Establezca la transformación del destino de representación en la matriz de identidades y borre la ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="49389-174">Recupera el tamaño del área de dibujo.</span><span class="sxs-lookup"><span data-stu-id="49389-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="49389-175">Dibuje un fondo de cuadrícula mediante un bucle **for** y el método [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) del destino de representación para dibujar una serie de líneas.</span><span class="sxs-lookup"><span data-stu-id="49389-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
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

    

7.  <span data-ttu-id="49389-176">Cree dos primitivas de rectángulo que están centradas en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="49389-176">Create two rectangle primitives that are centered on the screen.</span></span>
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

    

8.  <span data-ttu-id="49389-177">Use el método [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) del destino de representación para pintar el interior del primer rectángulo con el pincel gris.</span><span class="sxs-lookup"><span data-stu-id="49389-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="49389-178">Use el método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) del destino de representación para pintar el contorno del segundo rectángulo con el pincel azul azul aciano.</span><span class="sxs-lookup"><span data-stu-id="49389-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="49389-179">Llame al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="49389-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="49389-180">El método **EndDraw** devuelve un **valor HRESULT** para indicar si las operaciones de dibujo se realizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="49389-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="49389-181">Cierre la instrucción **If** que inició en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="49389-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="49389-182">Compruebe el **HRESULT** devuelto por [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="49389-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="49389-183">Si indica que el destino de representación debe volver a crearse, llame al método DemoApp::D iscardDeviceResources para liberarlo; se volverá a crear la próxima vez que la ventana reciba un mensaje [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) o [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="49389-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="49389-184">Devuelva el **valor HRESULT** y cierre el método.</span><span class="sxs-lookup"><span data-stu-id="49389-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="49389-185">Implemente el método DemoApp:: OnResize para que cambie el tamaño del destino de representación al nuevo tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="49389-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
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

    

<span data-ttu-id="49389-186">Ha completado el tutorial.</span><span class="sxs-lookup"><span data-stu-id="49389-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="49389-187">Para usar Direct2D, asegúrese de que la aplicación incluye el archivo de encabezado d2d1. h y se compila con la biblioteca d2d1. lib.</span><span class="sxs-lookup"><span data-stu-id="49389-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="49389-188">Puede encontrar d2d1. h y d2d1. lib en el [Kit de desarrollo de software (SDK) de Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49389-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="49389-189">Resumen</span><span class="sxs-lookup"><span data-stu-id="49389-189">Summary</span></span>

<span data-ttu-id="49389-190">En este tutorial, aprendió a crear recursos de Direct2D y dibujar formas básicas.</span><span class="sxs-lookup"><span data-stu-id="49389-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="49389-191">También aprendió a estructurar la aplicación para mejorar el rendimiento al minimizar la creación de recursos.</span><span class="sxs-lookup"><span data-stu-id="49389-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49389-192">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49389-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49389-193">Introducción a la API de Direct2D</span><span class="sxs-lookup"><span data-stu-id="49389-193">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> <dt>

[<span data-ttu-id="49389-194">Mejorar el rendimiento de Direct2D</span><span class="sxs-lookup"><span data-stu-id="49389-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 