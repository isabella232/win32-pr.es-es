---
title: Cómo crear un búfer de vértices
description: En este tema se muestra cómo inicializar un búfer de vértices estático, es decir, un búfer de vértice que no cambia.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- búfer de vértices, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357301"
---
# <a name="how-to-create-a-vertex-buffer"></a>Cómo: crear un búfer de vértices

Los [búferes de vértices](overviews-direct3d-11-resources-buffers-intro.md) contienen datos por vértice. En este tema se muestra cómo inicializar un [búfer de vértices](overviews-direct3d-11-resources-buffers-intro.md)estático, es decir, un búfer de vértice que no cambia. Para obtener ayuda para inicializar un búfer no estático, consulte la sección [comentarios](#remarks) .

**Para inicializar un búfer de vértices estáticos**

1.  Defina una estructura que describa un vértice. Por ejemplo, si los datos de vértice contienen datos de posición y datos de color, la estructura tendría un vector que describa la posición y otro que describa el color.
2.  Asigne memoria (mediante malloc o New) para la estructura que definió en el paso uno. Rellene este búfer con los datos de vértice reales que describen su geometría.
3.  Cree una descripción de búfer rellenando una estructura [**\_ \_ DESC de búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Pase la \_ marca de búfer de vértices BIND de D3D11 \_ \_ al miembro **BindFlags** y pase el tamaño de la estructura del paso uno al miembro **ByteWidth** .
4.  Cree una descripción de los datos de subrecurso rellenando una estructura de [**\_ \_ datos de subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . El miembro **pSysMem** de la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) debe apuntar directamente a los datos de recursos creados en el paso dos.
5.  Llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) mientras pasa la estructura de [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la estructura de [**\_ \_ datos del subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) y la dirección de un puntero a la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) que se va a inicializar.

En el ejemplo de código siguiente se muestra cómo crear un búfer de vértices. En este ejemplo se da por supuesto que **g \_ pd3dDevice** es un objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido.


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



## <a name="remarks"></a>Observaciones

A continuación se indican algunas maneras de inicializar un búfer de vértice que cambia con el tiempo.

1.  Cree un segundo búfer con [**el \_ \_ almacenamiento provisional del uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); rellene el segundo búfer con [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)desasignar; use [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) para copiar desde el búfer de almacenamiento provisional al búfer predeterminado.
2.  Use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para copiar datos de la memoria.
3.  Cree un búfer con el uso de D3D11 dinámico y rellénelo con [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar (mediante las marcas discard y NoOverwrite de [**\_ \_ forma**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)adecuada).

\#1 y \# 2 son útiles para el contenido que cambia menos de una vez por fotograma. En general, las lecturas de GPU serán rápidas y las actualizaciones de CPU serán más lentas.

\#3 es útil para el contenido que cambia más de una vez por fotograma. En general, las lecturas de GPU serán más lentas, pero las actualizaciones de la CPU serán más rápidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




