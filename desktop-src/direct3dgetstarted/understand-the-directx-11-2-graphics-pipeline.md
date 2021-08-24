---
title: Información sobre la canalización de representación de Direct3D 11
description: Anteriormente, ha visto cómo crear una ventana que puede usar para dibujar en Trabajar con recursos de dispositivo DirectX. Ahora, aprenderá a crear la canalización de gráficos y a dónde puede enlazarla.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41a3e0fa7e3f7775c5cd51d49f9867864e7a204975fd982565491a63db829aa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727525"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Información sobre la canalización de representación de Direct3D 11

Anteriormente, ha visto cómo crear una ventana que puede usar para dibujar en [Trabajar con recursos de dispositivo DirectX.](work-with-dxgi.md) Ahora, aprenderá a crear la canalización de gráficos y a dónde puede enlazarla.

Recuerde que hay dos interfaces de Direct3D que definen la canalización de gráficos: [**ID3D11Device,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2)que proporciona una representación virtual de la GPU y sus recursos. e [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), que representa el procesamiento de gráficos para la canalización. Normalmente, se usa una instancia de **ID3D11Device** para configurar y obtener los recursos de GPU que necesita para empezar a procesar los gráficos en una escena, y se usa **ID3D11DeviceContext** para procesar esos recursos en cada fase de sombreador adecuada de la canalización de gráficos. Normalmente se llama **a los métodos ID3D11Device** con poca frecuencia, es decir, solo cuando se configura una escena o cuando cambia el dispositivo. Por otro lado, llamará a **ID3D11DeviceContext** cada vez que procese un fotograma para mostrarlo.

En este ejemplo se crea y configura una canalización de gráficos mínima adecuada para mostrar un cubo con sombreado de vértice simple. Muestra aproximadamente el conjunto más pequeño de recursos necesarios para su presentación. A medida que lea la información aquí, tenga en cuenta las limitaciones del ejemplo dado, donde es posible que tenga que ampliarla para admitir la escena que desea representar.

En este ejemplo se tratan dos clases de C++ para gráficos: una clase del administrador de recursos de dispositivo y una clase de representador de escena 3D. Este tema se centra específicamente en el representador de escena 3D.

## <a name="what-does-the-cube-renderer-do"></a>¿Qué hace el representador de cubos?

La canalización de gráficos se define mediante la clase de representador de escena 3D. El representador de la escena puede:

-   Defina búferes constantes para almacenar los datos uniformes.
-   Defina búferes de vértices para contener los datos de vértices de objeto y los búferes de índice correspondientes para permitir que el sombreador de vértices recorrido los triángulos correctamente.
-   Cree recursos de textura y vistas de recursos.
-   Cargue los objetos del sombreador.
-   Actualice los datos gráficos para mostrar cada fotograma.
-   Representar (dibujar) los gráficos en la cadena de intercambio.

Los cuatro primeros procesos suelen usar los métodos de interfaz [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) para inicializar y administrar recursos gráficos, y los dos últimos usan los métodos de interfaz [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) para administrar y ejecutar la canalización de gráficos.

Se crea una instancia **de la clase Renderer** y se administra como una variable miembro en la clase de proyecto principal. La **instancia deviceResources** se administra como un puntero compartido entre  varias clases, incluida la clase de proyecto principal, la clase del proveedor de vistas App y **el representador**. Si reemplaza **Renderer por** su propia clase, considere la posibilidad de declarar y asignar también la instancia **DeviceResources** como miembro de puntero compartido:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Simplemente pase el puntero al constructor de clase (u otro método de inicialización) después de crear la instancia **DeviceResources** en el método **Initialize** de la **clase App.** También puede pasar una referencia **\_ ptr** débil si, en su lugar, quiere que la clase principal sea la propietaria por completo de **la instancia DeviceResources.**

## <a name="create-the-cube-renderer"></a>Creación del representador de cubos

En este ejemplo, organizamos la clase de representador de escena con los métodos siguientes:

-   **CreateDeviceDependentResources:** se llama cada vez que se debe inicializar o reiniciar la escena. Este método carga los datos iniciales de vértices, texturas, sombreadores y otros recursos, y construye los búferes iniciales de vértices y constantes. Normalmente, la mayor parte del trabajo aquí se realiza con [**métodos ID3D11Device,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) no con [**métodos ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)
-   **CreateWindowSizeDependentResources:** se llama cada vez que cambia el estado de la ventana, como cuando se produce el cambio de tamaño o cuando cambia la orientación. Este método vuelve a generar matrices de transformación, como las de la cámara.
-   **Update:** normalmente se llama desde la parte del programa que administra el estado inmediato del juego; en este ejemplo, simplemente lo llamamos desde la **clase Main.** Haga que este método lea de cualquier información de estado del juego que afecte a la representación, como las actualizaciones de la posición del objeto o los fotogramas de animación, además de los datos globales del juego, como los niveles de luz o los cambios en la física del juego. Estas entradas se usan para actualizar los búferes constantes por fotograma y los datos de objeto.
-   **Render:** normalmente se llama desde la parte del programa que administra el bucle de juego; En este caso, se llama desde la **clase Main.** Este método construye la canalización de gráficos: enlaza sombreadores, enlaza búferes y recursos a las fases del sombreador e invoca el dibujo para el marco actual.

Estos métodos componen el cuerpo de los comportamientos para representar una escena con Direct3D mediante los recursos. Si extiende este ejemplo con una nueva clase de representación, declare en la clase de proyecto principal. Por lo tanto, esto:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

se transforma en:

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

De nuevo, tenga en cuenta que en este ejemplo se supone que los métodos tienen las mismas firmas en la implementación. Si las firmas han cambiado, revise el **bucle Main** y realice los cambios en consecuencia.

Echemos un vistazo a los métodos de representación de escena con más detalle.

## <a name="create-device-dependent-resources"></a>Creación de recursos dependientes del dispositivo

**CreateDeviceDependentResources** consolida todas las operaciones para inicializar la escena y sus recursos mediante [**llamadas ID3D11Device.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) Este método supone que el dispositivo Direct3D se acaba de inicializar (o se ha recreado) para una escena. Vuelve a crear o volver a cargar todos los recursos gráficos específicos de la escena, como los sombreadores de vértices y píxeles, los búferes de vértice e índice para objetos y cualquier otro recurso (por ejemplo, como texturas y sus vistas correspondientes).

Este es el código de ejemplo **para CreateDeviceDependentResources:**


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



Cada vez que se cargan recursos desde el disco (recursos como archivos de objeto de sombreador compilados (CSO o .cso) o texturas, lo hacen de forma asincrónica. Esto le permite mantener otro trabajo al mismo tiempo (como otras tareas de configuración) y, como el bucle principal no está bloqueado, puede seguir mostrando algo visualmente interesante para el usuario (como una animación de carga para el juego). En este ejemplo se usa concurrency::Tasks API que está disponible a partir de Windows 8; Tenga en cuenta la sintaxis lambda utilizada para encapsular las tareas de carga asincrónicas. Estas expresiones lambda representan las funciones llamadas off-thread, por lo que se captura explícitamente un puntero al objeto de clase actual **(** este ).

Este es un ejemplo de cómo puede cargar el código de bytes del sombreador:


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



Este es un ejemplo de cómo crear búferes de vértices e índices:


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



En este ejemplo no se carga ninguna malla ni textura. Debe crear los métodos para cargar los tipos de malla y textura específicos del juego y llamarlos de forma asincrónica.

Rellene aquí también los valores iniciales de los búferes constantes por escena. Entre los ejemplos de búfer constante por escena se incluyen luces fijas u otros elementos y datos de la escena estática.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementación del método CreateWindowSizeDependentResources

**Se llama a los métodos CreateWindowSizeDependentResources** cada vez que cambia el tamaño, la orientación o la resolución de la ventana.

Los recursos de tamaño de ventana se actualizan de esta manera: el proceso de mensaje estático obtiene uno de varios eventos posibles que indican un cambio en el estado de la ventana. A continuación, se informa al bucle main sobre el evento y llama a **CreateWindowSizeDependentResources** en la instancia de clase principal, que llama a la implementación **CreateWindowSizeDependentResources** en la clase de representador de escena.

El trabajo principal de este método es asegurarse de que los objetos visuales no se confundan o no son válidos debido a un cambio en las propiedades de la ventana. En este ejemplo, actualizamos las matrices de proyecto con un nuevo campo de vista (FOV) para la ventana con cambio de tamaño o con reoriente.

Ya hemos visto el código para crear recursos de ventana en **DeviceResources,** que era la cadena de intercambio (con búfer de reserva) y representar la vista de destino. Este es el modo en que el representador crea transformaciones dependientes de la relación de aspecto:


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



Si la escena tiene un diseño específico de componentes que depende de la relación de aspecto, este es el lugar para reorganizarlos para que coincidan con esa relación de aspecto. Es posible que también quiera cambiar la configuración del comportamiento posterior al procesamiento aquí.

## <a name="implement-the-update-method"></a>Implementación del método Update

Se llama al método **Update** una vez por bucle de juego: en este ejemplo, el método de la clase principal lo llama con el mismo nombre. Tiene un propósito sencillo: actualizar la geometría de la escena y el estado del juego en función de la cantidad de tiempo transcurrido (o pasos de tiempo transcurrido) desde el fotograma anterior. En este ejemplo, simplemente giramos el cubo una vez por fotograma. En una escena de juego real, este método contiene mucho más código para comprobar el estado del juego, actualizar búferes constantes por fotograma (u otros dinámicos), búferes de geometría y otros recursos en memoria en consecuencia. Dado que la comunicación entre la CPU y la GPU incurre en sobrecarga, asegúrese de actualizar solo los búferes que han cambiado realmente desde el último fotograma: los búferes constantes se pueden agrupar o dividir, según sea necesario para que esto sea más eficaz.


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



En este caso, **Rotate** actualiza el búfer constante con una nueva matriz de transformación para el cubo. La matriz se multiplicará por vértice durante la fase del sombreador de vértices. Puesto que se llama a este método con cada fotograma, este es un buen lugar para agregar cualquier método que actualice los búferes dinámicos de vértices y constantes, o para realizar cualquier otra operación que prepare los objetos de la escena para la transformación mediante la canalización de gráficos.

## <a name="implement-the-render-method"></a>Implementación del método Render

Se llama a este método una vez por cada bucle de juego después de llamar **a Update**. Al **igual que Update,** también se llama al método **Render** desde la clase principal. Este es el método donde se construye y procesa la canalización de gráficos para el fotograma mediante métodos en la [**instancia ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) Esto se produce en una llamada final a [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). Es importante comprender que esta llamada (u otras llamadas Draw _ similares definidas en **\* *_* ID3D11DeviceContext)** ejecuta realmente la canalización. En concreto, esto se produce cuando Direct3D se comunica con la GPU para establecer el estado de dibujo, ejecuta cada fase de canalización y escribe los resultados de píxeles en el recurso de búfer de destino de representación para que los muestre la cadena de intercambio. Dado que la comunicación entre la CPU y la GPU incurre en sobrecarga, combine varias llamadas a draw en una sola, si es posible, especialmente si la escena tiene una gran cantidad de objetos representados.


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



Es un procedimiento recomendado establecer las distintas fases de canalización de gráficos en el contexto en orden. Normalmente, el orden es:

-   Actualice los recursos de búfer constante con datos nuevos según sea necesario (mediante los datos de **Update**).
-   Ensamblado de entrada (IA): aquí es donde se adjuntan los búferes de vértice e índice que definen la geometría de la escena. Debe adjuntar cada vértice y búfer de índice para cada objeto de la escena. Dado que este ejemplo tiene solo el cubo, es bastante sencillo.
-   Sombreador de vértices (VS): adjunte cualquier sombreador de vértices que transforme los datos de los búferes de vértices y adjunte búferes constantes para el sombreador de vértices.
-   Sombreador de píxeles (PS): adjunte cualquier sombreador de píxeles que realice operaciones por píxel en la escena rasterizada y adjunte los recursos del dispositivo para el sombreador de píxeles (búferes constantes, texturas, entre otros).
-   Fusión de salida (OM): esta es la fase en la que se mezclan los píxeles, una vez finalizados los sombreadores. Se trata de una excepción a la regla, ya que se adjuntan las galerías de símbolos de profundidad y se representan los destinos antes de establecer cualquiera de las demás fases. Puede tener varias galerías de símbolos y destinos si tiene sombreadores de vértices y píxeles adicionales que generan texturas como mapas de sombra, mapas de alto u otras técnicas de muestreo; en este caso, cada paso de dibujo necesitará los destinos adecuados antes de llamar a una función de dibujo.

A continuación, en la sección final[(Trabajar](work-with-shaders-and-shader-resources.md)con sombreadores y recursos de sombreador), examinaremos los sombreadores y analizaremos cómo los ejecuta Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Siguiente**
</dt> <dt>

[Trabajar con sombreadores y recursos de sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
