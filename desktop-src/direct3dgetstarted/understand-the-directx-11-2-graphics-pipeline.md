---
title: Descripción de la canalización de representación de Direct3D 11
description: Anteriormente, se examinó cómo crear una ventana que se puede usar para dibujar en el trabajo con los recursos de dispositivo de DirectX. Ahora, aprenderá a crear la canalización de gráficos y dónde puede enlazarla.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "105721323"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="37cdb-104">Descripción de la canalización de representación de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="37cdb-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="37cdb-105">Anteriormente, se examinó cómo crear una ventana que se puede usar para dibujar en el [trabajo con los recursos de dispositivo de DirectX](work-with-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="37cdb-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="37cdb-106">Ahora, aprenderá a crear la canalización de gráficos y dónde puede enlazarla.</span><span class="sxs-lookup"><span data-stu-id="37cdb-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="37cdb-107">Recordará que hay dos interfaces de Direct3D que definen la canalización de gráficos: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), que proporciona una representación virtual de la GPU y sus recursos; y [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), que representa el procesamiento de gráficos para la canalización.</span><span class="sxs-lookup"><span data-stu-id="37cdb-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="37cdb-108">Normalmente, se usa una instancia de **ID3D11Device** para configurar y obtener los recursos de GPU necesarios para iniciar el procesamiento de los gráficos en una escena, y se usa **ID3D11DeviceContext** para procesar esos recursos en cada fase del sombreador adecuada en la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="37cdb-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="37cdb-109">Normalmente, se llama a los métodos **ID3D11Device** con poca frecuencia, es decir, solo cuando se configura una escena o cuando el dispositivo cambia.</span><span class="sxs-lookup"><span data-stu-id="37cdb-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="37cdb-110">Por otro lado, llamará a **ID3D11DeviceContext** cada vez que procese un fotograma para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="37cdb-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="37cdb-111">En este ejemplo se crea y configura una canalización de gráficos mínima adecuada para mostrar un cubo simple de giro sombreado de vértices.</span><span class="sxs-lookup"><span data-stu-id="37cdb-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="37cdb-112">Muestra aproximadamente el conjunto más pequeño de recursos necesarios para la presentación.</span><span class="sxs-lookup"><span data-stu-id="37cdb-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="37cdb-113">Cuando lea la información aquí, tenga en cuenta las limitaciones del ejemplo determinado, donde puede que tenga que extenderlo para admitir la escena que desea representar.</span><span class="sxs-lookup"><span data-stu-id="37cdb-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="37cdb-114">En este ejemplo se tratan dos clases de C++ para gráficos: una clase de administrador de recursos de dispositivo y una clase de representador de escena 3D.</span><span class="sxs-lookup"><span data-stu-id="37cdb-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="37cdb-115">Este tema se centra específicamente en el representador de escenas 3D.</span><span class="sxs-lookup"><span data-stu-id="37cdb-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="37cdb-116">¿Qué hace el representador de cubos?</span><span class="sxs-lookup"><span data-stu-id="37cdb-116">What does the cube renderer do?</span></span>

<span data-ttu-id="37cdb-117">La canalización de gráficos se define mediante la clase de representador de escena 3D.</span><span class="sxs-lookup"><span data-stu-id="37cdb-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="37cdb-118">El representador de escenas puede:</span><span class="sxs-lookup"><span data-stu-id="37cdb-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="37cdb-119">Defina búferes constantes para almacenar los datos uniformes.</span><span class="sxs-lookup"><span data-stu-id="37cdb-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="37cdb-120">Defina los búferes de vértices para que contengan los datos del vértice del objeto y los búferes de índice correspondientes para permitir que el sombreador de vértices examine los triángulos correctamente.</span><span class="sxs-lookup"><span data-stu-id="37cdb-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="37cdb-121">Cree recursos de textura y vistas de recursos.</span><span class="sxs-lookup"><span data-stu-id="37cdb-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="37cdb-122">Cargue los objetos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="37cdb-122">Load your shader objects.</span></span>
-   <span data-ttu-id="37cdb-123">Actualice los datos de los gráficos para mostrar cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="37cdb-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="37cdb-124">Representar (dibujar) los gráficos en la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="37cdb-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="37cdb-125">Los primeros cuatro procesos suelen usar los métodos de la interfaz [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) para inicializar y administrar los recursos de gráficos, y los dos últimos usan los métodos de la interfaz [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) para administrar y ejecutar la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="37cdb-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="37cdb-126">Una instancia de la clase de **representador** se crea y se administra como una variable miembro en la clase de proyecto principal.</span><span class="sxs-lookup"><span data-stu-id="37cdb-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="37cdb-127">La instancia de **DeviceResources** se administra como un puntero compartido en varias clases, incluida la clase de proyecto principal, la clase de proveedor de vista de **aplicaciones** y el **representador**.</span><span class="sxs-lookup"><span data-stu-id="37cdb-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="37cdb-128">Si reemplaza **renderer** por su propia clase, considere la posibilidad de declarar y asignar la instancia de **DeviceResources** como un miembro de puntero compartido también:</span><span class="sxs-lookup"><span data-stu-id="37cdb-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="37cdb-129">Simplemente pase el puntero en el constructor de clase (u otro método de inicialización) después de crear la instancia de **DeviceResources** en el método **Initialize** de la clase **App** .</span><span class="sxs-lookup"><span data-stu-id="37cdb-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="37cdb-130">También puede pasar una referencia **\_ ptr débil** si, en su lugar, desea que la clase principal sea totalmente propietaria de la instancia de **DeviceResources** .</span><span class="sxs-lookup"><span data-stu-id="37cdb-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="37cdb-131">Crear el representador de cubos</span><span class="sxs-lookup"><span data-stu-id="37cdb-131">Create the cube renderer</span></span>

<span data-ttu-id="37cdb-132">En este ejemplo, se organiza la clase de representador de escena con los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="37cdb-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="37cdb-133">**CreateDeviceDependentResources**: se llama cada vez que se debe inicializar o reiniciar la escena.</span><span class="sxs-lookup"><span data-stu-id="37cdb-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="37cdb-134">Este método carga los datos de vértices iniciales, texturas, sombreadores y otros recursos, y construye los búferes de vértices y constantes iniciales.</span><span class="sxs-lookup"><span data-stu-id="37cdb-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="37cdb-135">Normalmente, la mayor parte del trabajo se realiza aquí con métodos [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , no con métodos [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="37cdb-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="37cdb-136">**CreateWindowSizeDependentResources**: se llama cada vez que cambia el estado de la ventana, por ejemplo, cuando se produce el cambio de tamaño o cuando cambia la orientación.</span><span class="sxs-lookup"><span data-stu-id="37cdb-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="37cdb-137">Este método vuelve a generar las matrices de transformación, como las de la cámara.</span><span class="sxs-lookup"><span data-stu-id="37cdb-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="37cdb-138">**Actualización**: se suele llamar desde la parte del programa que administra el estado inmediato del juego; en este ejemplo, solo se llama desde la clase **principal** .</span><span class="sxs-lookup"><span data-stu-id="37cdb-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="37cdb-139">Haga que este método Lea cualquier información de estado de juego que afecte a la representación, como las actualizaciones de la posición de objeto o fotogramas de animación, además de los datos de juego globales, como los niveles claros o los cambios en la física del juego.</span><span class="sxs-lookup"><span data-stu-id="37cdb-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="37cdb-140">Estas entradas se usan para actualizar los datos de objetos y los búferes de constantes por fotograma.</span><span class="sxs-lookup"><span data-stu-id="37cdb-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="37cdb-141">**Render**: suele llamarse desde la parte del programa que administra el bucle del juego. en este caso, se llama desde la clase **principal** .</span><span class="sxs-lookup"><span data-stu-id="37cdb-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="37cdb-142">Este método crea la canalización de gráficos: enlaza sombreadores, enlaza búferes y recursos a las fases del sombreador e invoca el dibujo del marco actual.</span><span class="sxs-lookup"><span data-stu-id="37cdb-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="37cdb-143">Estos métodos comprenden el cuerpo de los comportamientos para representar una escena con Direct3D mediante los recursos.</span><span class="sxs-lookup"><span data-stu-id="37cdb-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="37cdb-144">Si extiende este ejemplo con una nueva clase de representación, declárelo en la clase de proyecto principal.</span><span class="sxs-lookup"><span data-stu-id="37cdb-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="37cdb-145">Por lo tanto:</span><span class="sxs-lookup"><span data-stu-id="37cdb-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="37cdb-146">se transforma en:</span><span class="sxs-lookup"><span data-stu-id="37cdb-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="37cdb-147">De nuevo, tenga en cuenta que en este ejemplo se da por supuesto que los métodos tienen las mismas firmas en la implementación.</span><span class="sxs-lookup"><span data-stu-id="37cdb-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="37cdb-148">Si las firmas han cambiado, revise el bucle **principal** y realice los cambios en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="37cdb-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="37cdb-149">Echemos un vistazo a los métodos de representación de escenas con más detalle.</span><span class="sxs-lookup"><span data-stu-id="37cdb-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="37cdb-150">Crear recursos dependientes del dispositivo</span><span class="sxs-lookup"><span data-stu-id="37cdb-150">Create device dependent resources</span></span>

<span data-ttu-id="37cdb-151">**CreateDeviceDependentResources** consolida todas las operaciones para inicializar la escena y sus recursos mediante llamadas a [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) .</span><span class="sxs-lookup"><span data-stu-id="37cdb-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="37cdb-152">Este método supone que el dispositivo Direct3D se acaba de inicializar (o se ha creado de forma recreada) para una escena.</span><span class="sxs-lookup"><span data-stu-id="37cdb-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="37cdb-153">Vuelve a crear o recarga todos los recursos de gráficos específicos de la escena, como los sombreadores de vértices y píxeles, los búferes de vértices y de índices de los objetos, y cualquier otro recurso (por ejemplo, como texturas y sus vistas correspondientes).</span><span class="sxs-lookup"><span data-stu-id="37cdb-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="37cdb-154">Este es el código de ejemplo de **CreateDeviceDependentResources**:</span><span class="sxs-lookup"><span data-stu-id="37cdb-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



<span data-ttu-id="37cdb-155">Cada vez que carga recursos desde el disco (recursos como objetos de sombreador compilados (CSO o. CSO) o texturas, lo hace de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="37cdb-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="37cdb-156">Esto le permite mantener otro trabajo trabajando al mismo tiempo (como otras tareas de configuración) y, dado que el bucle principal no está bloqueado, puede seguir mostrando algo visualmente interesante para el usuario (por ejemplo, una animación de carga para el juego).</span><span class="sxs-lookup"><span data-stu-id="37cdb-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="37cdb-157">En este ejemplo se usa la API Concurrency:: Tasks que está disponible a partir de Windows 8. Tenga en cuenta la sintaxis lambda que se usa para encapsular tareas de carga asincrónica.</span><span class="sxs-lookup"><span data-stu-id="37cdb-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="37cdb-158">Estas expresiones lambda representan las funciones llamadas fuera de subproceso, por lo que se captura explícitamente un puntero al objeto de clase actual (**this**).</span><span class="sxs-lookup"><span data-stu-id="37cdb-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="37cdb-159">A continuación se muestra un ejemplo de cómo se puede cargar el código de bytes del sombreador:</span><span class="sxs-lookup"><span data-stu-id="37cdb-159">Here's an example of how you can load shader bytecode:</span></span>


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



<span data-ttu-id="37cdb-160">A continuación se muestra un ejemplo de cómo crear búferes de vértices y de índices:</span><span class="sxs-lookup"><span data-stu-id="37cdb-160">Here's an example of how to create vertex and index buffers:</span></span>


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



<span data-ttu-id="37cdb-161">En este ejemplo no se carga ninguna malla ni texturas.</span><span class="sxs-lookup"><span data-stu-id="37cdb-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="37cdb-162">Debe crear los métodos para cargar los tipos de malla y textura específicos del juego y llamarlos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="37cdb-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="37cdb-163">Rellene los valores iniciales de los búferes de constantes por escena aquí también.</span><span class="sxs-lookup"><span data-stu-id="37cdb-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="37cdb-164">Entre los ejemplos de búfer de constantes por escena se incluyen las luces fijas u otros elementos y datos de la escena estática.</span><span class="sxs-lookup"><span data-stu-id="37cdb-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="37cdb-165">Implementar el método CreateWindowSizeDependentResources</span><span class="sxs-lookup"><span data-stu-id="37cdb-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="37cdb-166">Se llama a los métodos **CreateWindowSizeDependentResources** cada vez que cambia el tamaño de la ventana, la orientación o la resolución.</span><span class="sxs-lookup"><span data-stu-id="37cdb-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="37cdb-167">Los recursos de tamaño de ventana se actualizan de la siguiente manera: el procedimiento de mensajes estáticos obtiene uno de varios posibles eventos que indican un cambio en el estado de la ventana.</span><span class="sxs-lookup"><span data-stu-id="37cdb-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="37cdb-168">A continuación, el bucle principal se informa del evento y llama a **CreateWindowSizeDependentResources** en la instancia de la clase principal, que luego llama a la implementación de **CreateWindowSizeDependentResources** en la clase de representador de la escena.</span><span class="sxs-lookup"><span data-stu-id="37cdb-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="37cdb-169">El trabajo principal de este método es asegurarse de que los objetos visuales no se confunden o no son válidos debido a un cambio en las propiedades de la ventana.</span><span class="sxs-lookup"><span data-stu-id="37cdb-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="37cdb-170">En este ejemplo, se actualizan las matrices del proyecto con un nuevo campo de vista (campo de campo) para la ventana cuyo tamaño se ha cambiado o se ha reorientado.</span><span class="sxs-lookup"><span data-stu-id="37cdb-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="37cdb-171">Ya hemos visto el código para crear recursos de ventana en **DeviceResources** , que era la cadena de intercambio (con el búfer de reserva) y la vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="37cdb-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="37cdb-172">Este es el modo en que el representador crea transformaciones dependientes de la relación de aspecto:</span><span class="sxs-lookup"><span data-stu-id="37cdb-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



<span data-ttu-id="37cdb-173">Si la escena tiene un diseño específico de componentes que depende de la relación de aspecto, es el lugar donde reorganizarlos para que coincidan con la relación de aspecto.</span><span class="sxs-lookup"><span data-stu-id="37cdb-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="37cdb-174">Puede que también desee cambiar la configuración del comportamiento posterior al procesamiento aquí.</span><span class="sxs-lookup"><span data-stu-id="37cdb-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="37cdb-175">Implementar el método Update</span><span class="sxs-lookup"><span data-stu-id="37cdb-175">Implement the Update method</span></span>

<span data-ttu-id="37cdb-176">Se llama al método **Update** una vez por cada bucle de juego; en este ejemplo, se llama mediante el método de la clase principal con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="37cdb-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="37cdb-177">Tiene un propósito sencillo: actualizar la geometría de la escena y el estado del juego en función de la cantidad de tiempo transcurrido (o de los pasos de tiempo transcurridos) desde el fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="37cdb-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="37cdb-178">En este ejemplo, simplemente giramos el cubo una vez por fotograma.</span><span class="sxs-lookup"><span data-stu-id="37cdb-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="37cdb-179">En una escena de juego real, este método contiene mucho más código para comprobar el estado del juego, actualizar los búferes de constantes de cada fotograma (u otros dinámicos), los búferes de geometría y otros recursos en memoria en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="37cdb-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="37cdb-180">Dado que la comunicación entre la CPU y la GPU incurre en una sobrecarga, asegúrese de que solo se actualizan los búferes que han cambiado desde el último fotograma: los búferes de constantes se pueden agrupar, o dividir, según sea necesario para que sea más eficaz.</span><span class="sxs-lookup"><span data-stu-id="37cdb-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



<span data-ttu-id="37cdb-181">En este caso, **girar** actualiza el búfer de constantes con una nueva matriz de transformación para el cubo.</span><span class="sxs-lookup"><span data-stu-id="37cdb-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="37cdb-182">La matriz se multiplicará por vértice durante la etapa del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="37cdb-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="37cdb-183">Dado que se llama a este método con cada fotograma, es un buen lugar para agregar métodos que actualicen los búferes de constantes y vértices dinámicos, o para realizar otras operaciones que preparen los objetos de la escena para su transformación por la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="37cdb-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="37cdb-184">Implementar el método Render</span><span class="sxs-lookup"><span data-stu-id="37cdb-184">Implement the Render method</span></span>

<span data-ttu-id="37cdb-185">Se llama a este método una vez por cada bucle de juego después de llamar a **Update**.</span><span class="sxs-lookup"><span data-stu-id="37cdb-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="37cdb-186">Al igual que la **actualización**, el método **Render** también se llama desde la clase principal.</span><span class="sxs-lookup"><span data-stu-id="37cdb-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="37cdb-187">Este es el método en el que la canalización de gráficos se construye y procesa para el marco mediante métodos en la instancia de [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="37cdb-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="37cdb-188">Esto culmina en una llamada final a [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span><span class="sxs-lookup"><span data-stu-id="37cdb-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="37cdb-189">Es importante comprender que esta llamada (u otras **\* *llamadas de Draw _ similares definidas en _* ID3D11DeviceContext**) ejecutan realmente la canalización.</span><span class="sxs-lookup"><span data-stu-id="37cdb-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="37cdb-190">En concreto, esto se produce cuando Direct3D se comunica con la GPU para establecer el estado del dibujo, ejecuta cada fase de canalización y escribe los resultados de píxeles en el recurso de búfer de destino de representación para su presentación en la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="37cdb-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="37cdb-191">Dado que la comunicación entre la CPU y la GPU incurre en una sobrecarga, combine varias llamadas a Draw en una sola si es posible, especialmente si la escena tiene muchos objetos representados.</span><span class="sxs-lookup"><span data-stu-id="37cdb-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



<span data-ttu-id="37cdb-192">Se recomienda establecer las distintas fases de canalización de gráficos en el contexto en orden.</span><span class="sxs-lookup"><span data-stu-id="37cdb-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="37cdb-193">Normalmente, el orden es:</span><span class="sxs-lookup"><span data-stu-id="37cdb-193">Typically, the order is:</span></span>

-   <span data-ttu-id="37cdb-194">Actualice los recursos de búfer constantes con nuevos datos según sea necesario (mediante la **actualización** de datos).</span><span class="sxs-lookup"><span data-stu-id="37cdb-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="37cdb-195">Ensamblado de entrada (IA): aquí es donde se adjuntan los búferes de vértices y de índices que definen la geometría de la escena.</span><span class="sxs-lookup"><span data-stu-id="37cdb-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="37cdb-196">Debe adjuntar cada vértice y búfer de índice para cada objeto de la escena.</span><span class="sxs-lookup"><span data-stu-id="37cdb-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="37cdb-197">Dado que este ejemplo solo tiene el cubo, es bastante sencillo.</span><span class="sxs-lookup"><span data-stu-id="37cdb-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="37cdb-198">Sombreador de vértices (VS): Adjunte cualquier sombreador de vértices que transforme los datos en los búferes de vértices y adjunte búferes de constantes para el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="37cdb-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="37cdb-199">Sombreador de píxeles (PS): Conecte los sombreadores de píxeles que realizarán operaciones por píxel en la escena rasterizada y conecte los recursos de dispositivo para el sombreador de píxeles (búferes de constantes, texturas, etc.).</span><span class="sxs-lookup"><span data-stu-id="37cdb-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="37cdb-200">Fusión de salida (OM): esta es la fase en la que se combinan los píxeles, una vez finalizados los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="37cdb-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="37cdb-201">Esta es una excepción a la regla, ya que se adjuntan las galerías de símbolos de profundidad y los destinos de representación antes de establecer cualquiera de las otras fases.</span><span class="sxs-lookup"><span data-stu-id="37cdb-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="37cdb-202">Puede tener varias galerías de símbolos y destinos si tiene sombreadores de vértices y píxeles adicionales que generan texturas como mapas de sombras, mapas de alto u otras técnicas de muestreo; en este caso, cada paso del dibujo necesitará los destinos adecuados establecidos antes de llamar a una función Draw.</span><span class="sxs-lookup"><span data-stu-id="37cdb-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="37cdb-203">Después, en la sección final ([trabajar con sombreadores y recursos del sombreador](work-with-shaders-and-shader-resources.md)), veremos los sombreadores y veremos cómo los ejecuta Direct3D.</span><span class="sxs-lookup"><span data-stu-id="37cdb-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37cdb-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37cdb-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="37cdb-205">**Siguiente**</span><span class="sxs-lookup"><span data-stu-id="37cdb-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="37cdb-206">Trabajar con sombreadores y recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="37cdb-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
