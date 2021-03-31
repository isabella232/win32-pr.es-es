---
description: La creación de búferes requiere la definición de los datos que almacenará el búfer, el suministro de datos de inicialización y la configuración de las marcas de uso y enlace apropiadas. Para crear texturas, vea crear recursos de textura (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Crear recursos de búfer (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807537"
---
# <a name="creating-buffer-resources-direct3d-10"></a>Crear recursos de búfer (Direct3D 10)

La creación de búferes requiere la definición de los datos que almacenará el búfer, el suministro de datos de inicialización y la configuración de las marcas de uso y enlace apropiadas. Para crear texturas, vea [crear recursos de textura (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).

-   [Crear un búfer de vértices](#create-a-vertex-buffer)
    -   [Crear una descripción de búfer](#create-a-buffer-description)
    -   [Crear los datos de inicialización del búfer](#create-the-initialization-data-for-the-buffer)
    -   [Crear el búfer](#create-the-buffer)
-   [Crear un búfer de índice](#create-an-index-buffer)
-   [Crear un búfer de constantes](#create-a-constant-buffer)
-   [Temas relacionados](#related-topics)

## <a name="create-a-vertex-buffer"></a>Crear un búfer de vértices

Los pasos para crear un [búfer de vértice](d3d10-graphics-programming-guide-resources-types.md) son los siguientes.

-   [Crear una descripción de búfer](#create-a-buffer-description)
-   [Crear los datos de inicialización del búfer](#create-the-initialization-data-for-the-buffer)
-   [Crear el búfer](#create-the-buffer)

### <a name="create-a-buffer-description"></a>Crear una descripción de búfer

Al crear un búfer de vértices, se usa una descripción de búfer (vea [**D3D10 \_ buffer \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) para definir cómo se organizan los datos en el búfer, cómo la canalización puede tener acceso al búfer y cómo se usará el búfer.

En el ejemplo siguiente se muestra cómo crear una descripción de búfer para un solo triángulo con vértices que contienen valores de posición y color.


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



En este ejemplo, la descripción del búfer se inicializa con casi todos los valores predeterminados para el [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), el [**acceso a la CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) y las [**marcas misceláneas**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag). Los demás valores son para el [**marcador de enlace**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) que identifica el recurso como solo un búfer de vértices y el tamaño del búfer.

Las marcas de acceso de uso y de CPU son importantes para el rendimiento. Estas dos marcas determinan con qué frecuencia se obtiene acceso a un recurso, el tipo de memoria en el que se puede cargar el recurso y el procesador que necesita para tener acceso al recurso. Uso predeterminado: este recurso no se actualizará con mucha frecuencia. Establecer el acceso a la CPU en 0 significa que la CPU no necesitará leer ni escribir el recurso. Tomadas en combinación, esto significa que el tiempo de ejecución puede cargar el recurso en la memoria de mayor rendimiento para la GPU, ya que el recurso no requiere acceso a la CPU.

Tal y como se espera, existe un equilibrio entre el mejor rendimiento y la accesibilidad en cualquier momento por cada procesador. Por ejemplo, el uso predeterminado sin acceso a la CPU significa que el recurso se puede poner a disposición de la GPU exclusivamente. Esto podría incluir la carga del recurso en la memoria no accesible directamente por la CPU. El recurso solo se puede modificar con [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).

### <a name="create-the-initialization-data-for-the-buffer"></a>Crear los datos de inicialización del búfer

Un búfer es simplemente una colección de elementos y se coloca como una matriz 1D. Como resultado, el paso de la memoria del sistema y el intervalo de la memoria del sistema son los mismos; tamaño de la declaración de datos de vértice. Una aplicación puede proporcionar datos de inicialización cuando se crea un búfer mediante una [**Descripción de subrecurso**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), que contiene un puntero a los datos de recursos reales y contiene información sobre el tamaño y el diseño de los datos.

Cualquier búfer creado con uso inmutable (consulte [**D3D10 \_ Usage \_ inmutable**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) debe inicializarse en el momento de la creación. Los búferes que usan cualquiera de las otras marcas de uso se pueden actualizar después de la inicialización con [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)y [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), o mediante el acceso a su memoria subyacente mediante el método [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .

### <a name="create-the-buffer"></a>Crear el búfer

Con la descripción del búfer y los datos de inicialización (que es opcional), llame a [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) para crear un búfer de vértice. El siguiente fragmento de código muestra cómo crear un búfer de vértices a partir de una matriz de datos de vértice declarada por la aplicación.


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>Crear un búfer de índice

Crear un búfer de índice es muy similar a crear un búfer de vértices. con dos diferencias. Un búfer de índice solo contiene datos de 16 o 32 bits (en lugar de la amplia gama de formatos disponibles para un búfer de vértices. Un búfer de índice también requiere una marca de enlace de búfer de índice.

En el ejemplo siguiente se muestra cómo crear un búfer de índice a partir de una matriz de datos de índice.


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>Crear un búfer de constantes

Direct3D 10 introduce un búfer de constantes. Un búfer de constantes o un búfer de constantes de sombreador es un búfer que contiene constantes de sombreador. Este es un ejemplo de cómo crear un búfer de constantes, tomado del [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



Tenga en cuenta que cuando se usa la interfaz de [**interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , el proceso de creación, enlace y concesión de un búfer de constantes se controla mediante la instancia de la **interfaz ID3D10Effect** . En ese caso, solo se nescesary para obtener la variable del efecto con uno de los métodos GetVariable como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) y actualizar la variable con uno de los métodos SetVariable como [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Para obtener un ejemplo del uso de la **interfaz ID3D10Effect** para administrar un búfer de constantes [, vea Tutorial 7: asignación de texturas y búferes de constantes](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



