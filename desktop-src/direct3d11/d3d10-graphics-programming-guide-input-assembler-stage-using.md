---
title: Usar valores System-Generated
description: Los valores generados por el sistema se generan mediante la fase del IA (basada en la semántica de entrada proporcionada por el usuario) para permitir ciertas eficiencias en las operaciones del sombreador.
ms.assetid: eed1e377-4b0e-4958-b6d4-945b2a952ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d484a42992206cb04aaef8fdd8ebaef6e08d7f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078023"
---
# <a name="using-system-generated-values"></a>Usar valores System-Generated

Los valores generados por el sistema se generan mediante la fase del IA (basada en la [semántica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)de entrada proporcionada por el usuario) para permitir ciertas eficiencias en las operaciones del sombreador.

Al adjuntar datos, como un identificador de instancia (visible para VS), un identificador de vértice (visible para VS) o un identificador primitivo (visible para GS/PS), una etapa del sombreador posterior puede buscar estos valores del sistema para optimizar el procesamiento en esa fase. Por ejemplo, la fase de VS puede buscar el identificador de instancia para captar datos adicionales por vértice para el sombreador o para realizar otras operaciones; las fases GS y PS pueden utilizar el identificador primitivo para capturar datos por primitivos de la misma manera.

-   [VertexID](#vertexid)
-   [PrimitiveID](#primitiveid)
-   [InstanceID](#instanceid)
-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="vertexid"></a>VertexID

Cada fase del sombreador usa un identificador de vértice para identificar cada vértice. Es un entero de 32 bits sin signo cuyo valor predeterminado es 0. Se asigna a un vértice cuando la fase del IA procesa el primitivo. Adjunte la semántica del identificador de vértice a la declaración de entrada del sombreador para informar a la fase del IA que genere un identificador por vértice.

El IA agregará un identificador de vértice a cada vértice para que lo usen las fases del sombreador. Para cada llamada a Draw, el identificador de vértice se incrementa en 1. En las llamadas a Draw indizadas, el recuento vuelve a establecer el valor de inicio. En el caso de [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) y [**ID3D11DeviceContext::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced), el identificador de vértice representa el valor de índice. Si el identificador de vértice desborda (supera 2 ³ ² – 1), se ajusta a 0.

En todos los tipos primitivos, los vértices tienen un identificador de vértice asociado a ellos (independientemente de la adyacencia).

## <a name="primitiveid"></a>PrimitiveID

Cada fase del sombreador usa un identificador primitivo para identificar cada primitiva. Es un entero de 32 bits sin signo cuyo valor predeterminado es 0. Se asigna a un primitivo cuando la fase del IA procesa el primitivo. Para informar a la fase del IA que genere un identificador primitivo, adjunte la semántica de identificador primitivo a la declaración de entrada del sombreador.

La fase IA agregará un identificador primitivo a cada primitivo para que lo use el sombreador de geometría o la etapa del sombreador de píxeles (lo que sea la primera fase activa después de la fase IA). En cada llamada a Draw indizada, el identificador primitivo se incrementa en 1; sin embargo, el identificador primitivo se restablece en 0 cada vez que se inicia una nueva instancia. Todas las demás llamadas a Draw no cambian el valor del identificador de instancia. Si el identificador de instancia se desborda (supera 2 ³ ² – 1), se ajusta a 0.

La fase del sombreador de píxeles no tiene una entrada independiente para un identificador primitivo; sin embargo, cualquier entrada del sombreador de píxeles que especifique un identificador primitivo utiliza un modo de interpolación constante.

No se admite la generación automática de un identificador primitivo para primitivos adyacentes. En el caso de los tipos primitivos con adyacencias, como una franja de triángulo con adyacencias, solo se mantiene un identificador primitivo para los primitivos interiores (los primitivos no adyacentes), al igual que el conjunto de primitivas en una franja de triángulo sin adyacencias.

## <a name="instanceid"></a>InstanceID

Cada fase del sombreador usa un identificador de instancia para identificar la instancia de la geometría que se está procesando actualmente. Es un entero de 32 bits sin signo cuyo valor predeterminado es 0.

La fase IA agregará un identificador de instancia a cada vértice si la declaración de entrada del sombreador de vértices incluye la semántica del identificador de instancia. Para cada llamada a Draw indizada, el ID. de instancia se incrementa en 1. Todas las demás llamadas a Draw no cambian el valor de ID. de instancia. Si el identificador de instancia se desborda (supera 2 ³ ² – 1), se ajusta a 0.

## <a name="example"></a>Ejemplo

En la ilustración siguiente se muestra cómo se adjuntan los valores del sistema a una franja de triángulo de instancia en la fase de IA.

![Ilustración de los valores del sistema para una franja de triángulo con instancias](images/d3d10-ia-example.png)

En estas tablas se muestran los valores del sistema generados para ambas instancias de la misma franja de triángulo. La primera instancia (instancia U) se muestra en azul; la segunda instancia (instancia V) se muestra en verde. Las líneas sólidas conectan los vértices de los primitivos, las líneas discontinuas conectan los vértices adyacentes.

En las tablas siguientes se muestran los valores generados por el sistema para la instancia U.



| Datos de vértices    | C, U | D, U | E, U | F, U | G, U | H, U | I, U | J, U | K, U | L, U |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |



 



|                 |     |     |     |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 0   | 0   | 0   |



 

En las tablas siguientes se muestran los valores generados por el sistema para la instancia V.



| Datos de vértices    | C, V | D, V | E, V | F, V | G, V | H, V | I, V | J, V | K, V | L, V |
|----------------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| **VertexID**   | 0   | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   |
| **InstanceID** | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |



 



|                 |     |     |     |
|-----------------|-----|-----|-----|
| **PrimitiveID** | 0   | 1   | 2   |
| **InstanceID**  | 1   | 1   | 1   |



 

El ensamblador de entrada genera los identificadores (vértice, primitivo e instancia); Observe también que a cada instancia se le asigna un identificador de instancia único. Los datos finalizan con el corte de franja, que separa cada instancia de la franja de triángulo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Fase del ensamblador de entrada](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 