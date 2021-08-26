---
title: Trabajar con recursos de dispositivo DirectX
description: Comprenda el rol de Microsoft Infraestructura de gráficos de DirectX (DXGI) en el juego Windows Store DirectX.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068665"
---
# <a name="work-with-directx-device-resources"></a>Trabajar con recursos de dispositivo DirectX

Comprenda el rol de Microsoft Infraestructura de gráficos de DirectX (DXGI) en el juego Windows Store DirectX. DXGI es un conjunto de API que se usan para configurar y administrar recursos de adaptador de gráficos y gráficos de bajo nivel. Sin él, no tendría ninguna manera de dibujar los gráficos del juego en una ventana.

Piense en DXGI de esta manera: para acceder directamente a la GPU y administrar sus recursos, debe tener una manera de describirla en la aplicación. La información más importante que necesita sobre la GPU es el lugar donde dibujar píxeles para que pueda enviar esos píxeles a la pantalla. Normalmente, esto se denomina "búfer de reserva", una ubicación en la memoria de GPU en la que puede dibujar los píxeles y, a continuación, hacer que se "voltear" o "intercambiar" y enviar a la pantalla en una señal de actualización. DXGI le permite adquirir esa ubicación y los  medios para usar ese búfer (denominado cadena de intercambio porque es una cadena de búferes intercambiables, lo que permite varias estrategias de almacenamiento en búfer).

Para ello, necesita acceso para escribir en la cadena de intercambio y un identificador en la ventana que mostrará el búfer de reserva actual para la cadena de intercambio. También debe conectar los dos para asegurarse de que el sistema operativo actualizará la ventana con el contenido del búfer de reserva cuando solicite que lo haga.

El proceso general para dibujar en la pantalla es el siguiente:

-   Obtenga un [**elemento CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para la aplicación.
-   Obtenga una interfaz para el dispositivo y el contexto de Direct3D.
-   Cree la cadena de intercambio para mostrar la imagen representado en [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).
-   Cree un destino de representación para dibujar y rellene con píxeles.
-   Presente la cadena de intercambio.

## <a name="create-a-window-for-your-app"></a>Creación de una ventana para la aplicación

Lo primero que debemos hacer es crear una ventana. En primer lugar, cree una clase de ventana mediante la rellenar una instancia de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)y, a continuación, regístrela [**mediante RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). La clase window contiene propiedades esenciales de la ventana, incluido el icono que usa, la función de procesamiento de mensajes estáticos (más adelante) y un nombre único para la clase de ventana.


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



A continuación, cree la ventana. También es necesario proporcionar información de tamaño para la ventana y el nombre de la clase de ventana que acaba de crear. Cuando se llama [**a CreateWindow,**](/windows/desktop/api/winuser/nf-winuser-createwindowa)se obtiene un puntero opaco a la ventana denominado HWND; Tendrá que mantener el puntero HWND y usarlo en cualquier momento que necesite hacer referencia a la ventana, incluido destruirlo o volver a crearlo, y (especialmente importante) al crear la cadena de intercambio DXGI que use para dibujar en la ventana.


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



El Windows de aplicación de escritorio incluye un enlace al Windows de mensajes. Deberá basar el bucle de programa principal fuera de este enlace escribiendo una función "StaticWindowProc" para procesar eventos de ventana. Debe ser una función estática porque Windows llamará fuera del contexto de cualquier instancia de clase. Este es un ejemplo muy sencillo de una función de procesamiento de mensajes estáticos.


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



En este ejemplo simple solo se comprueban las condiciones de salida del programa: [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close), que se envía cuando se solicita que se cierre la ventana, y [**WM \_ DESTROY,**](/windows/desktop/winmsg/wm-destroy)que se envía después de que la ventana se quite realmente de la pantalla. Una aplicación completa de producción también debe controlar otros eventos de ventana: para obtener la lista completa de eventos de ventana, vea [Notificaciones de ventana.](/windows/desktop/winmsg/window-notifications)

El propio bucle de programa principal debe confirmar Windows mensajes al permitir Windows la oportunidad de ejecutar el procedimiento de mensaje estático. Ayude a que el programa se ejecute de forma eficaz mediante la forzamiento del comportamiento: cada iteración debe elegir procesar nuevos mensajes Windows si están disponibles y, si no hay ningún mensaje en la cola, debe representar un nuevo marco. Este es un ejemplo muy sencillo:


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Obtener una interfaz para el dispositivo y el contexto de Direct3D

El primer paso para usar Direct3D es adquirir una interfaz para el hardware de Direct3D (la GPU), representada como instancias de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) La primera es una representación virtual de los recursos de GPU y la segunda es una abstracción independiente del dispositivo de la canalización y el proceso de representación. Esta es una manera fácil de pensar en ello: **ID3D11Device** contiene los métodos gráficos a los que llama con poca frecuencia, normalmente antes de que se produzca cualquier representación, para adquirir y configurar el conjunto de recursos que necesita para empezar a dibujar píxeles. POR otro lado, **ID3D11DeviceContext** contiene los métodos a los que se llama a cada fotograma: cargar en búferes y vistas y otros recursos, cambiar el estado de fusión de salida y rasterizador, administrar sombreadores y dibujar los resultados de pasar esos recursos a través de los estados y sombreadores.

Hay una parte muy importante de este proceso: establecer el nivel de característica. El nivel de característica indica a DirectX el nivel mínimo de hardware que admite la aplicación, con D3D FEATURE LEVEL 9 1 como el conjunto de características más bajo y \_ \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ \_ 11 1 como el máximo actual. Debe admitir 9 1 como mínimo si desea llegar a \_ la audiencia más amplia posible. Dedícate un tiempo a [](/previous-versions/windows/apps/hh994923(v=win.10)) leer los niveles de características de Direct3D y a evaluar por ti mismo los niveles mínimo y máximo de características que quieres que tu juego admita y para comprender las implicaciones de tu elección.

Obtenga referencias (punteros) al contexto de dispositivo y dispositivo de Direct3D y almacénelas como variables de nivel de clase en la instancia **DeviceResources** (como punteros inteligentes **ComPtr).** Use estas referencias siempre que necesite acceder al contexto de dispositivo o dispositivo de Direct3D.


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a>Creación de la cadena de intercambio

Correcto: tiene una ventana en la que dibujar y tiene una interfaz para enviar datos y proporcionar comandos a la GPU. Ahora veamos cómo reunirlos.

En primer lugar, debe decir a DXGI qué valores usar para las propiedades de la cadena de intercambio. Para ello, use [**una estructura \_ \_ \_ DESC DESC DE DXGI SWAP CHAIN.**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) Seis campos son especialmente importantes para las aplicaciones de escritorio:

-   **Ventana:** indica si la cadena de intercambio es de pantalla completa o se recorta a la ventana. Establezca esta opción en TRUE para colocar la cadena de intercambio en la ventana que creó anteriormente.
-   **BufferUsage:** esta opción se establece en DXGI \_ USAGE RENDER TARGET \_ \_ \_ OUTPUT. Esto indica que la cadena de intercambio será una superficie de dibujo, lo que le permite usarla como destino de representación de Direct3D.
-   **SwapEffect:** esta opción se establece en DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL.
-   **Formato:** el formato DXGI \_ FORMAT \_ B8G8R8A8 UNORM especifica un color de 32 bits: 8 bits para cada uno de los tres canales de color RGB y 8 bits para el \_ canal alfa.
-   **BufferCount:** esta opción se establece en 2 para un comportamiento tradicional de doble búfer para evitar la lágrima. Establezca el recuento de búferes en 3 si el contenido gráfico tarda más de un ciclo de actualización del monitor para representar un único fotograma (por ejemplo, a 60 Hz, el umbral es superior a 16 ms).
-   **SampleDesc:** este campo controla la multimuestreo. Establezca **Recuento en** 1 y **Calidad** en 0 para cadenas de intercambio de modelos de volteo. (Para usar multimuestreo con cadenas de intercambio de modelos de volteo, dibuje en un destino de representación multimuestreo independiente y, a continuación, resuelva ese destino en la cadena de intercambio justo antes de presentarlo. El código de ejemplo se proporciona [en Multisampling en Windows Store).](/previous-versions/windows/apps/dn458384(v=win.10))

Después de especificar una configuración para la cadena de intercambio, debe usar el mismo generador de DXGI que creó el dispositivo Direct3D (y el contexto del dispositivo) para crear la cadena de intercambio.

**Forma corta: **

Obtenga la [**referencia ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que creó anteriormente. Consóndalo a [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (si aún no lo ha hecho) y, a continuación, llame a [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) para adquirir el adaptador de DXGI. Obtenga el generador primario para ese adaptador mediante una llamada a [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) hereda de [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)), ahora puede usar ese generador para crear la cadena de intercambio mediante una llamada a [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), como se muestra en el ejemplo de código siguiente.


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



Si acaba de empezar, probablemente sea mejor usar la configuración que se muestra aquí. Ahora, si ya está familiarizado con las versiones anteriores de DirectX, podría preguntar: "¿Por qué no creamos el dispositivo y la cadena de intercambio al mismo tiempo, en lugar de volver a través de todas esas clases?". La respuesta es la eficacia: las cadenas de intercambio son recursos de dispositivo Direct3D y los recursos de dispositivo están asociados al dispositivo Direct3D concreto que los creó. Si crea un dispositivo con una nueva cadena de intercambio, tendrá que volver a crear todos los recursos del dispositivo mediante el nuevo dispositivo Direct3D. Por lo tanto, al crear la cadena de intercambio con la misma fábrica (como se muestra anteriormente), puede volver a crear la cadena de intercambio y seguir usando los recursos de dispositivo Direct3D que ya ha cargado.

Ahora tiene una ventana del sistema operativo, una manera de acceder a la GPU y sus recursos y una cadena de intercambio para mostrar los resultados de la representación. Lo único que queda es conectar todo el proceso.

## <a name="create-a-render-target-for-drawing"></a>Creación de un destino de representación para dibujar

La canalización del sombreador necesita un recurso en el que dibujar píxeles. La manera más sencilla de crear este recurso es definir un recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) como búfer de reserva en el que dibujar el sombreador de píxeles y, a continuación, leer esa textura en la cadena de intercambio.

Para ello, cree una vista render-target . En Direct3D, una vista es una manera de acceder a un recurso específico. En este caso, la vista permite que el sombreador de píxeles escriba en la textura a medida que completa sus operaciones por píxel.

Echemos un vistazo al código para esto. Al establecer DXGI USAGE RENDER TARGET OUTPUT en la cadena de intercambio, esto permitió que el recurso \_ \_ de \_ Direct3D subyacente se usara \_ como superficie de dibujo. Por lo tanto, para obtener la vista de destino de representación, basta con obtener el búfer de reserva de la cadena de intercambio y crear una vista de destino de representación enlazada al recurso de búfer de reserva.


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



Cree también un *búfer de galería de símbolos de profundidad*. Un búfer de galería de símbolos de profundidad es simplemente una forma determinada de recurso [**ID3D11Texture2D,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) que normalmente se usa para determinar qué píxeles tienen prioridad de dibujo durante la rasterización en función de la distancia de los objetos de la escena desde la cámara. También se puede usar un búfer de galería de símbolos de profundidad para efectos de galería de símbolos, donde se descartan u omiten píxeles específicos durante la rasterización. Este búfer debe tener el mismo tamaño que el destino de representación. Tenga en cuenta que no se puede leer ni representar en la textura de galería de símbolos de profundidad del búfer de marco porque la canalización del sombreador la usa exclusivamente antes y durante la rasterización final.

Cree también una vista para el búfer de galería de símbolos de profundidad como [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). La vista indica a la canalización del sombreador cómo interpretar el recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) subyacente, por lo que si no proporciona esta vista, no se realiza ninguna prueba de profundidad por píxel y los objetos de la escena pueden parecer un poco dentro de la escena como mínimo.


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



El último paso es crear una ventanilla. Esto define el rectángulo visible del búfer de reserva que se muestra en la pantalla; Puede cambiar la parte del búfer que se muestra en la pantalla cambiando los parámetros de la ventanilla. Este código tiene como destino todo el tamaño de la ventana o la resolución de pantalla, en el caso de cadenas de intercambio de pantalla completa. Para que sea divertido, cambie los valores de coordenadas proporcionados y observe los resultados.


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



Y así es como se pasa de nada a dibujar píxeles en una ventana. Al empezar, es una buena idea familiarizarse con cómo DirectX, a través de DXGI, administra los recursos principales que necesita para empezar a dibujar píxeles.

A continuación, veremos la estructura de la canalización de gráficos. consulte [Información sobre la canalización de representación de la plantilla de aplicación de DirectX.](understand-the-directx-11-2-graphics-pipeline.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Siguiente**
</dt> <dt>

[Trabajar con sombreadores y recursos de sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 