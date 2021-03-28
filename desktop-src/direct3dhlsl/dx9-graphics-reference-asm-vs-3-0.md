---
title: vs_3_0
description: Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 22a0e6e84aff34dcec44713dc4382e391ad05c2b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103904878"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Un sombreador de vértices programable se compone de un conjunto de instrucciones que operan en los datos de vértices. Registra datos de transferencia dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

La versión del sombreador de vértices frente \_ \_ a 3 0 extiende el conjunto de características compatible con vs \_ 2 \_ x. Cada una de las características de vs \_ 2 \_ X que requiere que se establezca un límite, está disponible en vs \_ 3 \_ 0 sin necesidad del Cap.

-   [Instrucciones: vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene una lista de las instrucciones disponibles.
-   [Registros: vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) muestra los distintos tipos de registros utilizados por el sombreador de vértices Alu.
-   Los [modificadores de registro del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers.md) se utilizan para modificar la forma en que funciona una instrucción.
-   Los [modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos del registro de origen antes de que se ejecute la instrucción.
-   [El registro de origen permutación](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) proporciona control adicional sobre qué componentes de registro se leen, se copian o se escriben.
-   [El enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina los componentes del registro de destino que se van a escribir.

## <a name="new-features"></a>Nuevas características

\_ \_ En las secciones siguientes se enumeran las nuevas características de la versión de sombreador de vértices frente a 3 0.

### <a name="indexing-registers"></a>Registros de indexación

En los modelos de sombreador anteriores, solo se podría indexar el Banco de registro de constantes. En este modelo, se pueden indexar los siguientes bancos de registro mediante el registro de contador de bucle (aL):

-   Registro de entrada (v \# )
-   Registro de salida (o \# )

### <a name="vertex-textures"></a>Texturas de vértices

Este modelo de sombreador admite la búsqueda de texturas en el sombreador de vértices mediante texldl. El motor de vértices tiene cuatro fases de muestra de textura (distintas de la muestra de mapa de desplazamiento y los muestreadores de textura en el motor de píxeles) que se pueden usar para muestrear las texturas establecidas en esas fases. Vea [texturas de vértices en vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0).

### <a name="vertex-stream-frequency"></a>Frecuencia de flujo de vértices

Esta característica permite inicializar un subconjunto de los registros de entrada a una velocidad distinta de una vez por cada vértice. Vea [dibujar geometría no indizada](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry).

### <a name="shader-output"></a>Salida del sombreador

Similar a vs \_ 2 \_ 0, la salida del sombreador puede variar con el control de flujo estático. Tenga cuidado con la bifurcación dinámica, ya que esto puede hacer que las salidas del sombreador varíen según el vértice. Esto producirá resultados imprevisibles en hardware diferente.

### <a name="dynamic-flow-control"></a>Control de flujo dinámico

Se admiten todas las instrucciones de control de flujo dinámico. El valor de profundidad de anidamiento máximo permitido es 24. (Vea [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para más información).

### <a name="temporary-registers"></a>Registros temporales

Se admite un total de 32 registros temporales (r \# ).

### <a name="static-flow-control"></a>Control de flujo estático

La profundidad de anidamiento máxima para el [bucle-vs](loop---vs.md) / [REP-vs](rep---vs.md) es 4. La profundidad de anidamiento máxima para [Call-vs](call---vs.md) / [callnz bool-vs](callnz-bool---vs.md) / [callnz Pred-vs](callnz-pred---vs.md) es 4. Para [Si bool-vs](if-bool---vs.md), el valor de profundidad de anidamiento máximo permitido es 24. (Vea [límites de anidamiento de control de flujo](dx9-graphics-reference-asm-vs-instructions-flow-control.md) para más información).

### <a name="predication"></a>Predicación

Se admite la instrucción predication. Use [SETP \_ COMP-vs](setp-comp---vs.md) para establecer el registro de predicado.

### <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de vértices se permite desde 512 hasta el número de ranuras de MaxVertexShader30InstructionSlots en [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). El número de instrucciones que se ejecutan puede ser mucho mayor debido a la compatibilidad con bucles o representantes; sin embargo, esto está limitado por MaxVShaderInstructionsExecuted en D3DCAPS9, que debe ser al menos 0xFFFF.

### <a name="device-caps"></a>Cap del dispositivo

Si se admite el sombreador de vértices 3 \_ 0, se admiten los siguientes límites en el hardware (como mínimo):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Punto</th>
<th>Capacidad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Límites del sombreador</td>
<td><ul>
<li>DynamicFlowControlDepth es 24</li>
<li>NumTemps es 32</li>
<li>StaticFlowControlDepth es 4</li>
<li>Se admite Predication.</li>
</ul></td>
</tr>
<tr class="even">
<td>GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom</td>
<td>8 K</td>
</tr>
<tr class="odd">
<td>VertexShaderVersion</td>
<td>3_0</td>
</tr>
<tr class="even">
<td>MaxVertexShaderConst</td>
<td>256</td>
</tr>
<tr class="odd">
<td>MaxVertexShader30InstructionSlots</td>
<td>512</td>
</tr>
<tr class="even">
<td>Compatibilidad con niebla</td>
<td>D3DPRASTERCAPS_FOGVERTEX</td>
</tr>
<tr class="odd">
<td>VertexTextureFilterCaps</td>
<td><ul>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li>
<li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a></td>
<td>Los elementos de vértice en una declaración de vértice pueden compartir el mismo desplazamiento de flujo.</td>
</tr>
<tr class="odd">
<td>Formatos de vértices</td>
<td><ul>
<li>D3DDECLTYPE_UBYTE4</li>
<li>D3DDECLTYPE_UBYTE4N</li>
<li>D3DDECLTYPE_SHORT2N</li>
<li>D3DDECLTYPE_SHORT4N</li>
<li>D3DDECLTYPE_FLOAT16_2</li>
<li>D3DDECLTYPE_FLOAT16_4</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 