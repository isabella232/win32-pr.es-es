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
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Descripción de la canalización de representación de Direct3D 11

Anteriormente, se examinó cómo crear una ventana que se puede usar para dibujar en el [trabajo con los recursos de dispositivo de DirectX](work-with-dxgi.md). Ahora, aprenderá a crear la canalización de gráficos y dónde puede enlazarla.

Recordará que hay dos interfaces de Direct3D que definen la canalización de gráficos: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), que proporciona una representación virtual de la GPU y sus recursos; y [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), que representa el procesamiento de gráficos para la canalización. Normalmente, se usa una instancia de **ID3D11Device** para configurar y obtener los recursos de GPU necesarios para iniciar el procesamiento de los gráficos en una escena, y se usa **ID3D11DeviceContext** para procesar esos recursos en cada fase del sombreador adecuada en la canalización de gráficos. Normalmente, se llama a los métodos **ID3D11Device** con poca frecuencia, es decir, solo cuando se configura una escena o cuando el dispositivo cambia. Por otro lado, llamará a **ID3D11DeviceContext** cada vez que procese un fotograma para mostrarlo.

En este ejemplo se crea y configura una canalización de gráficos mínima adecuada para mostrar un cubo simple de giro sombreado de vértices. Muestra aproximadamente el conjunto más pequeño de recursos necesarios para la presentación. Cuando lea la información aquí, tenga en cuenta las limitaciones del ejemplo determinado, donde puede que tenga que extenderlo para admitir la escena que desea representar.

En este ejemplo se tratan dos clases de C++ para gráficos: una clase de administrador de recursos de dispositivo y una clase de representador de escena 3D. Este tema se centra específicamente en el representador de escenas 3D.

## <a name="what-does-the-cube-renderer-do"></a>¿Qué hace el representador de cubos?

La canalización de gráficos se define mediante la clase de representador de escena 3D. El representador de escenas puede:

-   Defina búferes constantes para almacenar los datos uniformes.
-   Defina los búferes de vértices para que contengan los datos del vértice del objeto y los búferes de índice correspondientes para permitir que el sombreador de vértices examine los triángulos correctamente.
-   Cree recursos de textura y vistas de recursos.
-   Cargue los objetos de sombreador.
-   Actualice los datos de los gráficos para mostrar cada fotograma.
-   Representar (dibujar) los gráficos en la cadena de intercambio.

Los primeros cuatro procesos suelen usar los métodos de la interfaz [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) para inicializar y administrar los recursos de gráficos, y los dos últimos usan los métodos de la interfaz [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) para administrar y ejecutar la canalización de gráficos.

Una instancia de la clase de **representador** se crea y se administra como una variable miembro en la clase de proyecto principal. La instancia de **DeviceResources** se administra como un puntero compartido en varias clases, incluida la clase de proyecto principal, la clase de proveedor de vista de **aplicaciones** y el **representador**. Si reemplaza **renderer** por su propia clase, considere la posibilidad de declarar y asignar la instancia de **DeviceResources** como un miembro de puntero compartido también:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Simplemente pase el puntero en el constructor de clase (u otro método de inicialización) después de crear la instancia de **DeviceResources** en el método **Initialize** de la clase **App** . También puede pasar una referencia **\_ ptr débil** si, en su lugar, desea que la clase principal sea totalmente propietaria de la instancia de **DeviceResources** .

## <a name="create-the-cube-renderer"></a>Crear el representador de cubos

En este ejemplo, se organiza la clase de representador de escena con los siguientes métodos:

-   **CreateDeviceDependentResources**: se llama cada vez que se debe inicializar o reiniciar la escena. Este método carga los datos de vértices iniciales, texturas, sombreadores y otros recursos, y construye los búferes de vértices y constantes iniciales. Normalmente, la mayor parte del trabajo se realiza aquí con métodos [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , no con métodos [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .
-   **CreateWindowSizeDependentResources**: se llama cada vez que cambia el estado de la ventana, por ejemplo, cuando se produce el cambio de tamaño o cuando cambia la orientación. Este método vuelve a generar las matrices de transformación, como las de la cámara.
-   **Actualización**: se suele llamar desde la parte del programa que administra el estado inmediato del juego; en este ejemplo, solo se llama desde la clase **principal** . Haga que este método Lea cualquier información de estado de juego que afecte a la representación, como las actualizaciones de la posición de objeto o fotogramas de animación, además de los datos de juego globales, como los niveles claros o los cambios en la física del juego. Estas entradas se usan para actualizar los datos de objetos y los búferes de constantes por fotograma.
-   **Render**: suele llamarse desde la parte del programa que administra el bucle del juego. en este caso, se llama desde la clase **principal** . Este método crea la canalización de gráficos: enlaza sombreadores, enlaza búferes y recursos a las fases del sombreador e invoca el dibujo del marco actual.

Estos métodos comprenden el cuerpo de los comportamientos para representar una escena con Direct3D mediante los recursos. Si extiende este ejemplo con una nueva clase de representación, declárelo en la clase de proyecto principal. Por lo tanto:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

se transforma en:

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

De nuevo, tenga en cuenta que en este ejemplo se da por supuesto que los métodos tienen las mismas firmas en la implementación. Si las firmas han cambiado, revise el bucle **principal** y realice los cambios en consecuencia.

Echemos un vistazo a los métodos de representación de escenas con más detalle.

## <a name="create-device-dependent-resources"></a>Crear recursos dependientes del dispositivo

**CreateDeviceDependentResources** consolida todas las operaciones para inicializar la escena y sus recursos mediante llamadas a [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) . Este método supone que el dispositivo Direct3D se acaba de inicializar (o se ha creado de forma recreada) para una escena. Vuelve a crear o recarga todos los recursos de gráficos específicos de la escena, como los sombreadores de vértices y píxeles, los búferes de vértices y de índices de los objetos, y cualquier otro recurso (por ejemplo, como texturas y sus vistas correspondientes).

Este es el código de ejemplo de **CreateDeviceDependentResources**:


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



Cada vez que carga recursos desde el disco (recursos como objetos de sombreador compilados (CSO o. CSO) o texturas, lo hace de forma asincrónica. Esto le permite mantener otro trabajo trabajando al mismo tiempo (como otras tareas de configuración) y, dado que el bucle principal no está bloqueado, puede seguir mostrando algo visualmente interesante para el usuario (por ejemplo, una animación de carga para el juego). En este ejemplo se usa la API Concurrency:: Tasks que está disponible a partir de Windows 8. Tenga en cuenta la sintaxis lambda que se usa para encapsular tareas de carga asincrónica. Estas expresiones lambda representan las funciones llamadas fuera de subproceso, por lo que se captura explícitamente un puntero al objeto de clase actual (**this**).

A continuación se muestra un ejemplo de cómo se puede cargar el código de bytes del sombreador:


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



A continuación se muestra un ejemplo de cómo crear búferes de vértices y de índices:


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



En este ejemplo no se carga ninguna malla ni texturas. Debe crear los métodos para cargar los tipos de malla y textura específicos del juego y llamarlos de forma asincrónica.

Rellene los valores iniciales de los búferes de constantes por escena aquí también. Entre los ejemplos de búfer de constantes por escena se incluyen las luces fijas u otros elementos y datos de la escena estática.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementar el método CreateWindowSizeDependentResources

Se llama a los métodos **CreateWindowSizeDependentResources** cada vez que cambia el tamaño de la ventana, la orientación o la resolución.

Los recursos de tamaño de ventana se actualizan de la siguiente manera: el procedimiento de mensajes estáticos obtiene uno de varios posibles eventos que indican un cambio en el estado de la ventana. A continuación, el bucle principal se informa del evento y llama a **CreateWindowSizeDependentResources** en la instancia de la clase principal, que luego llama a la implementación de **CreateWindowSizeDependentResources** en la clase de representador de la escena.

El trabajo principal de este método es asegurarse de que los objetos visuales no se confunden o no son válidos debido a un cambio en las propiedades de la ventana. En este ejemplo, se actualizan las matrices del proyecto con un nuevo campo de vista (campo de campo) para la ventana cuyo tamaño se ha cambiado o se ha reorientado.

Ya hemos visto el código para crear recursos de ventana en **DeviceResources** , que era la cadena de intercambio (con el búfer de reserva) y la vista de destino de representación. Este es el modo en que el representador crea transformaciones dependientes de la relación de aspecto:


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



Si la escena tiene un diseño específico de componentes que depende de la relación de aspecto, es el lugar donde reorganizarlos para que coincidan con la relación de aspecto. Puede que también desee cambiar la configuración del comportamiento posterior al procesamiento aquí.

## <a name="implement-the-update-method"></a>Implementar el método Update

Se llama al método **Update** una vez por cada bucle de juego; en este ejemplo, se llama mediante el método de la clase principal con el mismo nombre. Tiene un propósito sencillo: actualizar la geometría de la escena y el estado del juego en función de la cantidad de tiempo transcurrido (o de los pasos de tiempo transcurridos) desde el fotograma anterior. En este ejemplo, simplemente giramos el cubo una vez por fotograma. En una escena de juego real, este método contiene mucho más código para comprobar el estado del juego, actualizar los búferes de constantes de cada fotograma (u otros dinámicos), los búferes de geometría y otros recursos en memoria en consecuencia. Dado que la comunicación entre la CPU y la GPU incurre en una sobrecarga, asegúrese de que solo se actualizan los búferes que han cambiado desde el último fotograma: los búferes de constantes se pueden agrupar, o dividir, según sea necesario para que sea más eficaz.


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



En este caso, **girar** actualiza el búfer de constantes con una nueva matriz de transformación para el cubo. La matriz se multiplicará por vértice durante la etapa del sombreador de vértices. Dado que se llama a este método con cada fotograma, es un buen lugar para agregar métodos que actualicen los búferes de constantes y vértices dinámicos, o para realizar otras operaciones que preparen los objetos de la escena para su transformación por la canalización de gráficos.

## <a name="implement-the-render-method"></a>Implementar el método Render

Se llama a este método una vez por cada bucle de juego después de llamar a **Update**. Al igual que la **actualización**, el método **Render** también se llama desde la clase principal. Este es el método en el que la canalización de gráficos se construye y procesa para el marco mediante métodos en la instancia de [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) . Esto culmina en una llamada final a [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). Es importante comprender que esta llamada (u otras **\* *llamadas de Draw _ similares definidas en _* ID3D11DeviceContext**) ejecutan realmente la canalización. En concreto, esto se produce cuando Direct3D se comunica con la GPU para establecer el estado del dibujo, ejecuta cada fase de canalización y escribe los resultados de píxeles en el recurso de búfer de destino de representación para su presentación en la cadena de intercambio. Dado que la comunicación entre la CPU y la GPU incurre en una sobrecarga, combine varias llamadas a Draw en una sola si es posible, especialmente si la escena tiene muchos objetos representados.


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



Se recomienda establecer las distintas fases de canalización de gráficos en el contexto en orden. Normalmente, el orden es:

-   Actualice los recursos de búfer constantes con nuevos datos según sea necesario (mediante la **actualización** de datos).
-   Ensamblado de entrada (IA): aquí es donde se adjuntan los búferes de vértices y de índices que definen la geometría de la escena. Debe adjuntar cada vértice y búfer de índice para cada objeto de la escena. Dado que este ejemplo solo tiene el cubo, es bastante sencillo.
-   Sombreador de vértices (VS): Adjunte cualquier sombreador de vértices que transforme los datos en los búferes de vértices y adjunte búferes de constantes para el sombreador de vértices.
-   Sombreador de píxeles (PS): Conecte los sombreadores de píxeles que realizarán operaciones por píxel en la escena rasterizada y conecte los recursos de dispositivo para el sombreador de píxeles (búferes de constantes, texturas, etc.).
-   Fusión de salida (OM): esta es la fase en la que se combinan los píxeles, una vez finalizados los sombreadores. Esta es una excepción a la regla, ya que se adjuntan las galerías de símbolos de profundidad y los destinos de representación antes de establecer cualquiera de las otras fases. Puede tener varias galerías de símbolos y destinos si tiene sombreadores de vértices y píxeles adicionales que generan texturas como mapas de sombras, mapas de alto u otras técnicas de muestreo; en este caso, cada paso del dibujo necesitará los destinos adecuados establecidos antes de llamar a una función Draw.

Después, en la sección final ([trabajar con sombreadores y recursos del sombreador](work-with-shaders-and-shader-resources.md)), veremos los sombreadores y veremos cómo los ejecuta Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Siguiente**
</dt> <dt>

[Trabajar con sombreadores y recursos del sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
