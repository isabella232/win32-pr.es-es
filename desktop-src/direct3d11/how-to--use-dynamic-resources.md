---
title: Uso de recursos dinámicos
description: Los recursos dinámicos se crean y usan cuando la aplicación necesita cambiar los datos de esos recursos. Puede crear texturas y búferes para el uso dinámico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d85933490d1e3bbbd09cc83720651c4fd634012f8e5aa70562396e87c096ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633105"
---
# <a name="how-to-use-dynamic-resources"></a>Uso de recursos dinámicos

**API importantes**

-   [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**USO DE D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Los recursos dinámicos se crean y usan cuando la aplicación necesita cambiar los datos de esos recursos. Puede crear texturas y búferes para el uso dinámico.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Cómo: Crear una textura](overviews-direct3d-11-resources-textures-create.md)
-   [Cómo: Inicializar una textura mediante programación](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Cómo: Crear un búfer constante](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Prerrequisitos

Suponemos que estás familiarizado con C++. También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.

## <a name="instructions"></a>Instructions

### <a name="step-1-specify-dynamic-usage"></a>Paso 1: Especificar el uso dinámico

Si desea que la aplicación pueda realizar cambios en los recursos, debe especificar esos recursos como dinámicos y grabables al crearlos.

**Para especificar el uso dinámico**

1.  Especifique el uso de recursos como dinámico. Por ejemplo, especifique el valor [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) en el miembro **Usage** de [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para un vértice o búfer constante y especifique el valor **D3D11 \_ USAGE \_ DYNAMIC** en el miembro **Usage** de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para una textura 2D.
2.  Especifique el recurso como grabable. Por ejemplo, especifique el valor [**D3D11 \_ CPU \_ ACCESS \_ WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) en el miembro **CPUAccessFlags** de [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) o [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).
3.  Pase la descripción del recurso a la función de creación. Por ejemplo, pase la dirección de [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) y pase la dirección de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) a [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Este es un ejemplo de creación de un búfer de vértice dinámico:


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a>Paso 2: Cambio de un recurso dinámico

Si especificó un recurso como dinámico y grabable al crearlo, puede realizar más adelante cambios en ese recurso.

**Para cambiar los datos de un recurso dinámico**

1.  Configure los nuevos datos para el recurso. Declare una variable [**de tipo D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inicialíctela en cero. Usará esta variable para cambiar el recurso.
2.  Deshabilite el acceso de la unidad de procesamiento gráfico (GPU) a los datos que desea cambiar y obtenga un puntero a la memoria que contiene los datos. Para obtener este puntero, pase [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) al *parámetro MapType* cuando llame a [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). Establezca este puntero en la dirección de la variable [**D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) del paso anterior.
3.  Escriba los nuevos datos en la memoria.
4.  Llame [**a ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) para volver a poder acceder mediante GPU a los datos cuando haya terminado de escribir los nuevos datos.

Este es un ejemplo de cómo cambiar un búfer de vértice dinámico:


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a>Comentarios

### <a name="using-dynamic-textures"></a>Uso de texturas dinámicas

Se recomienda crear solo una textura dinámica por formato y posiblemente por tamaño. No se recomienda crear mapas mip dinámicos, cubos y volúmenes debido a la sobrecarga adicional en la asignación de cada nivel. Para los mapas mip, puede especificar [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) solo en el nivel superior. Todos los niveles se descartan mediante la asignación solo del nivel superior. Este comportamiento es el mismo para volúmenes y cubos. En el caso de los cubos, se asignan el nivel superior y la cara 0.

### <a name="using-dynamic-buffers"></a>Uso de búferes dinámicos

Cuando se llama a [**Map en**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) un búfer de vértice estático mientras la GPU usa el búfer, se obtiene una reducción significativa del rendimiento. En esta situación, **Map** debe esperar hasta que la GPU termine de leer los datos de vértice o índice del búfer antes de que **Map** pueda volver a la aplicación que realiza la llamada, lo que provoca un retraso significativo. Llamar **a Map** y, a continuación, representar desde un búfer estático varias veces por fotograma también impide que la GPU almacena en búfer los comandos de representación porque debe finalizar los comandos antes de devolver el puntero de mapa. Sin los comandos almacenados en búfer, la GPU permanece inactiva hasta que la aplicación termina de rellenar el búfer de vértices o el búfer de índice y emite un comando de representación.

Idealmente, los datos de vértice o índice nunca cambiarían, pero esto no siempre es posible. Hay muchas situaciones en las que la aplicación necesita cambiar los datos de vértice o índice de cada fotograma, quizás incluso varias veces por fotograma. En estas situaciones, se recomienda crear el vértice o búfer de índice con [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Esta marca de uso hace que el tiempo de ejecución se optimice para las operaciones de asignación frecuentes. **D3D11 \_ USAGE \_ DYNAMIC solo** es útil cuando el búfer se asigna con frecuencia; Si los datos deben permanecer constantes, coloque los datos en un vértice estático o búfer de índice.

Para recibir una mejora del rendimiento al usar búferes de vértice dinámicos, la aplicación debe llamar a [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) con los valores map [**D3D11 \_ adecuados.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que la aplicación no necesita mantener los datos antiguos de vértice o índice en el búfer. Si la GPU sigue usando el búfer al llamar a **Map** con **D3D11 \_ MAP WRITE \_ \_ DISCARD**, el tiempo de ejecución devuelve un puntero a una nueva región de memoria en lugar de a los datos antiguos del búfer. Esto permite que la GPU siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer. No se requiere ninguna administración de memoria adicional en la aplicación; El búfer antiguo se reutiliza o destruye automáticamente cuando la GPU termina con él.

> [!Note]  
> Al asignar un búfer con [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), el tiempo de ejecución siempre descarta todo el búfer. No se puede conservar la información en áreas no asignados del búfer especificando un desplazamiento distinto de cero o un campo de tamaño limitado.

 

Hay casos en los que la cantidad de datos que la aplicación necesita almacenar por mapa es pequeña, como agregar cuatro vértices para representar un sprite. [**D3D11 \_ MAP \_ WRITE \_ NO \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que la aplicación no sobrescribirá los datos que ya están en uso en el búfer dinámico. La [**llamada a**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) Map devolverá un puntero a los datos antiguos, lo que permitirá a la aplicación agregar nuevos datos en regiones no utilizadas del vértice o búfer de índice. La aplicación no debe modificar los vértices ni los índices que se usan en una operación de dibujo, ya que es posible que todavía estén en uso por la GPU. Se recomienda que la aplicación use [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) después de que el búfer dinámico esté lleno para recibir una nueva región de memoria, que descarta los datos antiguos del vértice o del índice una vez finalizada la GPU.

El mecanismo de consulta asincrónica es útil para determinar si los vértices siguen siendo usados por la GPU. Emita una consulta de tipo [**D3D11 \_ QUERY \_ EVENT después**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) de la última llamada a draw que usa los vértices. Los vértices ya no se usan cuando [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) devuelve S \_ OK. Al asignar un búfer con [**D3D11 \_ MAP \_ WRITE \_ DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o ningún valor de mapa, siempre se garantiza que los vértices se sincronizan correctamente con la GPU. Sin embargo, al asignar sin valores de mapa, incurrirá en la penalización de rendimiento descrita anteriormente.

> [!Note]  
> El entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8, permite asignar búferes constantes dinámicos y vistas de recursos de sombreador (SRV) de búferes dinámicos con [**D3D11 \_ MAP WRITE NO \_ \_ \_ OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). Direct3D 11 y los tiempos de ejecución anteriores limitaban la asignación de actualización parcial sin sobrescritura a búferes de vértices o índices. Para determinar si un dispositivo Direct3D admite estas características, llame a [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** rellena los miembros de una estructura [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) con las características del dispositivo. Los miembros pertinentes aquí **son MapNoOverwriteOnDynamicConstantBuffer** y **MapNoOverwriteOnDynamicBufferSRV.**

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




