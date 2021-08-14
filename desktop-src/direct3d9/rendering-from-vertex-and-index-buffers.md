---
description: Direct3D admite los métodos de dibujo indexados y no indexados.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Representación a partir de búferes de vértices e índices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4290dc2ff40e1ec0448e3948342aa3b02ac62bf9866a44958ea53bee9658d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092644"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Representación a partir de búferes de vértices e índices (Direct3D 9)

Direct3D admite los métodos de dibujo indexados y no indexados. Los métodos indexados usan un único conjunto de índices para todos los componentes de vértice. Los datos de vértices se almacenan en búferes de vértices y los datos de índice se almacenan en búferes de índice. A continuación se enumeran algunos escenarios comunes para dibujar primitivos mediante búferes de vértices e índices.

En estos ejemplos se compara el uso de [**IDirect3DDevice9::D rawPrimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Escenario 1: Dibujar dos triángulos sin indexación

Supongamos que desea dibujar el cuadrándular que se muestra en la ilustración siguiente.

![ilustración de un cuadrado que consta de dos triángulos](images/dip-fig1.png)

Si usa el tipo primitivo Lista de triángulos para representar los dos triángulos, cada triángulo se almacenará como tres vértices individuales, lo que dará como resultado un búfer de vértice similar a la ilustración siguiente.

![diagrama de un búfer de vértices que define tres vértices para dos triángulos](images/dip-fig2.png)

La llamada de dibujo es muy sencilla; a partir de la ubicación 0 dentro del búfer de vértices, dibuje dos triángulos. Si la selección está habilitada, el orden de los vértices será importante. En este ejemplo se da por supuesto el estado predeterminado de la selección en sentido contrario a las agujas del reloj, por lo que los triángulos visibles deben dibujarse en el sentido de las agujas del reloj. El tipo primitivo Lista de triángulos simplemente lee tres vértices en orden lineal del búfer para cada triángulo, por lo que esta llamada dibujará triángulos (0, 1, 2) y (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Escenario 2: Dibujar dos triángulos con indexación

Como observará, el búfer de vértices contiene datos duplicados en las ubicaciones 0 y 4, 2 y 5. Esto tiene sentido porque los dos triángulos comparten dos vértices comunes. Estos datos duplicados son un desperdicio y el búfer de vértices se puede comprimir mediante un búfer de índice. Un búfer de vértices más pequeño reduce la cantidad de datos de vértice que se deben enviar al adaptador de gráficos. Aún más importante, el uso de un búfer de índice permite al adaptador almacenar vértices en una caché de vértices. si el primitivo que se dibuja contiene un vértice usado recientemente, ese vértice se puede capturar de la memoria caché en lugar de leerlo desde el búfer de vértices, lo que da como resultado un gran aumento del rendimiento.

Un búfer de índice "índices" en el búfer de vértices, por lo que cada vértice único debe almacenarse solo una vez en el búfer de vértices. En el diagrama siguiente se muestra un enfoque indexado para el escenario de dibujo anterior.

![diagrama de un búfer de índice para el búfer de vértices anterior](images/dip-fig3.png)

El búfer de índice almacena VB de índice, que hacen referencia a un vértice determinado dentro del búfer de vértices. Un búfer de vértices se puede pensar en como una matriz de vértices, por lo que el índice VB es simplemente el índice en el búfer de vértices para el vértice de destino. De forma similar, un índice IB es un índice en el búfer de índice. Esto puede resultar muy confuso muy rápidamente si no tiene cuidado, así que asegúrese de que está claro el vocabulario que se usa: VB Índice de valores de índice en el búfer de vértices, Índice de valores de índice IB en el búfer de índice y el propio búfer de índice almacena VB Valores de índice.

A continuación se muestra la llamada de dibujo. Los significados de todos los argumentos se analizan en longitud para el siguiente escenario de dibujo; Por ahora, solo tiene que tener en cuenta que esta llamada indica de nuevo a Direct3D que represente una lista de triángulos que contenga dos triángulos, empezando en la ubicación 0 dentro del búfer de índice. Esta llamada dibujará los mismos dos triángulos en el mismo orden exacto que antes, lo que garantiza una orientación correcta en el sentido de las agujas del reloj:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Escenario 3: Dibujar un triángulo con indexación

Ahora pretende que solo quiere dibujar el segundo triángulo, pero quiere usar el mismo búfer de vértices y búfer de índice que se usan al dibujar el cuadrándulo completo, como se muestra en el diagrama siguiente.

![diagrama del búfer de índice y el búfer de vértices para el segundo triángulo](images/dip-fig4.png)

Para esta llamada de dibujo, el primer índice IB utilizado es 3; Este valor se denomina StartIndex. El índice VB menor utilizado es 0; Este valor se denomina MinIndex. Aunque solo se necesitan tres vértices para dibujar el triángulo, esos tres vértices se reparten entre cuatro ubicaciones adyacentes en el búfer de vértices. El número de ubicaciones dentro del bloque contiguo de memoria de búfer de vértices necesaria para la llamada de dibujo se denomina NumVertices y se establecerá en 4 en esta llamada. Los valores MinIndex y NumVertices son simplemente sugerencias para ayudar a Direct3D a optimizar el acceso a la memoria durante el procesamiento de vértices de software, y simplemente se pueden establecer para incluir todo el búfer de vértices a precio de rendimiento.

Esta es la llamada de dibujo para el caso de triángulo único; El significado del argumento BaseVertexIndex se explicará a continuación:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Escenario 4: Dibujar un triángulo con indexación de desplazamiento

BaseVertexIndex es un valor que se agrega eficazmente a cada índice VB almacenado en el búfer de índice. Por ejemplo, si se hubiera pasado un valor de 50 para BaseVertexIndex durante la llamada anterior, funcionalmente sería lo mismo que usar el búfer de índice en el diagrama siguiente durante la duración de la llamada DrawIndexedPrimitive:

![diagrama de un búfer de índice con un valor de 50 para basevertexindex](images/dip-fig5.png)

Este valor rara vez se establece en algo distinto de 0, pero puede ser útil si desea desacoplar el búfer de índice del búfer de vértices: si al rellenar el búfer de índice para una malla determinada aún no se conoce la ubicación de la malla dentro del búfer de vértices, simplemente puede simular que los vértices de malla se ubicarán al principio del búfer de vértices. cuando llegue el momento de realizar la llamada a draw, simplemente pase la ubicación inicial real como BaseVertexIndex.

Esta técnica también se puede usar al dibujar varias instancias de una malla mediante un único búfer de índice. Por ejemplo, si el búfer de vértices contenía dos mallas con un orden de dibujo idéntico pero vértices ligeramente diferentes (quizás diferentes colores difusos o coordenadas de textura), ambas mallas se podrían dibujar utilizando valores diferentes para BaseVertexIndex. Si este concepto va un paso más allá, podría usar un búfer de índice para dibujar varias instancias de una malla, cada una contenida en un búfer de vértices diferente, simplemente mediante el ciclo de qué búfer de vértices está activo y ajustando BaseVertexIndex según sea necesario. Tenga en cuenta que el valor BaseVertexIndex también se agrega automáticamente al argumento MinIndex, lo que tiene sentido cuando se ve cómo se usa:

Ahora pretendemos que de nuevo queremos dibujar solo el segundo triángulo del cuádulo con el mismo búfer de índice que antes. sin embargo, se usa un búfer de vértices diferente en el que el cuadrándice se encuentra en VB índice 50. El orden relativo de los vértices cuadráticos no cambia, solo la ubicación inicial dentro del búfer de vértices es diferente. El búfer de índice y el búfer de vértices tendrían un aspecto parecido al diagrama siguiente.

![diagrama del búfer de índice y el búfer de vértices con un índice vb de 50](images/dip-fig6.png)

Esta es la llamada a draw adecuada; Tenga en cuenta que BaseVertexIndex es el único valor que ha cambiado con respecto al escenario anterior:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de primitivas](rendering-primitives.md)
</dt> </dl>

 

 
