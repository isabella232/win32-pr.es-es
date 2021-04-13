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
# <a name="work-with-directx-device-resources"></a><span data-ttu-id="1b72b-103">Trabajar con recursos de dispositivos DirectX</span><span class="sxs-lookup"><span data-stu-id="1b72b-103">Work with DirectX device resources</span></span>

<span data-ttu-id="1b72b-104">Comprenda el rol de la infraestructura de gráficos de Microsoft DirectX (DXGI) en el juego DirectX de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="1b72b-104">Understand the role of the Microsoft DirectX Graphics Infrastructure (DXGI) in your Windows Store DirectX game.</span></span> <span data-ttu-id="1b72b-105">DXGI es un conjunto de API que se usan para configurar y administrar los gráficos de bajo nivel y los recursos del adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1b72b-105">DXGI is a set of APIs used to configure and manage low-level graphics and graphics adapter resources.</span></span> <span data-ttu-id="1b72b-106">Sin él, no tendría ninguna manera de dibujar los gráficos del juego en una ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-106">Without it, you'd have no way to draw your game's graphics to a window.</span></span>

<span data-ttu-id="1b72b-107">Piense en DXGI de esta manera: para acceder directamente a la GPU y administrar sus recursos, debe tener una manera de describirla en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b72b-107">Think of DXGI this way: to directly access the GPU and manage its resources, you must have a way to describe it to your app.</span></span> <span data-ttu-id="1b72b-108">La parte más importante de la información que necesita sobre la GPU es el lugar para dibujar píxeles de modo que pueda enviar esos píxeles a la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1b72b-108">The most important piece of info you need about the GPU is the place to draw pixels so it can send those pixels to the screen.</span></span> <span data-ttu-id="1b72b-109">Normalmente, esto se denomina "búfer de reserva", una ubicación en la memoria de GPU en la que puede dibujar los píxeles y, a continuación, hacer que se "volteo" o "intercambie" y se envíen a la pantalla en una señal de actualización.</span><span class="sxs-lookup"><span data-stu-id="1b72b-109">Typically this is called the "back buffer"—a location in GPU memory where you can draw the pixels and then have it "flipped" or "swapped" and sent to the screen on a refresh signal.</span></span> <span data-ttu-id="1b72b-110">DXGI le permite adquirir esa ubicación y los medios para usar ese búfer (denominado *cadena de intercambio* porque es una cadena de búferes intercambiables, lo que permite varias estrategias de almacenamiento en búfer).</span><span class="sxs-lookup"><span data-stu-id="1b72b-110">DXGI lets you acquire that location and the means to use that buffer (called a *swap chain* because it is a chain of swappable buffers, allowing for multiple buffering strategies).</span></span>

<span data-ttu-id="1b72b-111">Para ello, necesita acceso para escribir en la cadena de intercambio y un identificador de la ventana que mostrará el búfer de reserva actual de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="1b72b-111">To do this, you need access to write to the swap chain, and a handle to the window that will display the current back buffer for the swap chain.</span></span> <span data-ttu-id="1b72b-112">También debe conectar los dos para asegurarse de que el sistema operativo actualizará la ventana con el contenido del búfer de reserva cuando se lo solicite.</span><span class="sxs-lookup"><span data-stu-id="1b72b-112">You also need to connect the two to ensure that the operating system will refresh the window with the contents of the back buffer when you request it to do so.</span></span>

<span data-ttu-id="1b72b-113">El proceso general para dibujar en la pantalla es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="1b72b-113">The overall process for drawing to the screen is as follows:</span></span>

-   <span data-ttu-id="1b72b-114">Obtiene un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b72b-114">Get a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) for your app.</span></span>
-   <span data-ttu-id="1b72b-115">Obtiene una interfaz para el dispositivo Direct3D y el contexto.</span><span class="sxs-lookup"><span data-stu-id="1b72b-115">Get an interface for the Direct3D device and context.</span></span>
-   <span data-ttu-id="1b72b-116">Cree la cadena de intercambio para mostrar la imagen representada en [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="1b72b-116">Create the swap chain to display your rendered image in the [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>
-   <span data-ttu-id="1b72b-117">Cree un destino de representación para dibujar y rellenarlo con píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b72b-117">Create a render target for drawing and populate it with pixels.</span></span>
-   <span data-ttu-id="1b72b-118">Presente la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="1b72b-118">Present the swap chain!</span></span>

## <a name="create-a-window-for-your-app"></a><span data-ttu-id="1b72b-119">Crear una ventana para la aplicación</span><span class="sxs-lookup"><span data-stu-id="1b72b-119">Create a window for your app</span></span>

<span data-ttu-id="1b72b-120">Lo primero que debemos hacer es crear una ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-120">The first thing we need to do is create a window.</span></span> <span data-ttu-id="1b72b-121">En primer lugar, cree una clase de ventana rellenando una instancia de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)y regístrela mediante [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="1b72b-121">First, create a window class by populating an instance of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), then register it using [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="1b72b-122">La clase de ventana contiene propiedades esenciales de la ventana, incluido el icono que usa, la función de procesamiento de mensajes estático (más información más adelante) y un nombre único para la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-122">The window class contains essential properties of the window, including the icon it uses, the static message processing function (more on this later), and a unique name for the window class.</span></span>


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



<span data-ttu-id="1b72b-123">A continuación, cree la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-123">Next, you create the window.</span></span> <span data-ttu-id="1b72b-124">También es necesario proporcionar información de tamaño para la ventana y el nombre de la clase de ventana que acabamos de crear.</span><span class="sxs-lookup"><span data-stu-id="1b72b-124">We also need to provide size information for the window and the name of the window class we just created.</span></span> <span data-ttu-id="1b72b-125">Cuando se llama a [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), se obtiene un puntero opaco a la ventana denominada HWND; deberá mantener el puntero HWND y usarlo en cualquier momento que necesite hacer referencia a la ventana, incluida la destrucción o la recreación, y (especialmente importante) al crear la cadena de intercambio de DXGI que usa para dibujar en la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-125">When you call [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), you get back an opaque pointer to the window called an HWND; you'll need to keep the HWND pointer and use it any time you need to reference the window, including destroying or recreating it, and (especially important) when creating the DXGI swap chain you use to draw in the window.</span></span>


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



<span data-ttu-id="1b72b-126">El modelo de aplicación de escritorio de Windows incluye un enlace en el bucle de mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="1b72b-126">The Windows desktop app model includes a hook into the Windows message loop.</span></span> <span data-ttu-id="1b72b-127">Deberá basar el bucle principal del programa de este enlace escribiendo una función "StaticWindowProc" para procesar los eventos de ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-127">You'll need to base your main program loop off of this hook by writing a "StaticWindowProc" function to process windowing events.</span></span> <span data-ttu-id="1b72b-128">Debe ser una función estática, ya que Windows la llamará fuera del contexto de cualquier instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="1b72b-128">This must be a static function because Windows will call it outside of the context of any class instance.</span></span> <span data-ttu-id="1b72b-129">Este es un ejemplo muy sencillo de una función de procesamiento de mensajes estáticos.</span><span class="sxs-lookup"><span data-stu-id="1b72b-129">Here's a very simple example of a static message processing function.</span></span>


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



<span data-ttu-id="1b72b-130">En este sencillo ejemplo solo se comprueban las condiciones de salida del programa: el [**\_ cierre de WM**](/windows/desktop/winmsg/wm-close), el que se envía cuando se solicita el cierre de la ventana y la [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy), que se envía después de que la ventana se quite realmente de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1b72b-130">This simple example only checks for program exit conditions: [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), sent when the window is requested to be closed, and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), which is sent after the window is actually removed from the screen.</span></span> <span data-ttu-id="1b72b-131">Una aplicación completa de producción debe controlar también otros eventos de ventana. para obtener la lista completa de eventos de ventana, vea [notificaciones de ventana](/windows/desktop/winmsg/window-notifications).</span><span class="sxs-lookup"><span data-stu-id="1b72b-131">A full, production app needs to handle other windowing events too—for the complete list of windowing events, see [Window Notifications](/windows/desktop/winmsg/window-notifications).</span></span>

<span data-ttu-id="1b72b-132">El propio bucle del programa principal debe confirmar los mensajes de Windows permitiendo a Windows la oportunidad de ejecutar el procedimiento de mensaje estático.</span><span class="sxs-lookup"><span data-stu-id="1b72b-132">The main program loop itself needs to acknowledge Windows messages by allowing Windows the opportunity to run the static message proc.</span></span> <span data-ttu-id="1b72b-133">Ayude a que el programa se ejecute de forma eficaz ramificando el comportamiento: cada iteración debe elegir procesar nuevos mensajes de Windows si están disponibles y, si no hay ningún mensaje en la cola, debe representar un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="1b72b-133">Help the program run efficiently by forking the behavior: each iteration should choose to process new Windows messages if they are available, and if no messages are in the queue it should render a new frame.</span></span> <span data-ttu-id="1b72b-134">Este es un ejemplo muy sencillo:</span><span class="sxs-lookup"><span data-stu-id="1b72b-134">Here's a very simple example:</span></span>


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a><span data-ttu-id="1b72b-135">Obtener una interfaz para el dispositivo y el contexto de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1b72b-135">Get an interface for the Direct3D device and context</span></span>

<span data-ttu-id="1b72b-136">El primer paso para usar Direct3D es adquirir una interfaz para el hardware de Direct3D (GPU), representada como instancias de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) y [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span><span class="sxs-lookup"><span data-stu-id="1b72b-136">The first step to using Direct3D is to acquire an interface for the Direct3D hardware (the GPU), represented as instances of [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span></span> <span data-ttu-id="1b72b-137">El primero es una representación virtual de los recursos de GPU y el último es una abstracción independiente del dispositivo de la canalización de representación y el proceso.</span><span class="sxs-lookup"><span data-stu-id="1b72b-137">The former is a virtual representation of the GPU resources, and the latter is a device-agnostic abstraction of the rendering pipeline and process.</span></span> <span data-ttu-id="1b72b-138">Esta es una manera fácil de pensar en ello: **ID3D11Device** contiene los métodos gráficos a los que llama con poca frecuencia, normalmente antes de que se produzca cualquier representación, para adquirir y configurar el conjunto de recursos que necesita para empezar a dibujar píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b72b-138">Here's an easy way to think of it: **ID3D11Device** contains the graphics methods you call infrequently, usually before any rendering occurs, to acquire and configure the set of resources you need to start drawing pixels.</span></span> <span data-ttu-id="1b72b-139">Por otro lado, **ID3D11DeviceContext** contiene los métodos a los que se llama cada fotograma: carga en búferes y vistas y otros recursos, cambiando la fusión de salida y el estado del rasterizador, administrando los sombreadores y dibujando los resultados de pasar esos recursos a través de los Estados y los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="1b72b-139">**ID3D11DeviceContext**, on the other hand, contains the methods you call every frame: loading in buffers and views and other resources, changing output-merger and rasterizer state, managing shaders, and drawing the results of passing those resources through the states and shaders.</span></span>

<span data-ttu-id="1b72b-140">Hay una parte muy importante de este proceso: establecer el nivel de características.</span><span class="sxs-lookup"><span data-stu-id="1b72b-140">There's one very important part of this process: setting the feature level.</span></span> <span data-ttu-id="1b72b-141">El nivel de característica indica a DirectX el nivel mínimo de hardware que admite la aplicación, con \_ \_ el nivel de característica de D3D \_ 9 \_ 1 como el conjunto de características más bajo y el nivel de característica de D3D \_ \_ \_ 11 \_ 1 como el valor más alto actual.</span><span class="sxs-lookup"><span data-stu-id="1b72b-141">The feature level tells DirectX the minimum level of hardware your app supports, with D3D\_FEATURE\_LEVEL\_9\_1 as the lowest feature set and D3D\_FEATURE\_LEVEL\_11\_1 as the current highest.</span></span> <span data-ttu-id="1b72b-142">Debe admitir 9 \_ 1 como mínimo si desea llegar al público más amplio posible.</span><span class="sxs-lookup"><span data-stu-id="1b72b-142">You should support 9\_1 as the minimum if you want to reach the widest possible audience.</span></span> <span data-ttu-id="1b72b-143">Tómese un tiempo para leer los niveles de [características](/previous-versions/windows/apps/hh994923(v=win.10)) de Direct3D y evalúe los niveles de características mínimo y máximo que desee que admita el juego y comprenda las implicaciones de su elección.</span><span class="sxs-lookup"><span data-stu-id="1b72b-143">Take some time to read up on Direct3D [feature levels](/previous-versions/windows/apps/hh994923(v=win.10)) and assess for yourself the minimum and maximum feature levels you want your game to support and to understand the implications of your choice.</span></span>

<span data-ttu-id="1b72b-144">Obtener referencias (punteros) en el dispositivo Direct3D y en el contexto del dispositivo y almacenarlas como variables de nivel de clase en la instancia de **DeviceResources** (como punteros inteligentes **ComPtr** ).</span><span class="sxs-lookup"><span data-stu-id="1b72b-144">Obtain references (pointers) to both the Direct3D device and device context and store them as class-level variables on the **DeviceResources** instance (as **ComPtr** smart pointers).</span></span> <span data-ttu-id="1b72b-145">Use estas referencias siempre que necesite tener acceso al dispositivo o contexto de dispositivo de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1b72b-145">Use these references whenever you need to access the Direct3D device or device context.</span></span>


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



## <a name="create-the-swap-chain"></a><span data-ttu-id="1b72b-146">Crear la cadena de intercambio</span><span class="sxs-lookup"><span data-stu-id="1b72b-146">Create the swap chain</span></span>

<span data-ttu-id="1b72b-147">Bien: tiene una ventana en la que dibujar y tiene una interfaz para enviar datos y proporcionar comandos a la GPU.</span><span class="sxs-lookup"><span data-stu-id="1b72b-147">Okay: You have a window to draw in, and you have an interface to send data and give commands to the GPU.</span></span> <span data-ttu-id="1b72b-148">Ahora veamos cómo unirlos.</span><span class="sxs-lookup"><span data-stu-id="1b72b-148">Now let's see how to bring them together.</span></span>

<span data-ttu-id="1b72b-149">En primer lugar, se indica a DXGI qué valores se deben usar para las propiedades de la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="1b72b-149">First, you tell DXGI what values to use for the properties of the swap chain.</span></span> <span data-ttu-id="1b72b-150">Para ello, use una estructura de [**DESC de cadena de intercambio de DXGI \_ \_ \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .</span><span class="sxs-lookup"><span data-stu-id="1b72b-150">Do this using a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span> <span data-ttu-id="1b72b-151">Los seis campos son especialmente importantes para las aplicaciones de escritorio:</span><span class="sxs-lookup"><span data-stu-id="1b72b-151">Six fields are particularly important for desktop apps:</span></span>

-   <span data-ttu-id="1b72b-152">**Windowed**: indica si la cadena de intercambio está en pantalla completa o recortada en la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-152">**Windowed**: Indicates whether the swap chain is full-screen or clipped to the window.</span></span> <span data-ttu-id="1b72b-153">Establézcalo en TRUE para colocar la cadena de intercambio en la ventana que creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1b72b-153">Set this to TRUE to put the swap chain in the window you created earlier.</span></span>
-   <span data-ttu-id="1b72b-154">**BufferUsage**: establezca este valor en \_ salida de destino de representación de uso de DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b72b-154">**BufferUsage**: Set this to DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT.</span></span> <span data-ttu-id="1b72b-155">Esto indica que la cadena de intercambio será una superficie de dibujo, lo que le permite usarlo como destino de representación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1b72b-155">This indicates that the swap chain will be a drawing surface, allowing you to use it as a Direct3D render-target.</span></span>
-   <span data-ttu-id="1b72b-156">**SwapEffect**: establezca este valor en el efecto de intercambio de DXGI \_ \_ \_ volteo \_ secuencial.</span><span class="sxs-lookup"><span data-stu-id="1b72b-156">**SwapEffect**: Set this to DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL.</span></span>
-   <span data-ttu-id="1b72b-157">**Format**: el formato de DXGI \_ \_ B8G8R8A8 \_ UNORM format especifica el color de 32 bits: 8 bits para cada uno de los tres canales de color RGB y 8 bits para el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="1b72b-157">**Format**: The DXGI\_FORMAT\_B8G8R8A8\_UNORM format specifies 32-bit color: 8 bits for each of the three RGB color channels, and 8 bits for the alpha channel.</span></span>
-   <span data-ttu-id="1b72b-158">**BufferCount**: establezca este valor en 2 para un comportamiento tradicional de búfer doble para evitar el desbordamiento.</span><span class="sxs-lookup"><span data-stu-id="1b72b-158">**BufferCount**: Set this to 2 for a traditional double-buffered behavior to avoid tearing.</span></span> <span data-ttu-id="1b72b-159">Establezca el número de búferes en 3 si el contenido de los gráficos toma más de un ciclo de actualización del monitor para representar un solo fotograma (en 60 Hz por ejemplo, el umbral es superior a 16 ms).</span><span class="sxs-lookup"><span data-stu-id="1b72b-159">Set the buffer count to 3 if your graphics content takes more than one monitor refresh cycle to render a single frame (at 60 Hz for example, the threshold is more than 16 ms).</span></span>
-   <span data-ttu-id="1b72b-160">**SampleDesc**: este campo controla el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="1b72b-160">**SampleDesc**: This field controls multisampling.</span></span> <span data-ttu-id="1b72b-161">Establezca **recuento** en 1 y **calidad** en 0 para las cadenas de intercambio del modelo de volteo.</span><span class="sxs-lookup"><span data-stu-id="1b72b-161">Set **Count** to 1 and **Quality** to 0 for flip-model swap chains.</span></span> <span data-ttu-id="1b72b-162">(Para usar el muestreo múltiple con cadenas de intercambio de modelo Flip, dibuje en un destino de representación multimuestreado independiente y, a continuación, resuelva ese destino en la cadena de intercambio justo antes de presentarlo.</span><span class="sxs-lookup"><span data-stu-id="1b72b-162">(To use multisampling with flip-model swap chains, draw on a separate multisampled render target and then resolve that target to the swap chain just before presenting it.</span></span> <span data-ttu-id="1b72b-163">El código de ejemplo se proporciona en el [muestreo múltiple en aplicaciones de la tienda Windows](/previous-versions/windows/apps/dn458384(v=win.10))).</span><span class="sxs-lookup"><span data-stu-id="1b72b-163">Example code is provided in [Multisampling in Windows Store apps](/previous-versions/windows/apps/dn458384(v=win.10)).)</span></span>

<span data-ttu-id="1b72b-164">Después de especificar una configuración para la cadena de intercambio, debe usar el mismo generador de DXGI que creó el dispositivo Direct3D (y el contexto de dispositivo) para crear la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="1b72b-164">After you have specified a configuration for the swap chain, you must use the same DXGI factory that created the Direct3D device (and device context) in order to create the swap chain.</span></span>

<span data-ttu-id="1b72b-165">**Forma abreviada:  **</span><span class="sxs-lookup"><span data-stu-id="1b72b-165">**Short form:  **</span></span>

<span data-ttu-id="1b72b-166">Obtenga la referencia de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que creó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1b72b-166">Get the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) reference you created previously.</span></span> <span data-ttu-id="1b72b-167">Vuelva a convertirlo en [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (si aún no lo ha hecho) y, después, llame a [**IDXGIDevice:: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) para adquirir el adaptador de DXGI.</span><span class="sxs-lookup"><span data-stu-id="1b72b-167">Upcast it to [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (if you haven't already) and then call [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) to acquire the DXGI adapter.</span></span> <span data-ttu-id="1b72b-168">Obtener el generador primario para ese adaptador llamando a [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) hereda de [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)): ahora puede usar ese generador para crear la cadena de intercambio llamando a [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b72b-168">Get the parent factory for that adapter by calling [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))—now you can use that factory to create the swap chain by calling [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), as seen in the following code sample.</span></span>


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



<span data-ttu-id="1b72b-169">Si acaba de empezar, probablemente sea mejor usar la configuración que se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="1b72b-169">If you're just starting out, it's probably best to use the configuration shown here.</span></span> <span data-ttu-id="1b72b-170">En este momento, si ya está familiarizado con las versiones anteriores de DirectX, puede que esté preguntando: "¿por qué no hemos creado el dispositivo y la cadena de intercambio al mismo tiempo, en lugar de recorrer todas esas clases?"</span><span class="sxs-lookup"><span data-stu-id="1b72b-170">Now at this point, if you are already familiar with previous versions of DirectX you might be asking: "Why didn't we create the device and swap chain at the same time, instead of walking back through all of those classes?"</span></span> <span data-ttu-id="1b72b-171">La respuesta es la eficiencia: las cadenas de intercambio son recursos de dispositivo de Direct3D y los recursos de dispositivo están vinculados al dispositivo Direct3D concreto que los creó.</span><span class="sxs-lookup"><span data-stu-id="1b72b-171">The answer is efficiency: swap chains are Direct3D device resources, and device resources are tied to the particular Direct3D device that created them.</span></span> <span data-ttu-id="1b72b-172">Si crea un dispositivo nuevo con una cadena de intercambio nueva, tendrá que volver a crear todos los recursos de dispositivo mediante el nuevo dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1b72b-172">If you create a new device with a new swap chain, you have to recreate all your device resources using the new Direct3D device.</span></span> <span data-ttu-id="1b72b-173">Por lo tanto, al crear la cadena de intercambio con el mismo generador (como se mostró anteriormente), podrá volver a crear la cadena de intercambio y seguir usando los recursos de dispositivo Direct3D que ya ha cargado.</span><span class="sxs-lookup"><span data-stu-id="1b72b-173">So by creating the swap chain with the same factory (as shown above), you are able to recreate the swap chain and continue using the Direct3D device resources you already have loaded!</span></span>

<span data-ttu-id="1b72b-174">Ahora tiene una ventana del sistema operativo, una manera de tener acceso a la GPU y sus recursos, y una cadena de intercambio para mostrar los resultados de la representación.</span><span class="sxs-lookup"><span data-stu-id="1b72b-174">Now you've got a window from the operating system, a way to access the GPU and its resources, and a swap chain to display the rendering results.</span></span> <span data-ttu-id="1b72b-175">Lo único que queda es conectar todo el conjunto.</span><span class="sxs-lookup"><span data-stu-id="1b72b-175">All that's left is to wire the whole thing together!</span></span>

## <a name="create-a-render-target-for-drawing"></a><span data-ttu-id="1b72b-176">Crear un destino de representación para dibujar</span><span class="sxs-lookup"><span data-stu-id="1b72b-176">Create a render target for drawing</span></span>

<span data-ttu-id="1b72b-177">La canalización del sombreador necesita un recurso para dibujar píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b72b-177">The shader pipeline needs a resource to draw pixels into.</span></span> <span data-ttu-id="1b72b-178">La manera más sencilla de crear este recurso es definir un recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) como un búfer de reserva para que el sombreador de píxeles dibuje en y, a continuación, leer esa textura en la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="1b72b-178">The simplest way to create this resource is to define a [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource as a back buffer for the pixel shader to draw into, and then read that texture into the swap chain.</span></span>

<span data-ttu-id="1b72b-179">Para ello, cree una *vista* de representación y destino.</span><span class="sxs-lookup"><span data-stu-id="1b72b-179">To do this, you create a render-target *view*.</span></span> <span data-ttu-id="1b72b-180">En Direct3D, una vista es una manera de tener acceso a un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="1b72b-180">In Direct3D, a view is a way to access a specific resource.</span></span> <span data-ttu-id="1b72b-181">En este caso, la vista permite que el sombreador de píxeles escriba en la textura a medida que completa sus operaciones por píxel.</span><span class="sxs-lookup"><span data-stu-id="1b72b-181">In this case, the view enables the pixel shader to write into the texture as it completes its per-pixel operations.</span></span>

<span data-ttu-id="1b72b-182">Echemos un vistazo al código para esto.</span><span class="sxs-lookup"><span data-stu-id="1b72b-182">Let's look at the code for this.</span></span> <span data-ttu-id="1b72b-183">Al establecer la \_ \_ \_ \_ salida de destino de representación de uso de DXGI en la cadena de intercambio, que permitía usar el recurso de Direct3D subyacente como una superficie de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1b72b-183">When you set DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT on the swap chain, that enabled the underlying Direct3D resource to be used as a drawing surface.</span></span> <span data-ttu-id="1b72b-184">Por lo tanto, para obtener la vista de destino de representación, solo necesitamos obtener el búfer de reserva de la cadena de intercambio y crear una vista de destino de presentación enlazada al recurso de búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="1b72b-184">So to get our render target view, we just need to get the back buffer from the swap chain and create a render target view bound to the back buffer resource.</span></span>


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



<span data-ttu-id="1b72b-185">Cree también un *búfer de estarcido de profundidad*.</span><span class="sxs-lookup"><span data-stu-id="1b72b-185">Also create a *depth-stencil buffer*.</span></span> <span data-ttu-id="1b72b-186">Un búfer de estarcido de profundidad es simplemente una forma determinada de recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , que normalmente se usa para determinar qué píxeles tienen prioridad de dibujo durante la rasterización en función de la distancia de los objetos de la escena de la cámara.</span><span class="sxs-lookup"><span data-stu-id="1b72b-186">A depth-stencil buffer is just a particular form of [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource, which is typically used to determine which pixels have draw priority during rasterization based on the distance of the objects in the scene from the camera.</span></span> <span data-ttu-id="1b72b-187">Un búfer de estarcido de profundidad también se puede utilizar para los efectos de estarcido, donde los píxeles específicos se descartan o se omiten durante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="1b72b-187">A depth-stencil buffer can also be used for stencil effects, where specific pixels are discarded or ignored during rasterization.</span></span> <span data-ttu-id="1b72b-188">Este búfer debe tener el mismo tamaño que el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1b72b-188">This buffer must be the same size as the render target.</span></span> <span data-ttu-id="1b72b-189">Tenga en cuenta que no puede leer o representar en la textura de la galería de símbolos de profundidad del búfer de fotogramas porque la canalización del sombreador la usa exclusivamente antes y durante la rasterización final.</span><span class="sxs-lookup"><span data-stu-id="1b72b-189">Note that you cannot read from or render to the frame buffer depth-stencil texture because it is used exclusively by the shader pipeline before and during final rasterization.</span></span>

<span data-ttu-id="1b72b-190">Cree también una vista para el búfer de estarcido de profundidad como [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="1b72b-190">Also create a view for the depth-stencil buffer as an [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span></span> <span data-ttu-id="1b72b-191">La vista indica a la canalización del sombreador cómo interpretar el recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) subyacente, por lo que si no se proporciona esta vista, no se realiza ninguna prueba de profundidad por píxel y los objetos de la escena pueden parecer un poco dentro del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="1b72b-191">The view tells the shader pipeline how to interpret the underlying [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource - so if you don't supply this view no per-pixel depth testing is performed, and the objects in your scene may seem a bit inside-out at the very least!</span></span>


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



<span data-ttu-id="1b72b-192">El último paso es crear una ventanilla.</span><span class="sxs-lookup"><span data-stu-id="1b72b-192">The last step is to create a viewport.</span></span> <span data-ttu-id="1b72b-193">Esto define el rectángulo visible del búfer de reserva que se muestra en la pantalla. puede cambiar la parte del búfer que se muestra en la pantalla cambiando los parámetros de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="1b72b-193">This defines the visible rectangle of the back buffer displayed on the screen; you can change the part of the buffer that is displayed on the screen by changing the parameters of the viewport.</span></span> <span data-ttu-id="1b72b-194">Este código tiene como destino todo el tamaño de la ventana, o la resolución de pantalla, en el caso de las cadenas de intercambio de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="1b72b-194">This code targets the whole window size—or the screen resolution, in the case of full-screen swap chains.</span></span> <span data-ttu-id="1b72b-195">Por diversión, cambie los valores de las coordenadas proporcionadas y observe los resultados.</span><span class="sxs-lookup"><span data-stu-id="1b72b-195">For fun, change the supplied coordinate values and observe the results.</span></span>


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



<span data-ttu-id="1b72b-196">Y eso es cómo pasar de nada a dibujar píxeles en una ventana.</span><span class="sxs-lookup"><span data-stu-id="1b72b-196">And that's how you go from nothing to drawing pixels in a window!</span></span> <span data-ttu-id="1b72b-197">A medida que empieza, es una buena idea familiarizarse con el modo en que DirectX, a través de DXGI, administra los recursos principales que necesita para empezar a dibujar píxeles.</span><span class="sxs-lookup"><span data-stu-id="1b72b-197">As you start out, it's a good idea to become familiar with how DirectX, through DXGI, manages the core resources you need to start drawing pixels.</span></span>

<span data-ttu-id="1b72b-198">A continuación, examinará la estructura de la canalización de gráficos. consulte [Descripción de la canalización de representación de la plantilla de aplicación de DirectX](understand-the-directx-11-2-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="1b72b-198">Next you'll look at the structure of the graphics pipeline; see [Understand the DirectX app template's rendering pipeline](understand-the-directx-11-2-graphics-pipeline.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b72b-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b72b-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1b72b-200">**Siguiente**</span><span class="sxs-lookup"><span data-stu-id="1b72b-200">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="1b72b-201">Trabajar con sombreadores y recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="1b72b-201">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 