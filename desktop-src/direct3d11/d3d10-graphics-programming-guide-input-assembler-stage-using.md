---
title: Uso de System-Generated valores
description: Los valores generados por el sistema se generan mediante la fase IA (basada en la semántica de entrada proporcionada por el usuario) para permitir ciertas eficiencias en las operaciones del sombreador.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdc723d335fd78277051099ec05b43ed954174d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335210"
---
# <a name="using-system-generated-values"></a>Uso de System-Generated valores

Los valores generados por el sistema se generan mediante la fase IA (basada en la semántica de entrada proporcionada por el usuario) para permitir ciertas [eficiencias](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)en las operaciones del sombreador.

Al adjuntar datos, como un identificador de instancia (visible para VS), un identificador de vértice (visible para VS) o un identificador primitivo (visible para GS/PS), una fase posterior del sombreador puede buscar estos valores del sistema para optimizar el procesamiento en esa fase. Por ejemplo, la fase de VS puede buscar el identificador de instancia para obtener datos adicionales por vértice para el sombreador o para realizar otras operaciones; Las fases GS y PS pueden usar el identificador primitivo para obtener datos por primitivo de la misma manera.

-   [VertexID](#vertexid)
-   [PrimitiveID](#primitiveid)
-   [InstanceID](#instanceid)
-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="vertexid"></a>VertexID

Cada fase del sombreador usa un identificador de vértice para identificar cada vértice. Es un entero de 32 bits sin signo cuyo valor predeterminado es 0. Se asigna a un vértice cuando la fase IA procesa la primitiva. Adjunte la semántica vertex-id a la declaración de entrada del sombreador para informar a la fase IA de que genere un identificador por vértice.

El IA agregará un identificador de vértice a cada vértice para que lo usen las fases del sombreador. Para cada llamada a draw, el identificador de vértice se incrementa en 1. En las llamadas a draw indexadas, el recuento se restablece al valor inicial. Para [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) e [**ID3D11DeviceContext::D rawIndexedInstanced,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced)el identificador de vértice representa el valor del índice. Si el identificador de vértice se desborda (supera 2- 1), se ajusta a 0.

Para todos los tipos primitivos, los vértices tienen un identificador de vértice asociado a ellos (independientemente de la adyacencia).

## <a name="primitiveid"></a>PrimitiveID

Cada fase del sombreador usa un identificador primitivo para identificar cada primitivo. Es un entero de 32 bits sin signo cuyo valor predeterminado es 0. Se asigna a una primitiva cuando la fase IA procesa la primitiva. Para informar a la fase IA de que genere un identificador primitivo, adjunte la semántica primitive-id a la declaración de entrada del sombreador.

La fase IA agregará un identificador primitivo a cada primitivo para que lo use el sombreador de geometría o la fase del sombreador de píxeles (la que sea la primera fase activa después de la fase IA). Para cada llamada a draw indexada, el identificador primitivo se incrementa en 1; sin embargo, el identificador primitivo se restablece a 0 cada vez que comienza una nueva instancia. Todas las demás llamadas a draw no cambian el valor del identificador de instancia. Si el identificador de instancia se desborda (es superior a 2: 1), se ajusta a 0.

La fase del sombreador de píxeles no tiene una entrada independiente para un identificador primitivo; sin embargo, cualquier entrada de sombreador de píxeles que especifique un identificador primitivo usa un modo de interpolación constante.

No se admite la generación automática de un identificador primitivo para las primitivas adyacentes. Para los tipos primitivos con adyacencia, como una franja de triángulo con adyacencia, solo se mantiene un identificador primitivo para las primitivas interiores (las primitivas no adyacentes), igual que el conjunto de primitivas de una franja de triángulos sin adyacencia.

## <a name="instanceid"></a>InstanceID

Cada fase del sombreador usa un identificador de instancia para identificar la instancia de la geometría que se está procesando actualmente. Es un entero de 32 bits sin signo cuyo valor predeterminado es 0.

La fase IA agregará un identificador de instancia a cada vértice si la declaración de entrada del sombreador de vértices incluye la semántica del identificador de instancia. Para cada llamada a draw indexada, el identificador de instancia se incrementa en 1. Todas las demás llamadas a draw no cambian el valor del identificador de instancia. Si el identificador de instancia se desborda (es superior a 2- 1), se ajusta a 0.

## <a name="example"></a>Ejemplo

En la ilustración siguiente se muestra cómo se asocian los valores del sistema a una franja de triángulos con instancias en la fase IA.

![ilustración de valores del sistema para una franja de triángulo de instancia](images/d3d10-ia-example.png)

Estas tablas muestran los valores del sistema generados para ambas instancias de la misma franja de triángulos. La primera instancia (instancia U) se muestra en azul y la segunda instancia (instancia V) en verde. Las líneas sólidas conectan los vértices de los primitivos, las líneas discontinuas conectan los vértices adyacentes.

En las tablas siguientes se muestran los valores generados por el sistema para la instancia U.



| Datos de vértices    | C,U | D,U | E,U | F,U | G,U | H,U | I,U | J,U | K,U | L,U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 | Valor    | Valor    | Valor    |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

En las tablas siguientes se muestran los valores generados por el sistema para la instancia V.



| Datos de vértices    | C,V | D,V | E,V | F,V | G,V | H,V | I,V | J,V | K,V | L,V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |Valor     | Valor    |  Valor   |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

El ensamblador de entrada genera los identificadores (vértice, primitivo e instancia); Observe también que a cada instancia se le proporciona un identificador de instancia único. Los datos terminan con el corte de franja, que separa cada instancia de la franja del triángulo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase del ensamblador de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 