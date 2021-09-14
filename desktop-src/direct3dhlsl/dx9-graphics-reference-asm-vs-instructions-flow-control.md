---
title: Flow Límites de anidamiento de controles
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974685"
---
# <a name="flow-control-nesting-limits"></a>Flow Límites de anidamiento de controles

Las instrucciones de control de flujo del sombreador de vértices tienen dos restricciones especiales. Las profundidades de anidamiento restringen el número de instrucciones a las que se puede llamar entre sí. Además, cada instrucción tiene un recuento de ranuras de instrucciones que se aplica al número máximo de instrucciones que un sombreador puede admitir.

> [!Note]  
> Cuando se usan los perfiles de sombreador HLSL de 4 0 nivel 0 x, se usan implícitamente los perfiles del modelo de sombreador 2.x para admitir hardware compatible con \* \_ \_ \_ \_ \_ Direct3D 9. [](dx-graphics-hlsl-sm2.md) Los perfiles del modelo de sombreador 2.x admiten un comportamiento de control de flujo más limitado que el modelo de sombreador [4.x](dx-graphics-hlsl-sm4.md) y los perfiles posteriores.

 

## <a name="depth-count-per-instruction-for-vs_2_0"></a>Recuento de profundidad por instrucción para frente \_ a 2 \_ 0

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático | Anidamiento dinámico | anidamiento de loop/rep | anidamiento de llamadas | Recuento de flujos estáticos                        |
|------------------------------------------|----------------|-----------------|------------------|--------------|------------------------------------------|
| [if bool - vs](if-bool---vs.md)         | 0              | 0               | 0                | 0            | 1                                        |
| [if \_ comp - vs](if-comp---vs.md)        | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [if pred - vs](if-pred---vs.md)         | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [else - vs](else---vs.md)               | 0              | 0               | 0                | 0            | 1([if bool - vs](if-bool---vs.md) only) |
| [endif- vs](endif---vs.md)             | -1             | 0               | 0                | 0            | 0                                        |
| [rep- vs](rep---vs.md)                 | 0              | 0               | 1                | 0            | 1                                        |
| [endrep- vs](endrep---vs.md)           | 0              | 0               | -1               | 0            | 0                                        |
| [loop: vs](loop---vs.md)               | 0              | 0               | 1                | 0            | 1                                        |
| [endloop- vs](endloop---vs.md)         | 0              | 0               | -1               | 0            | 0                                        |
| [break- vs](break---vs.md)             | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [break \_ comp - vs](break-comp---vs.md)  | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [breakp- vs](breakp---vs.md)           | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [call - vs](call---vs.md)               | 0              | 0               | 0                | 1            | 1                                        |
| [callnz bool - vs](callnz-bool---vs.md) | 0              | 0               | 0                | 1            | 1                                        |
| [callnz pred - vs](callnz-pred---vs.md) | N/D            | N/D             | N/D              | N/D          | N/D                                      |
| [ret - vs](ret---vs.md)                 | 0              | 0               | 0                | -1           | 0                                        |
| [setp \_ comp - vs](setp-comp---vs.md)    | N/D            | N/D             | N/D              | N/D          | N/D                                      |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define cuántas instrucciones se pueden llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento:



| Tipo de instrucción  | Máxima                               |
|-------------------|---------------------------------------|
| Anidamiento estático    | Solo limitado por el recuento de flujos estáticos |
| Anidamiento dinámico   | N/D                                   |
| anidamiento de loop/rep  | 1                                     |
| anidamiento de llamadas      | 1                                     |
| Recuento de flujos estáticos | 16                                    |



 

## <a name="depth-count-per-instruction-for-vs_2_x"></a>Recuento de profundidad por instrucción para frente \_ a 2 \_ x

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción suma o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas | Recuento de flujos estáticos                        |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|------------------------------------------|
| [if bool - vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | 1                                        |
| [if \_ comp - vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [if pred - vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | 0                                        |
| [else - vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | 1([if bool - vs](if-bool---vs.md) only) |
| [endif- vs](endif---vs.md)             | -1([if bool - vs](if-bool---vs.md)) | -1([si pred - vs](if-pred---vs.md) o if comp - [ \_ vs](if-comp---vs.md)) | 0                | 0            | 0                                        |
| [rep - vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endrep - vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [loop - vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | 1                                        |
| [endloop- vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | 0                                        |
| [break- vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [break \_ comp - vs](break-comp---vs.md)  | 0                                    | 1, -1                                                                     | 0                | 0            | 0                                        |
| [breakp- vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | 0                                        |
| [call - vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz bool - vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | 1                                        |
| [callnz pred - vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | 0                                        |
| [ret - vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred - vs](callnz-pred---vs.md))                             | 0                | -1           | 0                                        |
| [setp \_ comp - vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | 0                                        |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define cuántas instrucciones se pueden llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento:



| Tipo de instrucción  | Máxima                                                                              |
|-------------------|--------------------------------------------------------------------------------------|
| Anidamiento estático    | Solo limitado por el recuento de flujos estáticos                                                |
| Anidamiento dinámico   | 0 o 24, consulte D3DCAPS9. VS20Caps.DynamicFlowControlDepth                               |
| anidamiento de loop/rep  | De 1 a 4, consulte D3DCAPS9. VS20Caps.StaticFlowControlDepth                                 |
| anidamiento de llamadas      | De 1 a 4, consulte D3DCAPS9. VS20Caps.StaticFlowControlDepth (independiente del límite de bucles y réplicas) |
| Recuento de flujos estáticos | 16                                                                                   |



 

## <a name="depth-count-per-instruction-for-vs_2_sw"></a>Recuento de profundidad por instrucción para vs \_ 2 \_ sw

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas | Recuento de flujos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [if bool - vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [if \_ comp - vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [if pred - vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [else - vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif- vs](endif---vs.md)             | -1([if bool - vs](if-bool---vs.md)) | -1([si pred - vs](if-pred---vs.md) o if comp - [ \_ vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [rep- vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep- vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [loop: vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endloop- vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [break- vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [break \_ comp - vs](break-comp---vs.md)  | 0                                    | 1, -1                                                                     | 0                | 0            | N/D               |
| [breakp- vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [call - vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz bool - vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz pred - vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | N/D               |
| [ret - vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred - vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [setp \_ comp - vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define cuántas instrucciones se pueden llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento:



| Tipo de instrucción  | Máxima  |
|-------------------|----------|
| Anidamiento estático    | 24       |
| Anidamiento dinámico   | 24       |
| anidamiento de loop/rep  | 4        |
| anidamiento de llamadas      | 4        |
| Recuento de flujos estáticos | Sin límite |



 

## <a name="depth-count-per-instruction-for-vs_3_0"></a>Recuento de profundidad por instrucción para frente \_ a 3 \_ 0

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas | Recuento de flujos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [if bool - vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [if \_ comp - vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [if pred - vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [else - vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif- vs](endif---vs.md)             | -1([if bool - vs](if-bool---vs.md)) | -1([si pred - vs](if-pred---vs.md) o if comp - [ \_ vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [rep - vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep - vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [loop - vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endloop- vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [break- vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [break \_ comp: vs](break-comp---vs.md)  | 0                                    | 1, -1                                                                     | 0                | 0            | N/D               |
| [breakp: vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [call - vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz bool- vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz pred - vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | N/D               |
| [ret - vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred - vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [setp \_ comp - vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define cuántas instrucciones se pueden llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento:



| Tipo de instrucción  | Máxima  |
|-------------------|----------|
| Anidamiento estático    | 24       |
| Anidamiento dinámico   | 24       |
| anidamiento de loop/rep  | 4        |
| anidamiento de llamadas      | 4        |
| Recuento de flujos estáticos | Sin límite |



 

## <a name="depth-count-per-instruction-for-vs_3_sw"></a>Recuento de profundidad por instrucción para vs \_ 3 \_ sw

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente:



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas | Recuento de flujos estáticos |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|-------------------|
| [if bool - vs](if-bool---vs.md)         | 1                                    | 0                                                                         | 0                | 0            | N/D               |
| [if \_ comp - vs](if-comp---vs.md)        | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [if pred - vs](if-pred---vs.md)         | 0                                    | 1                                                                         | 0                | 0            | N/D               |
| [else - vs](else---vs.md)               | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [endif- vs](endif---vs.md)             | -1([if bool - vs](if-bool---vs.md)) | -1([si pred - vs](if-pred---vs.md) o if comp - [ \_ vs](if-comp---vs.md)) | 0                | 0            | N/D               |
| [rep- vs](rep---vs.md)                 | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endrep- vs](endrep---vs.md)           | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [loop: vs](loop---vs.md)               | 0                                    | 0                                                                         | 1                | 0            | N/D               |
| [endloop- vs](endloop---vs.md)         | 0                                    | 0                                                                         | -1               | 0            | N/D               |
| [break- vs](break---vs.md)             | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [break \_ comp - vs](break-comp---vs.md)  | 0                                    | 1, -1                                                                     | 0                | 0            | N/D               |
| [breakp- vs](breakp---vs.md)           | 0                                    | 0                                                                         | 0                | 0            | N/D               |
| [call - vs](call---vs.md)               | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz bool - vs](callnz-bool---vs.md) | 0                                    | 0                                                                         | 0                | 1            | N/D               |
| [callnz pred - vs](callnz-pred---vs.md) | 0                                    | 1                                                                         | 0                | 1            | N/D               |
| [ret - vs](ret---vs.md)                 | 0                                    | -1 ([callnz pred - vs](callnz-pred---vs.md))                             | 0                | -1           | N/D               |
| [setp \_ comp - vs](setp-comp---vs.md)    | 0                                    | 0                                                                         | 0                | 0            | N/D               |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define cuántas instrucciones se pueden llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento:



| Tipo de instrucción  | Máxima  |
|-------------------|----------|
| Anidamiento estático    | 24       |
| Anidamiento dinámico   | 24       |
| anidamiento de loop/rep  | 4        |
| anidamiento de llamadas      | 4        |
| Recuento de flujos estáticos | Sin límite |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




