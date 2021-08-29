---
title: Flow Limitaciones de control
description: Las instrucciones de control de flujo del sombreador de píxeles tienen límites que afectan al número de niveles de anidamiento que se pueden incluir en las instrucciones. Además, hay algunas limitaciones para implementar el control de flujo por píxel con instrucciones de degradado.
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b261cff11a95236e9bc6653c59c16ca0ac221ca719ade7497dbfffa2198da207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982945"
---
# <a name="flow-control-limitations"></a>Flow Limitaciones de control

Las instrucciones de control de flujo del sombreador de píxeles tienen límites que afectan al número de niveles de anidamiento que se pueden incluir en las instrucciones. Además, hay algunas limitaciones para implementar el control de flujo por píxel con instrucciones de degradado.

> [!Note]  
> Cuando se usan los perfiles de sombreador HLSL de nivel 4 0 de 9 x , se usan implícitamente los perfiles del modelo de sombreador 2.x para admitir hardware compatible con \* \_ \_ \_ \_ \_ Direct3D 9. [](dx-graphics-hlsl-sm2.md) Los perfiles del modelo de sombreador 2.x admiten un comportamiento de control de flujo más limitado que el modelo de sombreador [4.x](dx-graphics-hlsl-sm4.md) y los perfiles posteriores.

 

-   [Recuentos de profundidad de instrucciones del sombreador de píxeles](#pixel-shader-instruction-depth-counts)
-   [Interacción del control Per-Pixel Flow con degradados de pantalla](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>Recuentos de profundidad de instrucciones del sombreador de píxeles

ps \_ 2 \_ 0 no admite el control de flujo. A continuación se enumeran las limitaciones de las demás versiones del sombreador de píxeles.

### <a name="instruction-depth-count-for-ps_2_x"></a>Recuento de profundidad de instrucciones para ps \_ 2 \_ x

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En la tabla siguiente se muestra el recuento de profundidad que cada instrucción suma o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool - ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [if \_ comp : ps](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [if pred - ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [else: ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif: ps](endif---ps.md)             | -1([if bool - ps](if-bool---ps.md)) | -1([si pred - ps](if-pred---ps.md) o si comp - [ \_ ps](if-comp---ps.md)) | 0                | 0            |
| [rep - ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep - ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [break: ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [break \_ comp: ps](break-comp---ps.md)  | 0                                    | 1, -1                                                                     | 0                | 0            |
| [breakp: ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [call - ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool - ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred - ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret - ps](ret---ps.md)                 | 0                                    | -1([callnz pred - ps](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp - ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones a las que se puede llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máximo                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| Anidamiento estático   | 24 if (D3DCAPS9. D3DPSHADERCAPS2 \_ 0.StaticFlowControlDepth > 0); 0 en caso contrario            |
| Anidamiento dinámico  | De 0 a 24, consulte D3DCAPS9. D3DPSHADERCAPS2 \_ 0.DynamicFlowControlDepth                          |
| anidamiento de representantes      | De 0 a 4, consulte D3DCAPS9. D3DPSHADERCAPS2 \_ 0.StaticFlowControlDepth                            |
| anidamiento de llamadas     | De 0 a 4, consulte D3DCAPS9. D3DPSHADERCAPS2 \_ 0.StaticFlowControlDepth (independiente del límite de representantes) |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Recuento de profundidad de instrucciones para ps \_ 2 \_ sw

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción suma o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool - ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [if pred - ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [if \_ comp - ps](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else - ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif - ps](endif---ps.md)             | -1([if bool - ps](if-bool---ps.md)) | -1([si pred - ps](if-pred---ps.md) o if comp - [ \_ ps](if-comp---ps.md)) | 0                | 0            |
| [rep - ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep - ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [loop - ps](loop---ps.md)               | N/D                                  | N/D                                                                       | N/D              | N/D          |
| [endloop - ps](endloop---ps.md)         | N/D                                  | N/D                                                                       | N/D              | N/D          |
| [break- ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [break \_ comp - ps](break-comp---ps.md)  | 0                                    | 1, -1                                                                     | 0                | 0            |
| [breakp- ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [call - ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool - ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred - ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret - ps](ret---ps.md)                 | 0                                    | -1([callnz pred - ps](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp - ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones a las que se puede llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máximo |
|------------------|---------|
| Anidamiento estático   | 24      |
| Anidamiento dinámico  | 24      |
| anidamiento de representantes      | 4       |
| anidamiento de llamadas     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Recuento de profundidad de instrucciones para ps \_ 3 \_ 0

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción suma o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool - ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [if pred - ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [if \_ comp - ps](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else - ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif - ps](endif---ps.md)             | -1([if bool - ps](if-bool---ps.md)) | -1([si pred - ps](if-pred---ps.md) o if comp - [ \_ ps](if-comp---ps.md)) | 0                | 0            |
| [rep - ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep - ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [loop - ps](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [endloop- ps](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [break- ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [break \_ comp - ps](break-comp---ps.md)  | 0                                    | 1, -1                                                                     | 0                | 0            |
| [breakp- ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [call - ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool - ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred - ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret - ps](ret---ps.md)                 | 0                                    | -1([callnz pred - ps](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp - ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones a las que se puede llamar entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máximo |
|------------------|---------|
| Anidamiento estático   | 24      |
| Anidamiento dinámico  | 24      |
| anidamiento de loop/rep | 4       |
| anidamiento de llamadas     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Recuento de profundidad de instrucciones para ps \_ 3 \_ sw

Cada instrucción cuenta con uno o varios límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción suma o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de loop/rep | anidamiento de llamadas |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [if bool - ps](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [if pred - ps](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [if \_ comp - ps](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [else - ps](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif - ps](endif---ps.md)             | -1([if bool - ps](if-bool---ps.md)) | -1([si pred - ps](if-pred---ps.md) o if comp - [ \_ ps](if-comp---ps.md)) | 0                | 0            |
| [rep - ps](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep - ps](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [loop - ps](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [endloop- ps](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [break- ps](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [break \_ comp - ps](break-comp---ps.md)  | 0                                    | 1, -1                                                                     | 0                | 0            |
| [breakp- ps](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [call - ps](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool - ps](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz pred - ps](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [ret - ps](ret---ps.md)                 | 0                                    | -1([callnz pred - ps](callnz-pred---ps.md))                              | 0                | -1           |
| [setp \_ comp - ps](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones a las que se puede llamar desde dentro entre sí. Cada tipo de instrucción tiene uno o varios límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máximo |
|------------------|---------|
| Anidamiento estático   | 24      |
| Anidamiento dinámico  | 24      |
| anidamiento de loop/rep | 4       |
| anidamiento de llamadas     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Interacción del control Per-Pixel Flow con degradados de pantalla

El conjunto de instrucciones del sombreador de píxeles incluye varias instrucciones que producen o usan degradados de cantidades con respecto al espacio de pantalla x e y. El uso más común de los degradados es calcular cálculos de nivel de detalle para el muestreo de textura y, en el caso del filtrado anisotropico, seleccionar muestras a lo largo del eje de anisotropía. Normalmente, las implementaciones de hardware ejecutan el sombreador de píxeles en varios píxeles simultáneamente (por ejemplo, una cuadrícula de 2x2), de modo que los degradados de cantidades calculadas en el sombreador se puedan aproximar razonablemente como deltas de los valores en el mismo punto de ejecución en píxeles adyacentes.

Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden ejecutar rutas de control de flujo independientes. Por lo tanto, se considera que no es posible usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentra dentro de una construcción de control de flujo que podría variar en píxeles para una primitiva determinada que se está rasterizando.

Todas las instrucciones del sombreador de píxeles se particionar en las operaciones permitidas y en las que no se permiten dentro del control de flujo:

-   Escenario A: operaciones que no se permiten dentro del control de flujo que pueden variar entre los píxeles de una primitiva. Estas incluyen las operaciones enumeradas en la tabla siguiente. 

    | Instrucción                                                                                                      | Se permite en Flow control cuando:                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld - ps \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md) y [texldp - ps](texldp---ps.md) | Se usa un registro temporal para la coordenada de textura. |
    | [dsx - ps](dsx---ps.md) y [dsy - ps](dsy---ps.md)                                                            | Se usa un registro temporal para el operando.            |

    

     

-   Escenario B: operaciones permitidas en cualquier lugar. Estas incluyen las operaciones enumeradas en la tabla siguiente. 

    | Instrucción                                                                                                      | Se permite en cualquier lugar cuando:                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld - ps \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md) y [texldp - ps](texldp---ps.md) | Se usa una cantidad de solo lectura para la coordenada de textura (puede variar por píxel, como coordenadas de textura interpoladas). |
    | [dsx - ps](dsx---ps.md) y [dsy - ps](dsy---ps.md)                                                            | Se usa una cantidad de solo lectura para el operando de entrada (puede variar por píxel, como coordenadas de textura interpoladas).      |
    | [texldl: ps](texldl---ps.md)                                                                                   | El usuario proporciona nivel de detalle como argumento, por lo que no hay ningún degradado y, por tanto, no hay ningún problema con el control de flujo.       |
    | [texldd - ps](texldd---ps.md)                                                                                   | El usuario proporciona degradados como argumentos de entrada, por lo que no hay ningún problema con el control de flujo.                                 |

    

     

Estas restricciones se aplican estrictamente en la validación del sombreador. Los escenarios que tienen una condición de rama similar a la que se bifurcaría de forma coherente en una primitiva, aunque un operando de la expresión de condición es una cantidad calculada por sombreador de píxeles, no obstante, siguen estando en el escenario A y no se permiten. Del mismo modo, los escenarios en los que se solicitan degradados en alguna cantidad calculada por sombreador x desde dentro del control de flujo dinámico, pero donde parece que x no se modifica en ninguna de las ramas, no obstante, siguen estando en el escenario A y no se permiten.

La predicación se incluye en estas restricciones en el control de flujo, por lo que las implementaciones permanecen libres para intercambiar trivialmente la implementación de instrucciones de rama con instrucciones predicadas.

El usuario puede usar instrucciones de los escenarios A y B juntos. Por ejemplo, suponga que el usuario necesita una muestra de textura anisotrófica dada una coordenada de textura calculada del sombreador. sin embargo, la carga de textura solo es necesaria para los píxeles que cumplen alguna condición por píxel. Para cumplir estos requisitos, el usuario puede calcular la coordenada de textura de todos los píxeles, fuera del control de flujo variable por píxel, calculando inmediatamente los degradados mediante [instrucciones dsx - ps](dsx---ps.md) y [dsy - ps.](dsy---ps.md) A continuación, dentro de un bloque [bool - ps](if-bool---ps.md)endif - ps por píxel, el usuario puede usar texldd - ps (carga de textura con degradados proporcionados por el usuario), pasando los / [](endif---ps.md) degradados precalculados. [](texldd---ps.md) Otra manera de describir este patrón de uso es que, mientras que todos los píxeles de la primitiva tenían que calcular las coordenadas de textura y participar en el cálculo de degradado, solo lo hacían los píxeles necesarios para muestrear una textura.

Independientemente de estas reglas, la carga sigue siendo del usuario para asegurarse de que antes de calcular cualquier degradado (o realizar una muestra de textura que calcule implícitamente un degradado), el registro que contiene los datos de origen se debe haber inicializado con antelación para todas las rutas de ejecución. La inicialización de registros temporales no se valida ni se aplica en general.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




