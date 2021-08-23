---
title: 'Registros: hs_5_0'
description: Un sombreador de casco consta de tres fases distintas fase de punto de control, fase de bifurcación y fase de combinación. Cada fase tiene sus propios conjuntos de registros de entrada y salida.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3891130b4a952cb991615dbcc386e245d5eb8abedc2d8cec0b441eb6b3c2fbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854035"
---
# <a name="registers---hs_5_0"></a>Registros: hs \_ 5 \_ 0

Un sombreador de casco consta de tres fases distintas: fase de punto de control, fase de bifurcación y fase de combinación. Cada fase tiene sus propios conjuntos de registros de entrada y salida.

## <a name="control-point-phase"></a>Fase de punto de control

La fase de \_ punto de control \_ \_ hs es un programa de sombreador con el siguiente modelo de registro.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Count                 | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                 | 4096(r \# +x \# \[ n \] )    | L/E | 4         | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] )    | L/E | 4         | Sí              | None     | Sí          |
| Entrada de 32 bits (elemento de vértice v \[ \] \[ \] )             | 32(element) \* 32(vert) | R   | 4         | Sí              | None     | Sí          |
| Entrada UINT de 32 bits vOutputControlPointID(23.7)     | 1                     | R   | 1         | No               | None     | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)             | 1                     | R   | 1         | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                | 128                   | R   | 128       | Sí              | None     | Sí          |
| Sampler (s \# )                                     | 16                    | R   | 1         | Sí              | None     | Sí          |
| Referencia de ConstantBuffer (índice cb \# \[ \] )          | 15                    | R   | 4         | Sí              | None     | Sí          |
| Referencia de ConstantBuffer inmediato (índice icb \[ \] ) | 1                     | R   | 4         | Sí (contenido)   | Ninguno     | Sí          |



 

### <a name="output-registers"></a>Registros de salida



| Tipo de registro                           | Count | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de datos vertex de salida de 32 bits (o \# ) | 32    | W   | 4         | Sí              | None     | Sí          |



 

Cada registro de salida de la fase de punto de control del sombreador de casco es de hasta 4 vectores, de los cuales se pueden declarar hasta 32 registros. También hay de 1 a 32 puntos de control de salida declarados, lo que escala la cantidad de almacenamiento necesario. Vamos a hacer referencia al número agregado máximo permitido de escalares en todos los resultados de la fase de punto de control del sombreador de casco como \# cp \_ output \_ max.

\#cp \_ output max = \_ 3968 escalares.

Este límite se basa en un punto de diseño para cierto hardware de almacenamiento de 32 bits de 4096 \* aquí. La cantidad de salida del punto de control es 3968=4096-128, que es 32(puntos de control) \* 4(componentes) \* 32(elementos) - 4(componentes) \* 32(elementos). La resta reserva 128 escalares (un punto de control) de espacio dedicados a la fase 2 y 3 del sombreador de casco. La opción de reservar 128 escalares para constantes de revisión , en lugar de permitir que la cantidad sea simplemente cualquiera de los 4096 escalares de almacenamiento que los puntos de control de salida no usan, se adapta a los límites de otro diseño de hardware determinado. La fase de punto de control puede declarar 32 puntos de control de salida, pero no pueden ser totalmente 32 elementos con 4 componentes cada uno, porque el almacenamiento total sería demasiado alto.

## <a name="fork-phase"></a>Fase de bifurcación

Los registros siguientes son visibles en el modelo de fase \_ de \_ bifurcación hs.

Los recursos de entrada (t), los muestreadores (s), los búferes constantes (cb) y el búfer constante \# inmediato (icb) siguientes son el estado compartido con todas las demás fases del \# \# sombreador de casco. Es decir, desde el punto de vista de la API/DDI, el sombreador de casco tiene un único conjunto de estado de recursos de entrada para todas las fases. Esto va con el hecho de que, desde el punto de vista de la API/DDI, el sombreador de casco es un único sombreador atómico; las fases dentro de ella son detalles de implementación.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                         | Count              | L/E | Dimensión                           | Indexable by r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                                                     | 4096(r \# +x \# \[ n \] ) | L/E | 4                                   | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )                                                | 4096(r \# +x \# \[ n \] ) | L/E | 4                                   | Sí              | None     | Sí          |
| Puntos de control de entrada de 32 bits (elemento de vértice de sentidop \[ \] \[ \] ) (fase de punto de control anterior)     | 32 Vea la nota siguiente  | R   | 4(component) \* 32(element) \* 32(vert) | Sí              | None     | Sí          |
| Puntos de control de salida de 32 bits (elemento de vértice vocp \[ \] \[ \] \] ) (fase posterior al punto de control) | 32 Vea la nota siguiente  | R   | 4(component) \* 32(element) \* 32(vert) | Sí              | None     | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                                                 | 1                  | R   | 1                                   | No               | N/D      | Sí          |
| ForkInstanceID(23.8) de entrada UINT de 32 bits (vForkInstanceID)                              | 1                  | R   | 1                                   | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                                                    | 128                | R   | 128                                 | Sí              | None     | Sí          |
| Sampler (s \# )                                                                         | 16                 | R   | 1                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer (índice \# \[ \] cb)                                              | 15                 | R   | 4                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer inmediato (índice icb \[ \] )                                     | 1                  | R   | 4                                   | Sí (contenido)   | Ninguno     | Sí          |



 

> [!Note]
> Las declaraciones de registro de punto de control de entrada (ezp) de la fase de bifurcación del sombreador de casco deben ser cualquier subconjunto, a lo largo del eje de elemento, de la entrada del punto de control del sombreador de casco (fase de punto de \[ \] control previo). De forma similar, las declaraciones para la entrada de los puntos de control de salida (vocp) deben ser cualquier subconjunto, a lo largo del eje de elementos, de los puntos de control de salida del sombreador de casco (fase posterior al \[ \] punto de control).
> 
> A lo largo del eje de vértices, el número de puntos de control que se leerán para cada uno de los puntos de control de salida y vocp debe ser similar a un subconjunto del recuento de puntos de control de entrada del sombreador de casco y del número de puntos de control de salida del sombreador de \[ \] casco, respectivamente. Por ejemplo, si el eje de vértices de los registros de vocp se declara con n vértices, esto hace que los puntos de control de salida de la fase de punto de control \[ 0..n-1 estén disponibles como entrada de solo lectura en la fase de \] bifurcación.

### <a name="output-registers"></a>Registros de salida



| Registrarse                                        | Count               | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Elemento patch constant data (o) de salida de 32 bits \# | 32 Vea la nota 1 a continuación. | W   | 4         | Sí              | None     | Sí          |



 

> [!Note]  
> Las salidas de la bifurcación y la fase de combinación del sombreador de casco son un conjunto compartido de 4 registros de 4 vectores. Las salidas de cada programa de la fase de bifurcación o combinación no se pueden superponer entre sí. Los valores interpretados por el sistema, como TessFactors, proceden de este espacio.

## <a name="join-phase"></a>Fase de unión

Los registros siguientes son visibles en el modelo de fase de \_ \_ combinación hs. Hay tres conjuntos de registros de entrada: puntos de control de entrada de fase de punto de control (cvp), puntos de control de salida de fase de control vocp (vocp) y constantes de revisión (vcp). son la salida agregada de todos los programas de fase de bifurcación del sombreador de casco. Los registros de salida de la fase de combinación del sombreador de casco se encuentran en el mismo espacio de registro que las salidas de la fase de bifurcación \# del sombreador de casco.

Los recursos de entrada (t), los muestreadores (s), los búferes constantes (cb) y el búfer constante \# inmediato (icb) siguientes son el estado compartido con todas las demás fases del \# \# sombreador de casco. Es decir, desde el punto de vista de la API/DDI, el sombreador de casco tiene un único conjunto de estado de recursos de entrada para todas las fases. Esto va con el hecho de que, desde el punto de vista de la API/DDI, el sombreador de casco es un único sombreador atómico; las fases dentro de ella son detalles de implementación.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                       | Count               | L/E | Dimensión                           | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp de 32 bits (r \# )                                                                   | 4096(r \# +x \# \[ n \] )  | L/E | 4                                   | No               | None     | Sí          |
| Matriz temporal indexable de 32 bits (x \# \[ n \] )                                              | 4096(r \# +x \# \[ n \] )  | L/E | 4                                   | Sí              | None     | Sí          |
| Puntos de control de entrada de 32 bits (elemento de vértice Dep \[ \] \[ \] ) (fase de punto de control anterior)   | 32 Vea la nota 1 a continuación. | R   | 4(component) \* 32(element) \* 32(vert) | Sí              | None     | Sí          |
| Puntos de control de salida de 32 bits (elemento de vértice vocp \[ \] \[ \] ) (fase posterior al punto de control) | 32 Vea la nota 1 a continuación. | R   | 4(component) \* 32(element) \* 32(vert) | Sí              | None     | Sí          |
| Entrada de 32 bits (elemento de vpc \[ \] ) (datos constantes de revisión)                                 | 32 Vea la nota 2 a continuación. | R   | 4                                   | Sí              | None     | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                                               | 1                   | R   | 1                                   | No               | N/D      | Sí          |
| JoinInstanceID de entrada UINT de 32 bits (vJoinInstanceID)                                  | 1                   | R   | 1                                   | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                                                  | 128                 | R   | 128                                 | Sí              | None     | Sí          |
| Sampler (s \# )                                                                       | 16                  | R   | 1                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer (índice cb \# \[ \] )                                            | 15                  | R   | 4                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer inmediato (índice icb \[ \] )                                   | 1                   | R   | 4                                   | Sí (contenido)   | Ninguno     | Sí          |



 

**Nota 1:** Las declaraciones de registro de punto de control de entrada (lop) de la fase de combinación del sombreador de casco deben ser cualquier subconjunto, a lo largo del eje de elemento, de la entrada del punto de control del sombreador de casco (fase de punto de \[ \] control previo). De forma similar, las declaraciones para la entrada de los puntos de control de salida (vocp) deben ser cualquier subconjunto, a lo largo del eje de elementos, de los puntos de control de salida del sombreador de casco (fase posterior al \[ \] punto de control).

A lo largo del eje de vértices, el número de puntos de control que se leerán para cada uno de los puntos de control de salida y vocp debe ser similar a un subconjunto del recuento de puntos de control de entrada del sombreador de casco y del número de puntos de control de salida del sombreador de \[ \] casco, respectivamente. Por ejemplo, si el eje de vértices de los registros de vocp se declara con n vértices, esto hace que los puntos de control de salida de la fase de punto de control \[ 0..n-1 estén disponibles como entrada de solo lectura en la fase de \] combinación.

**Nota 2:** Además de la entrada de punto de control, la fase de combinación del sombreador de casco también ve como entrada los datos constantes de revisión calculados por los programas de fase de bifurcación del sombreador de casco. Esto se muestra en la fase de bifurcación del sombreador de casco a medida que se \# registra la vpc. Los registros de entrada de la fase de combinación del sombreador de casco comparten el mismo espacio de registro que los registros de salida de la fase de bifurcación del sombreador \# \# de casco. Las declaraciones de los registros o no deben superponerse con ninguna declaración de salida o programa de fase de bifurcación del sombreador de casco; la fase de combinación del sombreador de casco se agrega a la salida de datos de constante de revisión agregada para el sombreador de \# \# casco.

### <a name="output-registers"></a>Registros de salida



| Tipo de registro                                   | Count             | L/E | Dimensión | Indexable by r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Elemento patch constant data (o) de salida de 32 bits \# | 32 Vea la nota siguiente | W   | 4         | Sí              | None     | Sí          |



 

> [!Note]  
> Las salidas de bifurcación y fase de combinación del sombreador de casco son un conjunto compartido de 4 registros de 4 vectores. Las salidas de cada programa de la fase de bifurcación o combinación no se pueden superponer entre sí. Los valores interpretados por el sistema, como TessFactors, proceden de este espacio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




