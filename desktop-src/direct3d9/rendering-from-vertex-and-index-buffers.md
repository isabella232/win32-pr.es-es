---
description: Direct3D admite métodos de dibujo indexados y no indexados.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Representación de búferes de vértices y de índices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906438"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Representación de búferes de vértices y de índices (Direct3D 9)

Direct3D admite métodos de dibujo indexados y no indexados. Los métodos indizados usan un único conjunto de índices para todos los componentes de vértices. Los datos de vértice se almacenan en búferes de vértices y los datos de índice se almacenan en búferes de índice. A continuación se enumeran algunos escenarios comunes para dibujar primitivos mediante el uso de búferes de vértices y de índices.

En estos ejemplos se compara el uso de [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) y [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Escenario 1: dibujar dos triángulos sin indexación

Supongamos que desea dibujar la cuádruple que se muestra en la siguiente ilustración.

![Ilustración de un cuadrado que consta de dos triángulos](images/dip-fig1.png)

Si usa el tipo primitivo de la lista de triángulos para representar los dos triángulos, cada triángulo se almacenará como 3 vértices individuales, lo que dará lugar a un búfer de vértice similar a la siguiente ilustración.

![diagrama de un búfer de vértice que define tres vértices para dos triángulos](images/dip-fig2.png)

La llamada de dibujo es muy sencilla; a partir de la ubicación 0 dentro del búfer de vértices, dibuje dos triángulos. Si está habilitado el culling, el orden de los vértices será importante. En este ejemplo se da por supuesto el estado de selección en el sentido contrario a las agujas del reloj, por lo que los triángulos visibles deben dibujarse en el orden del reloj. El tipo primitivo de la lista triangular simplemente Lee tres vértices en orden lineal desde el búfer para cada triángulo, por lo que esta llamada dibujará triángulos (0, 1, 2) y (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Escenario 2: dibujar dos triángulos con indexación

Como observará, el búfer de vértices contiene datos duplicados en las ubicaciones 0 y 4, 2 y 5. Esto tiene sentido porque los dos triángulos comparten dos vértices comunes. Estos datos duplicados son excesivos y el búfer de vértices se puede comprimir mediante un búfer de índice. Un búfer de vértices más pequeño reduce la cantidad de datos de vértices que se deben enviar al adaptador de gráficos. Incluso más importante, el uso de un búfer de índice permite que el adaptador almacene los vértices en una memoria caché de vértices. Si el primitivo que se está dibujando contiene un vértice usado recientemente, ese vértice se puede capturar desde la memoria caché en lugar de leerlo desde el búfer de vértices, lo que provoca un aumento de gran rendimiento.

Un búfer de índice ' índices ' en el búfer de vértices, por lo que cada vértice único debe almacenarse una sola vez en el búfer de vértices. En el diagrama siguiente se muestra un enfoque indizado en el escenario de dibujo anterior.

![diagrama de un búfer de índice para el búfer de vértices anterior](images/dip-fig3.png)

El búfer de índice almacena los valores de índice de VB, que hacen referencia a un vértice determinado dentro del búfer de vértices. Un búfer de vértices se puede considerar como una matriz de vértices, por lo que el índice de VB es simplemente el índice en el búfer de vértices para el vértice de destino. Del mismo modo, un índice de IB es un índice en el búfer de índice. Esto puede resultar muy confuso si no tiene cuidado, por lo que debe asegurarse de que está claro en el vocabulario que se está usando: índice de valores de índice de VB en el búfer de vértices, IB index Values index en el búfer de índice y el propio búfer de índice almacena valores de índice de VB.

A continuación se muestra la llamada de dibujo. Los significados de todos los argumentos se describen en la longitud para el siguiente escenario de dibujo; por ahora, solo tenga en cuenta que esta llamada indica a Direct3D que represente una lista de triángulos que contiene dos triángulos, empezando en la ubicación 0 dentro del búfer de índice. Esta llamada dibujará los mismos dos triángulos en el mismo orden que antes, lo que garantiza una orientación adecuada en el sentido de las agujas del reloj:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Escenario 3: dibujo de un triángulo con indexación

Imagine ahora que desea dibujar solo el segundo triángulo, pero desea usar el mismo búfer de vértices y el búfer de índice que se usan al dibujar el cuádruple completo, tal como se muestra en el diagrama siguiente.

![diagrama del búfer de índice y del búfer de vértice del segundo triángulo](images/dip-fig4.png)

En esta llamada de dibujo, el primer índice de IB utilizado es 3; Este valor se denomina StartIndex. El índice de VB más bajo utilizado es 0; Este valor se denomina MinIndex. Aunque solo se necesitan tres vértices para dibujar el triángulo, los tres vértices se distribuyen en cuatro ubicaciones adyacentes en el búfer de vértices. el número de ubicaciones dentro del bloque contiguo de memoria del búfer de vértices necesario para la llamada de dibujo se denomina NumVertices y se establecerá en 4 en esta llamada. Los valores MinIndex y NumVertices son simplemente sugerencias para ayudar a Direct3D a optimizar el acceso a la memoria durante el procesamiento de vértices de software y se pueden establecer simplemente para incluir todo el búfer de vértices en el precio del rendimiento.

Esta es la llamada de dibujo del caso de un solo triángulo; el significado del argumento BaseVertexIndex se explicará a continuación:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Escenario 4: dibujo de un triángulo con índices de desplazamiento

BaseVertexIndex es un valor que se agrega de forma eficaz a cada índice de VB almacenado en el búfer de índice. Por ejemplo, si se hubiera pasado un valor de 50 para BaseVertexIndex durante la llamada anterior, esto sería lo mismo que usar el búfer de índice en el diagrama siguiente durante la llamada a DrawIndexedPrimitive:

![diagrama de un búfer de índice con un valor de 50 para basevertexindex](images/dip-fig5.png)

Este valor rara vez se establece en un valor distinto de 0, pero puede ser útil si desea desacoplar el búfer de índice del búfer de vértices: si al rellenar el búfer de índice para una malla determinada, la ubicación de la malla en el búfer de vértices no se conoce todavía, puede suponer que los vértices de la malla se encuentren al principio del búfer Cuando llega el momento de hacer la llamada a Draw, solo tiene que pasar la ubicación inicial real como BaseVertexIndex.

Esta técnica también se puede usar al dibujar varias instancias de una malla mediante un búfer de índice único. por ejemplo, si el búfer de vértices contenía dos mallas con un orden de dibujo idéntico, pero con vértices ligeramente diferentes (quizás diferentes colores difusos o coordenadas de textura), ambas mallas podrían dibujarse usando valores diferentes para BaseVertexIndex. Tomando este concepto un paso más, podría usar un búfer de índice para dibujar varias instancias de una malla, cada una de ellas en un búfer de vértices diferente, simplemente recorriendo el búfer de vértices activo y ajustando el BaseVertexIndex según sea necesario. Tenga en cuenta que el valor BaseVertexIndex también se agrega automáticamente al argumento MinIndex, que tiene sentido cuando se ve cómo se usa:

Imagine ahora que deseamos dibujar solo el segundo triángulo de la cuádruple con el mismo búfer de índice que antes; sin embargo, se usa un búfer de vértices diferente en el que se encuentra el cuádruple en el índice de VB 50. El orden relativo de los vértices cuádruples permanece sin cambios, solo la ubicación inicial dentro del búfer de vértices es diferente. El búfer de índice y el búfer de vértice serían similares al diagrama siguiente.

![diagrama del búfer de índice y del búfer de vértice con un índice de VB de 50](images/dip-fig6.png)

Esta es la llamada a Draw adecuada; Tenga en cuenta que BaseVertexIndex es el único valor que ha cambiado en el escenario anterior:


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

 

 
