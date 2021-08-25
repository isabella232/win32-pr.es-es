---
title: Introducción a los búferes en Direct3D 11
description: Un recurso de búfer es una colección de datos totalmente con tipo agrupados en elementos.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- búfer constante, ¿qué es ?
- búfer de vértices, ¿qué es ?
- búfer de índice, ¿qué es ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51f7b0dbd60264b77f9d9dc83f39cbb4325464079d537c3ee741a942d26a139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752025"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Introducción a los búferes en Direct3D 11

Un recurso de búfer es una colección de datos totalmente con tipo agrupados en elementos. Puede usar búferes para almacenar una amplia variedad de datos, incluidos vectores de posición, vectores normales, coordenadas de textura en un búfer de vértices, índices en un búfer de índice o estado de dispositivo. Un elemento de búfer se forma de 1 a 4 componentes. Los elementos de búfer pueden incluir valores de datos empaquetados (como valores de superficie R8G8B8A8), enteros de 8 bits únicos o cuatro valores de punto flotante de 32 bits.

Un búfer se crea como un recurso no estructurado. Dado que no está estructurado, un búfer no puede contener ningún nivel de mapa mip, no se puede filtrar cuando se lee y no se puede multimuestrear.

## <a name="buffer-types"></a>Tipos de búfer

Estos son los tipos de recursos de búfer admitidos por Direct3D 11. Todos los tipos de búfer se encapsulan mediante la [**interfaz ID3D11Buffer.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)

-   [Búfer de vértices](#vertex-buffer)
-   [Búfer de índice](#index-buffer)
-   [Búfer constante](#constant-buffer)

### <a name="vertex-buffer"></a>Búfer de vértices

Un búfer de vértices contiene los datos de vértice usados para definir la geometría. Los datos de vértice incluyen coordenadas de posición, datos de color, datos de coordenadas de textura, datos normales, y así sucesivamente.

El ejemplo más sencillo de un búfer de vértices es aquel que solo contiene datos de posición. Se puede visualizar como en la ilustración siguiente.

![ilustración de un búfer de vértices que contiene datos de posición](images/d3d10-resources-single-element-vb2.png)

Más a menudo, un búfer de vértices contiene todos los datos necesarios para especificar completamente los vértices 3D. Un ejemplo de esto podría ser un búfer de vértices que contiene coordenadas de posición por vértice, normal y de textura. Normalmente, estos datos se organizan como conjuntos de elementos por vértice, como se muestra en la ilustración siguiente.

![ilustración de un búfer de vértices que contiene datos de posición, normal y textura](images/d3d10-vertex-buffer-element.png)

Este búfer de vértice contiene datos por vértice; cada vértice almacena tres elementos (coordenadas de posición, normal y de textura). La posición y la normal se especifican normalmente mediante tres flotantes de 32 bits (DXGI FORMAT R32G32B32 FLOAT) y las coordenadas de textura mediante dos flotantes de \_ \_ 32 bits \_ (DXGI \_ FORMAT \_ R32G32 \_ FLOAT).

Para acceder a los datos desde un búfer de vértices, debe saber a qué vértice se debe acceder, además de los siguientes parámetros de búfer adicionales:

-   Desplazamiento: el número de bytes desde el inicio del búfer hasta los datos del primer vértice. Puede especificar el desplazamiento mediante el [**método ID3D11DeviceContext::IASetVertexBuffers.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)
-   BaseVertexLocation: el número de bytes desde el desplazamiento hasta el primer vértice utilizado por la llamada a draw adecuada.

Antes de crear un búfer de vértices, debe definir su diseño mediante la creación de una [**interfaz ID3D11InputLayout;**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) Para ello, llame al [**método ID3D11Device::CreateInputLayout.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) Una vez creado el objeto input-layout, puede enlazarlo a la fase input-assembler llamando a [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).

Para crear un búfer de vértices, llame [**a ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="index-buffer"></a>Búfer de índice

Los búferes de índice contienen desplazamientos de enteros en búferes de vértices y se usan para representar primitivas de forma más eficaz. Un búfer de índice contiene un conjunto secuencial de índices de 16 o 32 bits; cada índice se usa para identificar un vértice en un búfer de vértices. Un búfer de índice se puede visualizar como en la ilustración siguiente.

![ilustración de un búfer de índice](images/d3d10-index-buffer.png)

Los índices secuenciales almacenados en un búfer de índice se encuentran con los parámetros siguientes:

-   Offset: el número de bytes de la dirección base del búfer de índice. El desplazamiento se proporciona al método [**ID3D11DeviceContext::IASetIndexBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)
-   StartIndexLocation: especifica el primer elemento de búfer de índice de la dirección base y el desplazamiento proporcionado en [**IASetIndexBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) La ubicación de inicio se proporciona al método [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) o [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) y representa el primer índice que se va a representar.
-   IndexCount: el número de índices que se representará. El número se proporciona al método [**DrawIndexed.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)

Start of Index Buffer = Index Buffer Base Address + Offset (bytes) + StartIndexLocation \* ElementSize (bytes);

En este cálculo, ElementSize es el tamaño de cada elemento de búfer de índice, que es de dos o cuatro bytes.

Para crear un búfer de índice, llame [**a ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="constant-buffer"></a>Búfer constante

Un búfer constante permite proporcionar eficazmente datos de constantes de sombreador a la canalización. Puede usar un búfer constante para almacenar los resultados de la fase stream-output. Conceptualmente, un búfer constante se parece a un búfer de vértice de un solo elemento, como se muestra en la ilustración siguiente.

![ilustración de un búfer de constante de sombreador](images/d3d10-shader-resource-buffer.png)

Cada elemento almacena una constante de componente de 1 a 4, determinada por el formato de los datos almacenados. Para crear un búfer constante de sombreador, llame a [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) y especifique el miembro BIND CONSTANT BUFFER de **D3D11 \_ \_ \_** del tipo enumerado BIND FLAG de [**D3D11. \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

Un búfer constante solo puede usar una marca de enlace única **(D3D11 \_ BIND \_ CONSTANT \_ BUFFER),** que no se puede combinar con ninguna otra marca de enlace. Para enlazar un búfer constante de sombreador a la canalización, llame a uno de los métodos siguientes: [**ID3D11DeviceContext::GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**ID3D11DeviceContext::P SSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)o [**ID3D11DeviceContext::VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Para leer un búfer constante de sombreador desde un sombreador, use una función de carga HLSL (por ejemplo, [**Cargar**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)). Cada fase del sombreador permite hasta 15 búferes de constante de sombreador; cada búfer puede contener hasta 4096 constantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 