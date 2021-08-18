---
title: Cómo crear un búfer de vértices
description: En este tema se muestra cómo inicializar un búfer de vértice estático, es decir, un búfer de vértices que no cambia.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- búfer de vértices, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f919646dfd4e8f714b925606f342db586ff2b8f09690c58698b7dab2635159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496907"
---
# <a name="how-to-create-a-vertex-buffer"></a>Cómo: Crear un búfer de vértices

[Los búferes de vértice](overviews-direct3d-11-resources-buffers-intro.md) contienen datos por vértice. En este tema se muestra cómo inicializar un búfer de [vértice estático,](overviews-direct3d-11-resources-buffers-intro.md)es decir, un búfer de vértices que no cambia. Para obtener ayuda para inicializar un búfer no estático, consulte la [sección](#remarks) comentarios.

**Para inicializar un búfer de vértice estático**

1.  Defina una estructura que describa un vértice. Por ejemplo, si los datos de vértice contienen datos de posición y datos de color, la estructura tendría un vector que describe la posición y otro que describe el color.
2.  Asigne memoria (mediante malloc o new) para la estructura que definió en el paso uno. Rellene este búfer con los datos de vértice reales que describen la geometría.
3.  Cree una descripción del búfer rellenando una [**estructura \_ \_ DESC de BÚFER D3D11.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Pase la marca D3D11 BIND VERTEX BUFFER al miembro BindFlags y pase el tamaño de la estructura del paso uno al \_ \_ miembro \_ **ByteWidth.** 
4.  Cree una descripción de datos de subrecursos rellenando una estructura [**\_ SUBRESOURCE \_ DATA de D3D11.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) El **miembro pSysMem** de la estructura [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) debe apuntar directamente a los datos de recursos creados en el paso dos.
5.  Llame a [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) al pasar la estructura [**D3D11 \_ BUFFER \_ DESC,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) la estructura [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la [**interfaz ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se inicializará.

En el ejemplo de código siguiente se muestra cómo crear un búfer de vértices. En este ejemplo se supone que **g \_ pd3dDevice** es un [**objeto ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido.


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a>Comentarios

Estas son algunas maneras de inicializar un búfer de vértices que cambia con el tiempo.

1.  Cree un segundo búfer con [**D3D11 \_ USAGE \_ STAGING;**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)rellene el segundo búfer con [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap;**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) para copiar desde el búfer de almacenamiento provisional al búfer predeterminado.
2.  Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para copiar datos de la memoria.
3.  Cree un búfer con [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)y llénelo con [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (con las marcas Discard y NoOverwrite adecuadamente).

\#1 y \# 2 son útiles para el contenido que cambia menos de una vez por fotograma. En general, las lecturas de GPU serán rápidas y las actualizaciones de CPU serán más lentas.

\#3 es útil para el contenido que cambia más de una vez por fotograma. En general, las lecturas de GPU serán más lentas, pero las actualizaciones de CPU serán más rápidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




