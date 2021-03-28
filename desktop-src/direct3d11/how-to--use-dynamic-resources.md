---
title: Cómo usar recursos dinámicos
description: Los recursos dinámicos se crean y se usan cuando la aplicación necesita cambiar los datos de esos recursos. Puede crear texturas y búferes para el uso dinámico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268383"
---
# <a name="how-to-use-dynamic-resources"></a>Cómo: usar recursos dinámicos

**API importantes**

-   [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [**ID3D11DeviceContext:: desasignar**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [**Uso de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

Los recursos dinámicos se crean y se usan cuando la aplicación necesita cambiar los datos de esos recursos. Puede crear texturas y búferes para el uso dinámico.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Cómo: crear una textura](overviews-direct3d-11-resources-textures-create.md)
-   [Cómo: inicializar una textura mediante programación](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [Cómo: crear un búfer de constantes](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a>Requisitos previos

Suponemos que estás familiarizado con C++. También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-specify-dynamic-usage"></a>Paso 1: especificar el uso dinámico

Si desea que la aplicación pueda realizar cambios en los recursos, debe especificar esos recursos como dinámicos y que se pueden escribir al crearlos.

**Para especificar el uso dinámico**

1.  Especifique el uso de recursos como dinámico. Por ejemplo, especifique el [**valor \_ \_ dinámico D3D11 Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) en el miembro **Usage** de [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para un búfer de vértice o de constante y especifique el valor **\_ \_ dinámico de uso de D3D11** en el miembro **Usage** de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para una textura 2D.
2.  Especifique el recurso como grabable. Por ejemplo, especifique el valor de [**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) en el miembro **CPUAccessFlags** de [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) o [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).
3.  Pase la descripción del recurso a la función de creación. Por ejemplo, pase la dirección de [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) y pase la dirección de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).

Este es un ejemplo de cómo crear un búfer de vértice dinámico:


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



### <a name="step-2-change-a-dynamic-resource"></a>Paso 2: cambiar un recurso dinámico

Si especificó un recurso como dinámico y grabable cuando lo creó, puede realizar cambios más adelante en ese recurso.

**Para cambiar los datos de un recurso dinámico**

1.  Configure los nuevos datos para el recurso. Declare una variable de tipo [**\_ \_ subrecurso D3D11 asignada**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inicialícela en cero. Usará esta variable para cambiar el recurso.
2.  Deshabilite el acceso de la unidad de procesamiento de gráficos (GPU) a los datos que desea cambiar y obtenga un puntero a la memoria que contiene los datos. Para obtener este puntero, pase [**el \_ \_ \_ descartado de escritura de asignación de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) al parámetro *mapType* cuando llame a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). Establezca este puntero en la dirección de la variable de [**\_ \_ subrecurso asignada D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) del paso anterior.
3.  Escriba los nuevos datos en la memoria.
4.  Llame a [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) unwith para volver a habilitar el acceso de GPU a los datos cuando haya terminado de escribir los datos nuevos.

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



## <a name="remarks"></a>Observaciones

### <a name="using-dynamic-textures"></a>Usar texturas dinámicas

Se recomienda crear solo una textura dinámica por formato y, posiblemente, por tamaño. No se recomienda crear mapas de MIP, cubos y volúmenes dinámicos debido a la sobrecarga adicional en la asignación de todos los niveles. En el caso de los mapas MIP, puede especificar el [**\_ \_ \_ descartado de escritura de mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) solo en el nivel superior. Todos los niveles se descartan asignando solo el nivel superior. Este comportamiento es el mismo para los volúmenes y los cubos. En el caso de los cubos, se asignan el nivel superior y la esfera 0.

### <a name="using-dynamic-buffers"></a>Usar búferes dinámicos

Cuando se llama a [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) en un búfer de vértices estático mientras la GPU usa el búfer, se obtiene una penalización significativa del rendimiento. En esta situación, la **asignación** debe esperar hasta que la GPU termine de leer los datos de vértices o índices del búfer antes de que la **asignación** pueda volver a la aplicación que realiza la llamada, lo que produce un retraso significativo. La llamada a la **asignación** y, a continuación, la representación de un búfer estático varias veces por fotograma también impide que la GPU almacene en búfer comandos de representación porque debe finalizar los comandos antes de devolver el puntero de mapa. Sin comandos almacenados en búfer, la GPU permanece inactiva hasta que la aplicación termina de llenar el búfer de vértices o el búfer de índice y emite un comando de representación.

Idealmente, los datos de vértices o índices nunca cambiarían, pero esto no siempre es posible. Hay muchas situaciones en las que la aplicación necesita cambiar los datos de vértices o índices en cada fotograma, quizás incluso varias veces por fotograma. En estas situaciones, se recomienda crear el búfer de vértice o de índice con [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). Esta marca de uso hace que el tiempo de ejecución se optimice para las operaciones de asignación frecuentes. **D3D11 \_ USAGE \_ Dynamic** solo es útil cuando el búfer se asigna con frecuencia; Si los datos van a permanecer constantes, coloque los datos en un vértice estático o en un búfer de índice.

Para obtener una mejora del rendimiento cuando se usan búferes de vértices dinámicos, la aplicación debe llamar a [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) con los valores de [**\_ asignación D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) adecuados. [**D3D11 \_ \_ \_ Descartar escritura de asignación**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que la aplicación no necesita mantener los datos de índice o vértice antiguos en el búfer. Si la GPU todavía usa el búfer al llamar a **map** con **D3D11 \_ map \_ Write \_ discard**, el tiempo de ejecución devuelve un puntero a una nueva región de memoria en lugar de los datos de búfer antiguos. Esto permite que la GPU siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer. No se requiere ninguna administración de memoria adicional en la aplicación; el búfer antiguo se reutiliza o se destruye automáticamente cuando la GPU finaliza con él.

> [!Note]  
> Cuando se asigna un búfer con [**el \_ \_ \_ descartado de escritura de asignación de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), el tiempo de ejecución siempre descarta todo el búfer. No se puede conservar la información en áreas sin asignar del búfer mediante la especificación de un campo de desplazamiento distinto de cero o de tamaño limitado.

 

Hay casos en los que la cantidad de datos que la aplicación necesita almacenar por asignación es pequeña, como agregar cuatro vértices para representar un Sprite. [**D3D11 \_ La \_ escritura de asignación \_ no \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) sobrescribir indica que la aplicación no sobrescribirá los datos que ya se estén usando en el búfer dinámico. La llamada de [**asignación**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) devolverá un puntero a los datos antiguos, lo que permitirá a la aplicación agregar nuevos datos en regiones no utilizadas del búfer de vértice o de índice. La aplicación no debe modificar los vértices ni los índices que se usan en una operación de dibujo, ya que es posible que la GPU siga utilizándolos. Se recomienda que la aplicación use [**\_ \_ \_ descartar escritura de asignación de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) después de que el búfer dinámico esté lleno para recibir una nueva región de memoria, que descarta los datos de vértice o de vértice antiguos una vez finalizada la GPU.

El mecanismo de consulta asincrónico es útil para determinar si la GPU todavía está usando los vértices. Emita una consulta de tipo [**\_ \_ evento de consulta D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) después de la última llamada a Draw que use los vértices. Los vértices ya no se usan cuando [**ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) devuelve S \_ correctos. Cuando asigne un búfer con los [**valores \_ \_ \_ descartados de escritura de mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o sin valores de asignación, siempre se garantiza que los vértices se sincronizan correctamente con la GPU. Sin embargo, cuando se asignan sin valores de mapa, se incurrirá en la penalización de rendimiento que se ha descrito anteriormente.

> [!Note]  
> El tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8, habilita la asignación de búferes de constantes dinámicos y vistas de recursos de sombreador (SRVs) de búferes dinámicos con D3D11 no se sobrescribe la [**\_ \_ escritura de \_ \_ asignación**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map). En los tiempos de ejecución de Direct3D 11 y versiones anteriores, la asignación de actualización parcial no se sobrescribe en los búferes de vértices o índices. Para determinar si un dispositivo Direct3D admite estas características, llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ las opciones D3D11 de la característica D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature). **CheckFeatureSupport** rellena los miembros de una estructura de [**\_ \_ \_ \_ Opciones D3D11 de datos de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) con las características del dispositivo. Los miembros pertinentes aquí son **MapNoOverwriteOnDynamicConstantBuffer** y **MapNoOverwriteOnDynamicBufferSRV**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




