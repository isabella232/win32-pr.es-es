---
title: Introducción a los búferes en Direct3D 11
description: Un recurso de búfer es una colección de datos totalmente tipados agrupados en elementos.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- búfer de constantes, qué es
- búfer de vértices, qué es
- búfer de índice, qué es
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241ade0721ae87b1371586bc901ee18f8975b53f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359079"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Introducción a los búferes en Direct3D 11

Un recurso de búfer es una colección de datos totalmente tipados agrupados en elementos. Puede usar los búferes para almacenar una gran variedad de datos, incluidos los vectores de posición, los vectores normales, las coordenadas de textura en un búfer de vértices, los índices en un búfer de índice o el estado del dispositivo. Un elemento de búfer se compone de 1 a 4 componentes. Los elementos de búfer pueden incluir valores de datos empaquetados (como valores de la superficie R8G8B8A8), enteros de 8 bits únicos o valores de punto flotante de 4 32 bits.

Un búfer se crea como un recurso no estructurado. Dado que no está estructurado, un búfer no puede contener ningún nivel de mipmap, no se puede filtrar cuando se lee y no puede ser de muestreo multimuestreado.

## <a name="buffer-types"></a>Tipos de búfer

A continuación se muestran los tipos de recursos de búfer que admite Direct3D 11. Todos los tipos de búfer están encapsulados por la interfaz [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) .

-   [Búfer de vértices](#vertex-buffer)
-   [Búfer de índice](#index-buffer)
-   [Búfer de constantes](#constant-buffer)

### <a name="vertex-buffer"></a>Búfer de vértices

Un búfer de vértice contiene los datos de vértices que se usan para definir la geometría. Los datos de vértice incluyen coordenadas de posición, datos de color, datos de coordenadas de textura, datos normales, etc.

El ejemplo más simple de un búfer de vértice es aquél que solo contiene datos de posición. Se puede visualizar como la siguiente ilustración.

![Ilustración de un búfer de vértices que contiene datos de posición](images/d3d10-resources-single-element-vb2.png)

Con mayor frecuencia, un búfer de vértice contiene todos los datos necesarios para especificar por completo los vértices 3D. Un ejemplo de esto podría ser un búfer de vértices que contenga la posición por vértice, las coordenadas normales y de textura. Normalmente, estos datos se organizan como conjuntos de elementos por vértice, tal como se muestra en la siguiente ilustración.

![Ilustración de un búfer de vértices que contiene datos de posición, normal y de textura](images/d3d10-vertex-buffer-element.png)

Este búfer de vértice contiene datos por vértices; cada vértice almacena tres elementos (coordenadas de posición, normal y de textura). La posición y la normal se especifican normalmente con los flotantes de 3 32 bits (formato de DXGI \_ \_ R32G32B32 \_ float) y las coordenadas de textura con los flotantes de 2 32 bits (dxgi \_ format \_ R32G32 \_ float).

Para tener acceso a los datos de un búfer de vértice, debe saber a qué vértice acceder, además de los siguientes parámetros adicionales de búfer:

-   Offset: el número de bytes desde el inicio del búfer hasta los datos del primer vértice. Puede especificar el desplazamiento mediante el método [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) .
-   BaseVertexLocation: el número de bytes desde el desplazamiento hasta el primer vértice usado por la llamada a Draw adecuada.

Antes de crear un búfer de vértices, debe definir su diseño mediante la creación de una interfaz [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) . Esto se hace llamando al método [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) . Una vez creado el objeto de diseño de entrada, puede enlazarlo a la fase del ensamblador de entrada llamando a [**ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).

Para crear un búfer de vértices, llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="index-buffer"></a>Búfer de índice

Los búferes de índice contienen desplazamientos enteros en búferes de vértices y se usan para representar primitivas de forma más eficaz. Un búfer de índice contiene un conjunto secuencial de índices de 16 o 32 bits; cada índice se usa para identificar un vértice en un búfer de vértice. Un búfer de índice se puede visualizar como la siguiente ilustración.

![Ilustración de un búfer de índice](images/d3d10-index-buffer.png)

Los índices secuenciales almacenados en un búfer de índice se encuentran con los parámetros siguientes:

-   Offset: el número de bytes de la dirección base del búfer de índice. El desplazamiento se proporciona al método [**ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) .
-   StartIndexLocation: especifica el primer elemento de búfer de índice de la dirección base y el desplazamiento proporcionado en [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer). La ubicación de inicio se proporciona al método [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) o [**ID3D11DeviceContext::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) y representa el primer índice que se va a representar.
-   IndexCount: número de índices que se van a representar. El número se proporciona al método [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)

Inicio del búfer de índice = dirección base del búfer de índice + desplazamiento (bytes) + StartIndexLocation \* (bytes);

En este cálculo, el tamaño de los elementos es el tamaño de cada elemento de búfer de índice, que es de dos o cuatro bytes.

Para crear un búfer de índice, llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="constant-buffer"></a>Búfer de constantes

Un búfer de constantes permite proporcionar eficazmente datos de constantes de sombreador a la canalización. Puede usar un búfer de constantes para almacenar los resultados de la fase de flujo de salida. Conceptualmente, un búfer de constantes se parece a un búfer de vértice de un solo elemento, tal como se muestra en la siguiente ilustración.

![Ilustración de un búfer de constantes de sombreador](images/d3d10-shader-resource-buffer.png)

Cada elemento almacena una constante de componente de 1 a 4, determinada por el formato de los datos almacenados. Para crear un búfer de constantes de sombreador, llame a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) y especifique el miembro de **\_ búfer de \_ constantes \_ de enlace D3D11** del tipo enumerado del [**\_ \_ marcador de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Un búfer de constantes solo puede utilizar una única marca de enlace (**D3D11 de búfer de \_ \_ constantes \_ de enlace**), que no se puede combinar con ningún otro marcador de enlace. Para enlazar un búfer de constantes de sombreador a la canalización, llame a uno de los métodos siguientes: [**ID3D11DeviceContext:: GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**ID3D11DeviceContext::P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)o [**ID3D11DeviceContext:: VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Para leer un búfer de constantes de sombreador de un sombreador, use una función de carga de HLSL (por ejemplo, [**Load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)). Cada fase del sombreador permite hasta 15 búferes de constantes de sombreador; cada búfer puede contener hasta 4096 constantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 