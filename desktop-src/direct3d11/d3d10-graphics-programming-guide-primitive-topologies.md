---
title: Topologías primitivas
description: Direct3D 10 y versiones posteriores admiten varios tipos primitivos (o topologías) que están representados por el \_ tipo enumerado de la topología de D3D Primitive \_ . Estos tipos definen cómo se interpretan y representan los vértices mediante la canalización.
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359001"
---
# <a name="primitive-topologies"></a>Topologías primitivas

Direct3D 10 y versiones posteriores admiten varios tipos primitivos (o topologías) que están representados por el tipo enumerado de la [**topología de D3D \_ Primitive \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Estos tipos definen cómo se interpretan y representan los vértices mediante la canalización.

-   [Tipos primitivos básicos](#basic-primitive-types)
-   [Adyacencia primitiva](#primitive-adjacency)
-   [Dirección de bobinado y posiciones de vértice iniciales](#winding-direction-and-leading-vertex-positions)
-   [Generación de varias bandas](#generating-multiple-strips)
-   [Temas relacionados](#related-topics)

## <a name="basic-primitive-types"></a>Tipos primitivos básicos

Se admiten los siguientes tipos primitivos básicos:

-   [Lista de puntos](/windows/desktop/direct3d9/point-lists)
-   [Lista de líneas](/windows/desktop/direct3d9/line-lists)
-   [Franja de líneas](/windows/desktop/direct3d9/line-strips)
-   [Lista de triángulos](/windows/desktop/direct3d9/triangle-lists)
-   [Franja](/windows/desktop/direct3d9/triangle-strips)

Para ver una visualización de cada tipo primitivo, vea el diagrama que aparece más adelante en este tema en [dirección de bobinado y posiciones de vértice iniciales](#winding-direction-and-leading-vertex-positions).

La fase del ensamblador de entrada Lee los datos de los búferes de vértices y de índices, ensambla los datos en estos primitivos y, a continuación, envía los datos a las fases de canalización restantes. (Puede utilizar el método [**ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) para especificar el tipo primitivo para la fase del ensamblador de entrada).

## <a name="primitive-adjacency"></a>Adyacencia primitiva

Todos los tipos primitivos de Direct3D 10 y superior (excepto la lista de puntos) están disponibles en dos versiones: un tipo primitivo con adyacencias y un tipo primitivo sin adyacencias. Los primitivos con adyacencias contienen algunos de los vértices circundantes, mientras que los primitivos sin adyacencias contienen solo los vértices de la primitiva de destino. Por ejemplo, la primitiva de la lista de líneas (representada por el valor LINELIST de la **\_ \_ topología \_ primitiva D3D** ) tiene un primitivo de lista de líneas correspondiente que incluye la adyacencia (representada por el valor de ADJ de la **\_ \_ topología \_ \_ primitiva de D3D** ).

Los primitivos adyacentes están diseñados para proporcionar más información sobre su geometría y solo son visibles a través de un sombreador de geometría. La adyacencia es útil para los sombreadores de geometría que utilizan la detección de silueta, la extrusión de volumen de sombra, etc.

Por ejemplo, supongamos que desea dibujar una lista de triángulos con adyacencias. Una lista de triángulos que contiene 36 vértices (con adyacencias) producirá 6 primitivas completadas. Las primitivas con adyacencias (excepto las bandas de líneas) contienen exactamente el doble de vértices que el primitivo equivalente sin adyacencias, donde cada vértice adicional es un vértice adyacente.

## <a name="winding-direction-and-leading-vertex-positions"></a>Dirección de bobinado y posiciones de vértice iniciales

Como se muestra en la siguiente ilustración, un vértice inicial es el primer vértice no adyacente de un primitivo. Un tipo primitivo puede tener varios vértices iniciales definidos, siempre y cuando cada uno se use para un primitivo diferente. En el caso de una franja de triángulo con adyacencias, los vértices iniciales son 0, 2, 4, 6, etc. En el caso de una franja de líneas con adyacencias, los vértices iniciales son 1, 2, 3, etc. Por otro lado, un primitivo adyacente no tiene ningún vértice inicial.

En la ilustración siguiente se muestra el orden de los vértices de todos los tipos primitivos que puede generar el ensamblador de entrada.

![diagrama de ordenación de vértices para tipos primitivos](images/d3d10-primitive-topologies.png)

Los símbolos de la ilustración anterior se describen en la tabla siguiente.



| Símbolo                                                                                   | NOMBRE              | Descripción                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![símbolo de un vértice](images/d3d10-primitive-topologies-vertex.png)                     | Vértice            | Punto en el espacio 3D.                                                                                                                                                                               |
| ![símbolo de dirección de bobinado](images/d3d10-primitive-topologies-winding-direction.png) | Dirección de bobinado | El orden de los vértices al ensamblar un primitivo. Puede ser en el sentido contrario a las agujas del reloj; Especifique esta llamada a [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1). |
| ![símbolo para el vértice inicial](images/d3d10-primitive-topologies-leading-vertex.png)       | Vértice inicial    | Primer vértice no adyacente de un primitivo que contiene datos por constante.                                                                                                                      |



 

## <a name="generating-multiple-strips"></a>Generación de varias bandas

Puede generar varias bandas a través de la reducción de la franja. Puede realizar un corte de franja llamando explícitamente a la función HLSL [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) o insertando un valor de índice especial en el búfer de índice. Este valor es-1, que es 0xFFFFFFFF para índices de 32 bits o 0xFFFF para índices de 16 bits. Un índice de – 1 indica un "cortar" explícito o un "reinicio" de la franja actual. El índice anterior completa el primitivo o la franja anterior y el índice siguiente inicia una nueva banda o primitiva. Para obtener más información sobre la generación de varias bandas, vea [la fase de sombreador de geometría](/previous-versions//bb205146(v=vs.85)).

> [!Note]  
> Necesita el [nivel de características](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 o un hardware superior porque no todo el hardware de 10level9 implementa esta funcionalidad.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con la fase de Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[Fases de canalización (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 