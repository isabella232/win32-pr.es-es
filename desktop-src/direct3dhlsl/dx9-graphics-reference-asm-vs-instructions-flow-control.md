---
title: Límites de anidamiento de control de flujo
description: Las instrucciones de control de flujo del sombreador de vértices tienen dos restricciones especiales.
ms.assetid: c9f80a97-8245-4974-a284-7974e2d2e504
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebb5b491e074c2275081aa3fe629a2486a24c6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780028"
---
# <a name="flow-control-nesting-limits"></a>Límites de anidamiento de control de flujo

Las instrucciones de control de flujo del sombreador de vértices tienen dos restricciones especiales. Las profundidades de anidamiento restringen el número de instrucciones que se pueden llamar dentro de otras. Además, cada instrucción tiene un recuento de ranuras de instrucciones que se aplica al número máximo de instrucciones que puede admitir un sombreador.

> [!Note]  
> Cuando se usan los \* \_ \_ perfiles del \_ \_ \_ sombreador HLSL de 4 0 nivel 9 x, se usan implícitamente los perfiles del [modelo de sombreador 2. x](dx-graphics-hlsl-sm2.md) para admitir el hardware compatible con Direct3D 9. Los perfiles del modelo de sombreador 2. x admiten un comportamiento de control de flujo más limitado que los perfiles del [modelo de sombreador 4. x](dx-graphics-hlsl-sm4.md) y posteriores.

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Recuento de profundidad por instrucción para vs \_ 2 \_ 0

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático | Anidamiento dinámico | anidamiento de bucles/REP | llamar a anidamiento | Recuento de flujos estáticos                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [Si es bool-vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [If \_ COMP-vs](if-comp---vs.md)        | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [Si Pred-vs](if-pred---vs.md)         | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [Else-vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1 ([si solo es bool-vs](if-bool---vs.md) ) |
| [endif-vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [REP-vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [bucle-vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [Inter-vs](break---vs.md)             | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [Break \_ COMP-vs](break-comp---vs.md)  | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [breakp-vs](breakp---vs.md)           | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [llamada-vs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz Pred-vs](callnz-pred---vs.md) | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [RET-vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [\_COMP SETP-vs](setp-comp---vs.md)    | N/D            | N/D             | N/D              | N/D          | N/D                                      |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar dentro de otras. Cada tipo de instrucción tiene uno o más límites de anidamiento:



| Tipo de instrucción  | Máxima                               |
|-------------------|---------------------------------------|
| Anidamiento estático    | Solo está limitado por el recuento de flujos estáticos |
| Anidamiento dinámico   | N/D                                   |
| anidamiento de bucles/REP  | 1                                     |
| llamar a anidamiento      | 1                                     |
| Recuento de flujos estáticos | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Recuento de profundidad por instrucción para vs \_ 2 \_ x

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento | Recuento de flujos estáticos                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [Si es bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [If \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [Si Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1 ([si solo es bool-vs](if-bool---vs.md) ) |
| [endif-vs](endif---vs.md)             | -1 ([si es bool-vs](if-bool---vs.md)) | -1 ([si es Pred-vs](if-pred---vs.md) o [If \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | 0                                        |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [bucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [Inter-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [Break \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | 0                                        |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [llamada-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz Pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | 0                                        |
| [\_COMP SETP-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar dentro de otras. Cada tipo de instrucción tiene uno o más límites de anidamiento:



| Tipo de instrucción  | Máxima                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| Anidamiento estático    | Solo está limitado por el recuento de flujos estáticos                                                |
| Anidamiento dinámico   | 0 o 24, vea D3DCAPS9. VS20Caps.DynamicFlowControlDepth                               |
| anidamiento de bucles/REP  | de 1 a 4, vea D3DCAPS9. VS20Caps.StaticFlowControlDepth                                 |
| llamar a anidamiento      | de 1 a 4, vea D3DCAPS9. VS20Caps. StaticFlowControlDepth (independiente del límite del bucle o REP) |
| Recuento de flujos estáticos | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Recuento de profundidad por instrucción para vs \_ 2 \_ SW

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento | Recuento de flujos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Si es bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [If \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [Si Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif-vs](endif---vs.md)             | -1 ([si es bool-vs](if-bool---vs.md)) | -1 ([si es Pred-vs](if-pred---vs.md) o [If \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [bucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [Inter-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [Break \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | N/D               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [llamada-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz Pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | N/D               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [\_COMP SETP-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar dentro de otras. Cada tipo de instrucción tiene uno o más límites de anidamiento:



| Tipo de instrucción  | Máxima  |
|-------------------|----------|
| Anidamiento estático    | 24       |
| Anidamiento dinámico   | 24       |
| anidamiento de bucles/REP  | 4        |
| llamar a anidamiento      | 4        |
| Recuento de flujos estáticos | Sin límite |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Recuento de profundidad por instrucción para vs \_ 3 \_ 0

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento | Recuento de flujos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Si es bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [If \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [Si Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif-vs](endif---vs.md)             | -1 ([si es bool-vs](if-bool---vs.md)) | -1 ([si es Pred-vs](if-pred---vs.md) o [If \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [bucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [Inter-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [Break \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | N/D               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [llamada-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz Pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | N/D               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [\_COMP SETP-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar dentro de otras. Cada tipo de instrucción tiene uno o más límites de anidamiento:



| Tipo de instrucción  | Máxima  |
|-------------------|----------|
| Anidamiento estático    | 24       |
| Anidamiento dinámico   | 24       |
| anidamiento de bucles/REP  | 4        |
| llamar a anidamiento      | 4        |
| Recuento de flujos estáticos | Sin límite |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Recuento de profundidad por instrucción para vs \_ 3 \_ SW

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento | Recuento de flujos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [Si es bool-vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [If \_ COMP-vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [Si Pred-vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [Else-vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif-vs](endif---vs.md)             | -1 ([si es bool-vs](if-bool---vs.md)) | -1 ([si es Pred-vs](if-pred---vs.md) o [If \_ COMP-vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [REP-vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep-vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [bucle-vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [ENDLOOP-vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [Inter-vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [Break \_ COMP-vs](break-comp---vs.md)  | 0                                    | 1,-1                                                                     | 0                | 0            | N/D               |
| [breakp-vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [llamada-vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz bool-vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz Pred-vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | N/D               |
| [RET-vs](ret---vs.md)                 | 0                                    | -1 ([callnz Pred-vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [\_COMP SETP-vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar dentro de otras. Cada tipo de instrucción tiene uno o más límites de anidamiento:



| Tipo de instrucción  | Máxima  |
|-------------------|----------|
| Anidamiento estático    | 24       |
| Anidamiento dinámico   | 24       |
| anidamiento de bucles/REP  | 4        |
| llamar a anidamiento      | 4        |
| Recuento de flujos estáticos | Sin límite |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




