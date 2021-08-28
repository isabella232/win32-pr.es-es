---
title: vs_3_0
description: Obtenga información vs_3_0, un sombreador de vértices programable, que se forma de un conjunto de instrucciones que funcionan con datos de vértices.
ms.assetid: 0f40f946-3525-4203-bfe2-1cd941d8e2ec
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd10f6d726118679f395f01714233c7096fd5189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476421"
---
# <a name="vs_3_0"></a>vs \_ 3 \_ 0

Un sombreador de vértices programable se forma de un conjunto de instrucciones que funcionan con datos de vértices. Registra la transferencia de datos dentro y fuera de la ALU. Se puede aplicar un control adicional para modificar la instrucción, los resultados o los datos que se escriben.

La versión del sombreador de \_ \_ vértices frente a 3 0 amplía el conjunto de características admitido por frente \_ a 2 \_ x. Cada una de las características de frente a 2 X que requiere que se establezca un límite, está disponible en frente \_ \_ a \_ 3 0 sin necesidad del \_ límite.

-   [Instrucciones: frente \_ a \_ 3 0](dx9-graphics-reference-asm-vs-instructions-vs-3-0.md) contiene una lista de las instrucciones disponibles.
-   [Registros: frente \_ a 3 \_ 0,](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) se enumeran los distintos tipos de registros usados por el sombreador de vértices ALU.
-   [Los modificadores de registro del sombreador](dx9-graphics-reference-asm-vs-registers-modifiers.md) de vértices se usan para modificar el funcionamiento de una instrucción.
-   [Los modificadores de registro de origen del sombreador de vértices](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifican los datos de registro de origen antes de que se ejecute la instrucción.
-   [Source Register Swling proporciona](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) control adicional sobre qué componentes de registro se leen, copian o escriben.
-   [El enmascaramiento de registros de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determina qué componentes del registro de destino se escriben.

## <a name="new-features"></a>Nuevas características

Las nuevas características de la versión del sombreador de vértices frente \_ a \_ 3 0 se enumeran en las secciones siguientes.

### <a name="indexing-registers"></a>Indexación de registros

En los modelos de sombreador anteriores, solo se podía indexar el banco de registros constante. En este modelo, se pueden indexar los siguientes bancos de registro mediante el registro de contador de bucles (aL):

-   Registro de entrada (v \# )
-   Registro de salida (o \# )

### <a name="vertex-textures"></a>Texturas de vértice

Este modelo de sombreador admite la búsqueda de textura en el sombreador de vértices mediante texldl. El motor de vértices tiene cuatro fases del muestreador de textura (distintas del muestreador del mapa de desplazamiento y los muestreadores de textura en el motor de píxeles) que se pueden usar para muestrear texturas establecidas en esas fases. Vea [Texturas de vértice en vs \_ 3 \_ 0 (DirectX HLSL).](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)

### <a name="vertex-stream-frequency"></a>Frecuencia de flujo de vértices

Esta característica permite inicializar un subconjunto de los registros de entrada a una velocidad diferente de una vez por vértice. Vea [Dibujar geometría no indizada.](/windows/desktop/direct3d9/efficiently-drawing-multiple-instances-of-geometry)

### <a name="shader-output"></a>Salida del sombreador

De forma similar a \_ 2 \_ 0, la salida del sombreador puede variar con el control de flujo estático. Tenga cuidado con la bifurcación dinámica, ya que esto puede hacer que las salidas del sombreador varían por vértice. Esto producirá resultados impredecibles en hardware diferente.

### <a name="dynamic-flow-control"></a>Control de flujo dinámico

Se admiten todas las instrucciones de control de flujo dinámico. El valor máximo de profundidad de anidamiento permitido es 24. (Vea [Flow límites de anidamiento de controles para](dx9-graphics-reference-asm-vs-instructions-flow-control.md) obtener más información).

### <a name="temporary-registers"></a>Registros temporales

Se admite un total de 32 registros temporales (r \# ).

### <a name="static-flow-control"></a>Static Flow Control

La profundidad de anidamiento máxima del [bucle (frente](loop---vs.md) / [a rep) frente](rep---vs.md) a 4. La profundidad de anidamiento máxima para [la llamada ( vs](call---vs.md) / [callnz bool - vs](callnz-bool---vs.md) / [callnz pred ) vs](callnz-pred---vs.md) es 4. Para [if bool - vs](if-bool---vs.md), el valor máximo de profundidad de anidamiento permitido es 24. (Vea [Flow límites de anidamiento de controles para](dx9-graphics-reference-asm-vs-instructions-flow-control.md) obtener más información).

### <a name="predication"></a>Predicación

Se admite el predicado de instrucciones. Use [setp \_ comp - vs para](setp-comp---vs.md) establecer el registro de predicado.

### <a name="instruction-count"></a>Recuento de instrucciones

Cada sombreador de vértices se permite desde 512 hasta el número de ranuras de MaxVertexShader30InstructionSlots en [**D3DCAPS9.**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) El número de instrucciones que se ejecutan puede ser mucho mayor debido a la compatibilidad con bucles o representantes. sin embargo, MaxVShaderInstructionsExecuted en D3DCAPS9, que debe ser al menos 0xFFFF.

### <a name="device-caps"></a>Límites de dispositivo

Si se admite Sombreador de vértices 3 0, se admiten los siguientes límites en \_ el hardware (como mínimo):




| Tapa | Capacidad | 
|-----|------------|
| Límites de sombreador | <ul><li>DynamicFlowControlDepth es 24</li><li>NumTemps es 32</li><li>StaticFlowControlDepth es 4</li><li>Se admite la predicado.</li></ul> | 
| GuardBandLeft, GuardBandTop, GuardBandRight, GuardBandBottom | 8 K | 
| VertexShaderVersion | 3_0 | 
| MaxVertexShaderConst | 256 | 
| MaxVertexShader30InstructionSlots | 512 | 
| Compatibilidad con la nube | D3DPRASTERCAPS_FOGVERTEX | 
| VertexTextureFilterCaps | <ul><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MINFPOINT</a></li><li><a href="/windows/desktop/direct3d9/d3dptfiltercaps">D3DPTFILTERCAPS_MAGFPOINT</a></li></ul> | 
| <a href="/windows/desktop/direct3d9/d3ddevcaps2">D3DDEVCAPS2_VERTEXELEMENTSCANSHARESTREAMOFFSET</a> | Los elementos de vértice de una declaración de vértice pueden compartir el mismo desplazamiento de flujo. | 
| Formatos de vértice | <ul><li>D3DDECLTYPE_UBYTE4</li><li>D3DDECLTYPE_UBYTE4N</li><li>D3DDECLTYPE_SHORT2N</li><li>D3DDECLTYPE_SHORT4N</li><li>D3DDECLTYPE_FLOAT16_2</li><li>D3DDECLTYPE_FLOAT16_4</li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de vértices](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 
