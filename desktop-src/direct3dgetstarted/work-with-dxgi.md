---
title: Trabajar con recursos de dispositivos DirectX
description: Comprenda el rol de la infraestructura de gráficos de Microsoft DirectX (DXGI) en el juego DirectX de la tienda Windows.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096e2be6f957d99bc6e5055f845c14448ecd647f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487931"
---
# <a name="work-with-directx-device-resources"></a>Trabajar con recursos de dispositivos DirectX

Comprenda el rol de la infraestructura de gráficos de Microsoft DirectX (DXGI) en el juego DirectX de la tienda Windows. DXGI es un conjunto de API que se usan para configurar y administrar los gráficos de bajo nivel y los recursos del adaptador de gráficos. Sin él, no tendría ninguna manera de dibujar los gráficos del juego en una ventana.

Piense en DXGI de esta manera: para acceder directamente a la GPU y administrar sus recursos, debe tener una manera de describirla en la aplicación. La parte más importante de la información que necesita sobre la GPU es el lugar para dibujar píxeles de modo que pueda enviar esos píxeles a la pantalla. Normalmente, esto se denomina "búfer de reserva", una ubicación en la memoria de GPU en la que puede dibujar los píxeles y, a continuación, hacer que se "volteo" o "intercambie" y se envíen a la pantalla en una señal de actualización. DXGI le permite adquirir esa ubicación y los medios para usar ese búfer (denominado *cadena de intercambio* porque es una cadena de búferes intercambiables, lo que permite varias estrategias de almacenamiento en búfer).

Para ello, necesita acceso para escribir en la cadena de intercambio y un identificador de la ventana que mostrará el búfer de reserva actual de la cadena de intercambio. También debe conectar los dos para asegurarse de que el sistema operativo actualizará la ventana con el contenido del búfer de reserva cuando se lo solicite.

El proceso general para dibujar en la pantalla es el siguiente:

-   Obtiene un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para tu aplicación.
-   Obtiene una interfaz para el dispositivo Direct3D y el contexto.
-   Cree la cadena de intercambio para mostrar la imagen representada en [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).
-   Cree un destino de representación para dibujar y rellenarlo con píxeles.
-   Presente la cadena de intercambio.

## <a name="create-a-window-for-your-app"></a>Crear una ventana para la aplicación

Lo primero que debemos hacer es crear una ventana. En primer lugar, cree una clase de ventana rellenando una instancia de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)y regístrela mediante [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). La clase de ventana contiene propiedades esenciales de la ventana, incluido el icono que usa, la función de procesamiento de mensajes estático (más información más adelante) y un nombre único para la clase de ventana.


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



A continuación, cree la ventana. También es necesario proporcionar información de tamaño para la ventana y el nombre de la clase de ventana que acabamos de crear. Cuando se llama a [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), se obtiene un puntero opaco a la ventana denominada HWND; deberá mantener el puntero HWND y usarlo en cualquier momento que necesite hacer referencia a la ventana, incluida la destrucción o la recreación, y (especialmente importante) al crear la cadena de intercambio de DXGI que usa para dibujar en la ventana.


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



El modelo de aplicación de escritorio de Windows incluye un enlace en el bucle de mensajes de Windows. Deberá basar el bucle principal del programa de este enlace escribiendo una función "StaticWindowProc" para procesar los eventos de ventana. Debe ser una función estática, ya que Windows la llamará fuera del contexto de cualquier instancia de clase. Este es un ejemplo muy sencillo de una función de procesamiento de mensajes estáticos.


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



En este sencillo ejemplo solo se comprueban las condiciones de salida del programa: el [**\_ cierre de WM**](/windows/desktop/winmsg/wm-close), el que se envía cuando se solicita el cierre de la ventana y la [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy), que se envía después de que la ventana se quite realmente de la pantalla. Una aplicación completa de producción debe controlar también otros eventos de ventana. para obtener la lista completa de eventos de ventana, vea [notificaciones de ventana](/windows/desktop/winmsg/window-notifications).

El propio bucle del programa principal debe confirmar los mensajes de Windows permitiendo a Windows la oportunidad de ejecutar el procedimiento de mensaje estático. Ayude a que el programa se ejecute de forma eficaz ramificando el comportamiento: cada iteración debe elegir procesar nuevos mensajes de Windows si están disponibles y, si no hay ningún mensaje en la cola, debe representar un nuevo marco. Este es un ejemplo muy sencillo:


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

El primer paso para usar Direct3D es adquirir una interfaz para el hardware de Direct3D (GPU), representada como instancias de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) y [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2). El primero es una representación virtual de los recursos de GPU y el último es una abstracción independiente del dispositivo de la canalización de representación y el proceso. Esta es una manera fácil de pensar en ello: **ID3D11Device** contiene los métodos gráficos a los que llama con poca frecuencia, normalmente antes de que se produzca cualquier representación, para adquirir y configurar el conjunto de recursos que necesita para empezar a dibujar píxeles. Por otro lado, **ID3D11DeviceContext** contiene los métodos a los que se llama cada fotograma: carga en búferes y vistas y otros recursos, cambiando la fusión de salida y el estado del rasterizador, administrando los sombreadores y dibujando los resultados de pasar esos recursos a través de los Estados y los sombreadores.

Hay una parte muy importante de este proceso: establecer el nivel de características. El nivel de característica indica a DirectX el nivel mínimo de hardware que admite la aplicación, con \_ \_ el nivel de característica de D3D \_ 9 \_ 1 como el conjunto de características más bajo y el nivel de característica de D3D \_ \_ \_ 11 \_ 1 como el valor más alto actual. Debe admitir 9 \_ 1 como mínimo si desea llegar al público más amplio posible. Tómese un tiempo para leer los niveles de [características](/previous-versions/windows/apps/hh994923(v=win.10)) de Direct3D y evalúe los niveles de características mínimo y máximo que desee que admita el juego y comprenda las implicaciones de su elección.

Obtener referencias (punteros) en el dispositivo Direct3D y en el contexto del dispositivo y almacenarlas como variables de nivel de clase en la instancia de **DeviceResources** (como punteros inteligentes **ComPtr** ). Use estas referencias siempre que necesite tener acceso al dispositivo o contexto de dispositivo de Direct3D.


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



## <a name="create-the-swap-chain"></a>Crear la cadena de intercambio

Bien: tiene una ventana en la que dibujar y tiene una interfaz para enviar datos y proporcionar comandos a la GPU. Ahora veamos cómo unirlos.

En primer lugar, se indica a DXGI qué valores se deben usar para las propiedades de la cadena de intercambio. Para ello, use una estructura de [**DESC de cadena de intercambio de DXGI \_ \_ \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) . Los seis campos son especialmente importantes para las aplicaciones de escritorio:

-   **Windowed**: indica si la cadena de intercambio está en pantalla completa o recortada en la ventana. Establézcalo en TRUE para colocar la cadena de intercambio en la ventana que creó anteriormente.
-   **BufferUsage**: establezca este valor en \_ salida de destino de representación de uso de DXGI \_ \_ \_ . Esto indica que la cadena de intercambio será una superficie de dibujo, lo que le permite usarlo como destino de representación de Direct3D.
-   **SwapEffect**: establezca este valor en el efecto de intercambio de DXGI \_ \_ \_ volteo \_ secuencial.
-   **Format**: el formato de DXGI \_ \_ B8G8R8A8 \_ UNORM format especifica el color de 32 bits: 8 bits para cada uno de los tres canales de color RGB y 8 bits para el canal alfa.
-   **BufferCount**: establezca este valor en 2 para un comportamiento tradicional de búfer doble para evitar el desbordamiento. Establezca el número de búferes en 3 si el contenido de los gráficos toma más de un ciclo de actualización del monitor para representar un solo fotograma (en 60 Hz por ejemplo, el umbral es superior a 16 ms).
-   **SampleDesc**: este campo controla el muestreo múltiple. Establezca **recuento** en 1 y **calidad** en 0 para las cadenas de intercambio del modelo de volteo. (Para usar el muestreo múltiple con cadenas de intercambio de modelo Flip, dibuje en un destino de representación multimuestreado independiente y, a continuación, resuelva ese destino en la cadena de intercambio justo antes de presentarlo. El código de ejemplo se proporciona en el [muestreo múltiple en aplicaciones de la tienda Windows](/previous-versions/windows/apps/dn458384(v=win.10))).

Después de especificar una configuración para la cadena de intercambio, debe usar el mismo generador de DXGI que creó el dispositivo Direct3D (y el contexto de dispositivo) para crear la cadena de intercambio.

**Forma abreviada:  **

Obtenga la referencia de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que creó anteriormente. Vuelva a convertirlo en [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (si aún no lo ha hecho) y, después, llame a [**IDXGIDevice:: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) para adquirir el adaptador de DXGI. Obtener el generador primario para ese adaptador llamando a [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) hereda de [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)): ahora puede usar ese generador para crear la cadena de intercambio llamando a [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), como se muestra en el ejemplo de código siguiente.


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



Si acaba de empezar, probablemente sea mejor usar la configuración que se muestra aquí. En este momento, si ya está familiarizado con las versiones anteriores de DirectX, puede que esté preguntando: "¿por qué no hemos creado el dispositivo y la cadena de intercambio al mismo tiempo, en lugar de recorrer todas esas clases?" La respuesta es la eficiencia: las cadenas de intercambio son recursos de dispositivo de Direct3D y los recursos de dispositivo están vinculados al dispositivo Direct3D concreto que los creó. Si crea un dispositivo nuevo con una cadena de intercambio nueva, tendrá que volver a crear todos los recursos de dispositivo mediante el nuevo dispositivo Direct3D. Por lo tanto, al crear la cadena de intercambio con el mismo generador (como se mostró anteriormente), podrá volver a crear la cadena de intercambio y seguir usando los recursos de dispositivo Direct3D que ya ha cargado.

Ahora tiene una ventana del sistema operativo, una manera de tener acceso a la GPU y sus recursos, y una cadena de intercambio para mostrar los resultados de la representación. Lo único que queda es conectar todo el conjunto.

## <a name="create-a-render-target-for-drawing"></a>Crear un destino de representación para dibujar

La canalización del sombreador necesita un recurso para dibujar píxeles. La manera más sencilla de crear este recurso es definir un recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) como un búfer de reserva para que el sombreador de píxeles dibuje en y, a continuación, leer esa textura en la cadena de intercambio.

Para ello, cree una *vista* de representación y destino. En Direct3D, una vista es una manera de tener acceso a un recurso específico. En este caso, la vista permite que el sombreador de píxeles escriba en la textura a medida que completa sus operaciones por píxel.

Echemos un vistazo al código para esto. Al establecer la \_ \_ \_ \_ salida de destino de representación de uso de DXGI en la cadena de intercambio, que permitía usar el recurso de Direct3D subyacente como una superficie de dibujo. Por lo tanto, para obtener la vista de destino de representación, solo necesitamos obtener el búfer de reserva de la cadena de intercambio y crear una vista de destino de presentación enlazada al recurso de búfer de reserva.


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



Cree también un *búfer de estarcido de profundidad*. Un búfer de estarcido de profundidad es simplemente una forma determinada de recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , que normalmente se usa para determinar qué píxeles tienen prioridad de dibujo durante la rasterización en función de la distancia de los objetos de la escena de la cámara. Un búfer de estarcido de profundidad también se puede utilizar para los efectos de estarcido, donde los píxeles específicos se descartan o se omiten durante la rasterización. Este búfer debe tener el mismo tamaño que el destino de representación. Tenga en cuenta que no puede leer o representar en la textura de la galería de símbolos de profundidad del búfer de fotogramas porque la canalización del sombreador la usa exclusivamente antes y durante la rasterización final.

Cree también una vista para el búfer de estarcido de profundidad como [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). La vista indica a la canalización del sombreador cómo interpretar el recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) subyacente, por lo que si no se proporciona esta vista, no se realiza ninguna prueba de profundidad por píxel y los objetos de la escena pueden parecer un poco dentro del tiempo de espera.


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



El último paso es crear una ventanilla. Esto define el rectángulo visible del búfer de reserva que se muestra en la pantalla. puede cambiar la parte del búfer que se muestra en la pantalla cambiando los parámetros de la ventanilla. Este código tiene como destino todo el tamaño de la ventana, o la resolución de pantalla, en el caso de las cadenas de intercambio de pantalla completa. Por diversión, cambie los valores de las coordenadas proporcionadas y observe los resultados.


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



Y eso es cómo pasar de nada a dibujar píxeles en una ventana. A medida que empieza, es una buena idea familiarizarse con el modo en que DirectX, a través de DXGI, administra los recursos principales que necesita para empezar a dibujar píxeles.

A continuación, examinará la estructura de la canalización de gráficos. consulte [Descripción de la canalización de representación de la plantilla de aplicación de DirectX](understand-the-directx-11-2-graphics-pipeline.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Siguiente**
</dt> <dt>

[Trabajar con sombreadores y recursos del sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 