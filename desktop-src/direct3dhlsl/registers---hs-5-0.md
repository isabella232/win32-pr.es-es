---
title: 'Registros: hs_5_0'
description: Un sombreador de casco consta de tres fases distintas fase de punto de control, fase de bifurcación y fase de combinación. Cada fase tiene sus propios conjuntos de registros de entrada y salida.
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aca1377c7ca6b56434c361ba06b01cf659319f6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361978"
---
# <a name="registers---hs_5_0"></a>Registros-HS \_ 5 \_ 0

Un sombreador de casco consta de tres fases distintas: fase de punto de control, fase de bifurcación y fase de combinación. Cada fase tiene sus propios conjuntos de registros de entrada y salida.

## <a name="control-point-phase"></a>Fase de punto de control

\_ \_ la fase de punto de control HS \_ es un programa de sombreador con el siguiente modelo de registro.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                     | Count                 | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                 | 4096 (r \# + x \# \[ n \] )    | L/E | 4         | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] )    | L/E | 4         | Sí              | None     | Sí          |
| Entrada de bit 32 ( \[ elemento de vértice v \] \[ \] )             | 32 (elemento) \* 32 (Vert) | R   | 4         | Sí              | None     | Sí          |
| vOutputControlPointID de entrada UINT de 32 bits (23.7)     | 1                     | R   | 1         | No               | None     | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)             | 1                     | R   | 1         | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                | 128                   | R   | 128       | Sí              | None     | Sí          |
| Muestras (s \# )                                     | 16                    | R   | 1         | Sí              | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )          | 15                    | R   | 4         | Sí              | None     | Sí          |
| Referencia de ConstantBuffer inmediata ( \[ Índice de ICB \] ) | 1                     | R   | 4         | Sí (contenido)   | Ninguno     | Sí          |



 

### <a name="output-registers"></a>Registros de salida



| Tipo de registro                           | Count | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento de datos de vértice de salida de 32 bits (o \# ) | 32    | W   | 4         | Sí              | None     | Sí          |



 

Cada registro de salida de fase de punto de control del sombreador de casco es hasta un vector de 4, de los cuales se pueden declarar hasta 32 registros. También hay de 1 a 32 puntos de control de salida declarados, que escala la cantidad de almacenamiento necesario. Vamos a hacer referencia al número agregado máximo permitido de escalares en todas las salidas de fase de punto de control del sombreador de casco como la \# salida de CP \_ \_ máx.

\#CP \_ Output \_ max = 3968 Scalar.

Este límite se basa en un punto de diseño para cierto hardware de \* almacenamiento de 4096 32 bits aquí. La cantidad de la salida de punto de control es 3968 = 4096-128, que es 32 (puntos de control) \* 4 (componentes) \* 32 (elementos)-4 (componentes) \* 32 (elementos). La resta reserva 128 escalares (un punto de control) de espacio dedicado a las fases 2 y 3 del sombreador de casco. La opción de reservar 128 escalares para constantes de revisión, en lugar de permitir que la cantidad sea simplemente cualquiera de los 4096 escalares de almacenamiento, no se use en los puntos de control de salida, sino que admite los límites de otro diseño de hardware determinado. La fase de punto de control puede declarar 32 puntos de control de salida, pero simplemente no pueden ser totalmente de 32 elementos con 4 componentes, ya que el almacenamiento total sería demasiado alto.

## <a name="fork-phase"></a>Fase de bifurcación

Los registros siguientes están visibles en el modelo de \_ fase de bifurcación HS \_ .

Los recursos de entrada (t \# ), los muestreadores \# , los búferes de constantes (CB \# ) y el búfer de constantes inmediatas (ICB) son todos Estados compartidos con todas las demás fases del sombreador de casco. Es decir, desde el punto de vista de la API/DDI, el sombreador de casco tiene un único conjunto de estado de recursos de entrada para todas las fases. Esto se refiere al hecho de que, desde el punto de vista de la API/DDI, el sombreador de casco es un sombreador atómico único; las fases que contiene son detalles de la implementación.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                         | Count              | L/E | Dimensión                           | Indexable por r\# | Valores predeterminados | Requiere DCL |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                                                     | 4096 (r \# + x \# \[ n \] ) | L/E | 4                                   | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )                                                | 4096 (r \# + x \# \[ n \] ) | L/E | 4                                   | Sí              | None     | Sí          |
| Puntos de control de entrada de 32 bits ( \[ elemento de vértice VICP \] \[ \] ) (fase de punto de control anterior)     | 32 vea la nota siguiente  | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sí              | None     | Sí          |
| Puntos de control de salida de 32 bits \[ ( \] \[ elemento de vértice Vocp \] \] ) (fase de punto de control posterior) | 32 vea la nota siguiente  | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sí              | None     | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                                                 | 1                  | R   | 1                                   | No               | N/D      | Sí          |
| ForkInstanceID de entrada UINT de 32 bits (23.8) (vForkInstanceID)                              | 1                  | R   | 1                                   | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                                                    | 128                | R   | 128                                 | Sí              | None     | Sí          |
| Muestras (s \# )                                                                         | 16                 | R   | 1                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )                                              | 15                 | R   | 4                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer inmediata ( \[ Índice de ICB \] )                                     | 1                  | R   | 4                                   | Sí (contenido)   | Ninguno     | Sí          |



 

> [!Note]
> Las declaraciones del registro del punto de control de entrada (VICP) de la fase de bifurcación de casco deben ser cualquier subconjunto, a lo largo del \[ eje del elemento \] , de la entrada del punto de control del sombreador de casco (fase de punto de control previo). Del mismo modo, las declaraciones para la entrada de los puntos de control de salida (vocp) deben ser cualquier subconjunto, a lo largo del \[ eje del elemento \] , de los puntos de control de salida del sombreador de casco (fase de punto de control posterior).
> 
> A lo largo del \[ eje de vértices \] , el número de puntos de control que se van a leer para cada VICP y vocp debe ser igualmente un subconjunto del recuento de puntos de control de entrada del sombreador de casco y el recuento de puntos de control de salida del sombreador de casco, respectivamente. Por ejemplo, si el eje de vértices de los registros vocp se declaran con n vértices, hace que los puntos de control de salida de la fase de punto de control \[ 0.. n-1 \] esté disponible como entrada de solo lectura en la fase de bifurcación.

### <a name="output-registers"></a>Registros de salida



| Registrarse                                        | Count               | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Elemento de datos constante de revisión de salida de 32 bits (o \# ) | 32 véase la nota 1 a continuación | W   | 4         | Sí              | None     | Sí          |



 

> [!Note]  
> Las salidas de la bifurcación de sombreador de casco y de la fase de combinación son un conjunto compartido de registros de vector 4 4. Las salidas de cada programa de fase de bifurcación o combinación no pueden superponerse entre sí. Los valores interpretados por el sistema, como TessFactors, salen de este espacio.

## <a name="join-phase"></a>Fase de unión

Los registros siguientes están visibles en el modelo de \_ fase de combinación HS \_ . Hay tres conjuntos de registros de entrada: puntos de control de entrada de fase de punto de control (VICP), puntos de control de salida de fase de punto de control de vocp (vocp) y constantes de revisión (VCP). VPC son la salida agregada de todos los programas de la fase de bifurcación del sombreador de casco. El resultado de la fase de combinación del sombreador de casco o los \# registros se encuentran en el mismo espacio de registro que las salidas de la fase de bifurcación del sombreador de casco.

Los recursos de entrada (t \# ), los muestreadores \# , los búferes de constantes (CB \# ) y el búfer de constantes inmediatas (ICB) son todos Estados compartidos con todas las demás fases del sombreador de casco. Es decir, desde el punto de vista de la API/DDI, el sombreador de casco tiene un único conjunto de estado de recursos de entrada para todas las fases. Esto se refiere al hecho de que, desde el punto de vista de la API/DDI, el sombreador de casco es un sombreador atómico único; las fases que contiene son detalles de la implementación.

### <a name="input-registers"></a>Registros de entrada



| Tipo de registro                                                                       | Count               | L/E | Dimensión                           | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| 32-bit Temp (r \# )                                                                   | 4096 (r \# + x \# \[ n \] )  | L/E | 4                                   | No               | None     | Sí          |
| Matriz temporal Indizable de 32 bits (x \# \[ n \] )                                              | 4096 (r \# + x \# \[ n \] )  | L/E | 4                                   | Sí              | None     | Sí          |
| Puntos de control de entrada de 32 bits ( \[ elemento de vértice VICP \] \[ \] ) (fase de punto de control anterior)   | 32 véase la nota 1 a continuación | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sí              | None     | Sí          |
| Puntos de control de salida de 32 bits \[ ( \] \[ elemento \] de vértice vocp) (fase de punto de control posterior) | 32 véase la nota 1 a continuación | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sí              | None     | Sí          |
| Entrada de bit 32 ( \[ elemento VPC \] ) (datos constantes de revisión)                                 | 32 véase la nota 2 a continuación | R   | 4                                   | Sí              | None     | Sí          |
| PrimitiveID de entrada UINT de 32 bits (vPrim)                                               | 1                   | R   | 1                                   | No               | N/D      | Sí          |
| JoinInstanceID de entrada UINT de 32 bits (vJoinInstanceID)                                  | 1                   | R   | 1                                   | No               | N/D      | Sí          |
| Elemento de un recurso de entrada (t \# )                                                  | 128                 | R   | 128                                 | Sí              | None     | Sí          |
| Muestras (s \# )                                                                       | 16                  | R   | 1                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer ( \# \[ Índice CB \] )                                            | 15                  | R   | 4                                   | Sí              | None     | Sí          |
| Referencia de ConstantBuffer inmediata ( \[ Índice de ICB \] )                                   | 1                   | R   | 4                                   | Sí (contenido)   | Ninguno     | Sí          |



 

**Nota 1:** Las declaraciones del registro del punto de control de entrada (VICP) de la fase de combinación del sombreador de casco deben ser cualquier subconjunto, a lo largo del \[ eje del elemento \] , de la entrada del punto de control del sombreador de casco (fase de punto de control anterior). Del mismo modo, las declaraciones para la entrada de los puntos de control de salida (vocp) deben ser cualquier subconjunto, a lo largo del \[ eje del elemento \] , de los puntos de control de salida del sombreador de casco (fase de punto de control posterior).

A lo largo del \[ eje de vértices \] , el número de puntos de control que se van a leer para cada VICP y vocp debe ser igualmente un subconjunto del recuento de puntos de control de entrada del sombreador de casco y el recuento de puntos de control de salida del sombreador de casco, respectivamente. Por ejemplo, si el eje de vértices de los registros vocp se declaran con n vértices, hace que los puntos de control de salida de la fase de punto de control \[ 0.. n-1 \] esté disponible como entrada de solo lectura en la fase de combinación.

**Nota 2:** Además de la entrada del punto de control, la fase de unión del sombreador de casco también ve como entrada los datos constantes de la revisión calculados por los programas de la fase de bifurcación del sombreador de casco. Esto se muestra en la fase de bifurcación del sombreador de casco a medida que se registra el VPC \# . Los registros de VPC de entrada de la fase de combinación del sombreador de casco \# comparten el mismo espacio de registro que la salida de la fase de bifurcación del sombreador de casco \# . Las declaraciones de los registros o \# no deben superponerse con ninguna declaración de salida del programa o de la fase de bifurcación del sombreador de casco \# ; la fase de combinación del sombreador de casco se está agregando a la salida de datos constante de revisión agregada para el sombreador de casco.

### <a name="output-registers"></a>Registros de salida



| Tipo de registro                                   | Count             | L/E | Dimensión | Indexable por r\# | Valores predeterminados | Requiere DCL |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Elemento de datos constante de revisión de salida de 32 bits (o \# ) | 32 vea la nota siguiente | W   | 4         | Sí              | None     | Sí          |



 

> [!Note]  
> Las salidas de la bifurcación de sombreador de casco y de la fase de combinación son un conjunto compartido de registros de vector 4 4. Las salidas de cada programa de fase de bifurcación o combinación no pueden superponerse entre sí. Los valores interpretados por el sistema, como TessFactors, salen de este espacio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




