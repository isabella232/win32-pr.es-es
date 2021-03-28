---
title: Limitaciones del control de flujo
description: Las instrucciones de control de flujo del sombreador de píxeles tienen límites que afectan al número de niveles de anidamiento que se pueden incluir en las instrucciones. Además, hay algunas limitaciones para implementar el control de flujo por píxel con instrucciones de degradado.
ms.assetid: 17a902cd-16a4-4065-9249-01f9b1f40506
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34891e29a1bb27aead629db2cc7473c7d4329af5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903882"
---
# <a name="flow-control-limitations"></a>Limitaciones del control de flujo

Las instrucciones de control de flujo del sombreador de píxeles tienen límites que afectan al número de niveles de anidamiento que se pueden incluir en las instrucciones. Además, hay algunas limitaciones para implementar el control de flujo por píxel con instrucciones de degradado.

> [!Note]  
> Cuando se usan los \* \_ \_ perfiles del \_ \_ \_ sombreador HLSL de 4 0 nivel 9 x, se usan implícitamente los perfiles del [modelo de sombreador 2. x](dx-graphics-hlsl-sm2.md) para admitir el hardware compatible con Direct3D 9. Los perfiles del modelo de sombreador 2. x admiten un comportamiento de control de flujo más limitado que los perfiles del [modelo de sombreador 4. x](dx-graphics-hlsl-sm4.md) y posteriores.

 

-   [Recuentos de profundidad de instrucciones de sombreador de píxeles](#pixel-shader-instruction-depth-counts)
-   [Interacción de control de flujo de Per-Pixel con degradados de pantalla](#interaction-of-per-pixel-flow-control-with-screen-gradients)

## <a name="pixel-shader-instruction-depth-counts"></a>Recuentos de profundidad de instrucciones de sombreador de píxeles

PS \_ 2 \_ 0 no admite el control de flujo. A continuación se enumeran las limitaciones de las demás versiones del sombreador de píxeles.

### <a name="instruction-depth-count-for-ps_2_x"></a>Recuento de profundidad de instrucciones para PS \_ 2 \_ x

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En la tabla siguiente se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si es bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Si Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si es bool-PS](if-bool---ps.md)) | -1 ([si es Pred-PS](if-pred---ps.md) o [If \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Break \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [llamada a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones a las que se puede llamar desde el interior entre sí. Cada tipo de instrucción tiene uno o más límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máxima                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| Anidamiento estático   | 24 si (D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth > 0); 0 de lo contrario            |
| Anidamiento dinámico  | de 0 a 24, vea D3DCAPS9. D3DPSHADERCAPS2 \_ 0. DynamicFlowControlDepth                          |
| representación del representante      | de 0 a 4, vea D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth                            |
| llamar a anidamiento     | de 0 a 4, vea D3DCAPS9. D3DPSHADERCAPS2 \_ 0. StaticFlowControlDepth (independiente del límite de REP) |



 

### <a name="instruction-depth-count-for-ps_2_sw"></a>Recuento de profundidad de instrucciones para el \_ SW PS 2 \_

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si es bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si es bool-PS](if-bool---ps.md)) | -1 ([si es Pred-PS](if-pred---ps.md) o [If \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [bucle-PS](loop---ps.md)               | N/D                                  | N/D                                                                       | N/D              | N/D          |
| [ENDLOOP-PS](endloop---ps.md)         | N/D                                  | N/D                                                                       | N/D              | N/D          |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Break \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [llamada a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar entre sí. Cada tipo de instrucción tiene uno o más límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máxima |
|------------------|---------|
| Anidamiento estático   | 24      |
| Anidamiento dinámico  | 24      |
| representación del representante      | 4       |
| llamar a anidamiento     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_0"></a>Recuento de profundidad de instrucciones para PS \_ 3 \_ 0

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si es bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si es bool-PS](if-bool---ps.md)) | -1 ([si es Pred-PS](if-pred---ps.md) o [If \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [bucle-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Break \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [llamada a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar entre sí. Cada tipo de instrucción tiene uno o más límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máxima |
|------------------|---------|
| Anidamiento estático   | 24      |
| Anidamiento dinámico  | 24      |
| anidamiento de bucles/REP | 4       |
| llamar a anidamiento     | 4       |



 

### <a name="instruction-depth-count-for-ps_3_sw"></a>Recuento de profundidad de instrucciones para el \_ SW PS 3 \_

Cada instrucción cuenta con uno o más límites de profundidad de anidamiento. En esta tabla se muestra el recuento de profundidad que cada instrucción agrega o resta de la profundidad existente.



| Instrucción                              | Anidamiento estático                       | Anidamiento dinámico                                                           | anidamiento de bucles/REP | llamar a anidamiento |
|------------------------------------------|--------------------------------------|---------------------------------------------------------------------------|------------------|--------------|
| [Si es bool-PS](if-bool---ps.md)         | 1                                    | 0                                                                         | 0                | 0            |
| [Si Pred-PS](if-pred---ps.md)         | 0                                    | 1                                                                         | 0                | 0            |
| [Si \_ COMP-PS](if-comp---ps.md)        | 0                                    | 1                                                                         | 0                | 0            |
| [Else-PS](else---ps.md)               | 0                                    | 0                                                                         | 0                | 0            |
| [endif-PS](endif---ps.md)             | -1 ([si es bool-PS](if-bool---ps.md)) | -1 ([si es Pred-PS](if-pred---ps.md) o [If \_ COMP-PS](if-comp---ps.md)) | 0                | 0            |
| [REP-PS](rep---ps.md)                 | 0                                    | 0                                                                         | 1                | 0            |
| [endrep-PS](endrep---ps.md)           | 0                                    | 0                                                                         | -1               | 0            |
| [bucle-PS](loop---ps.md)               | 0                                    | 0                                                                         | 1                | 0            |
| [ENDLOOP-PS](endloop---ps.md)         | 0                                    | 0                                                                         | -1               | 0            |
| [Break-PS](break---ps.md)             | 0                                    | 0                                                                         | 0                | 0            |
| [Break \_ COMP-PS](break-comp---ps.md)  | 0                                    | 1,-1                                                                     | 0                | 0            |
| [breakp-PS](break-p---ps.md)          | 0                                    | 0                                                                         | 0                | 0            |
| [llamada a PS](call---ps.md)               | 0                                    | 0                                                                         | 0                | 1            |
| [callnz bool-PS](callnz-bool---ps.md) | 0                                    | 0                                                                         | 0                | 1            |
| [callnz Pred-PS](callnz-pred---ps.md) | 0                                    | 1                                                                         | 0                | 1            |
| [RET-PS](ret---ps.md)                 | 0                                    | -1 ([callnz Pred-PS](callnz-pred---ps.md))                              | 0                | -1           |
| [SETP \_ COMP-PS](setp-comp---ps.md)    | 0                                    | 0                                                                         | 0                | 0            |



 

### <a name="nesting-depth"></a>Profundidad de anidamiento

La profundidad de anidamiento define el número de instrucciones que se pueden llamar entre sí. Cada tipo de instrucción tiene uno o más límites de anidamiento, como se indica en la tabla siguiente.



| Tipo de instrucción | Máxima |
|------------------|---------|
| Anidamiento estático   | 24      |
| Anidamiento dinámico  | 24      |
| anidamiento de bucles/REP | 4       |
| llamar a anidamiento     | 4       |



 

## <a name="interaction-of-per-pixel-flow-control-with-screen-gradients"></a>Interacción de control de flujo de Per-Pixel con degradados de pantalla

El conjunto de instrucciones del sombreador de píxeles incluye varias instrucciones que producen o utilizan degradados de cantidades con respecto al espacio de pantalla x e y. El uso más común de los degradados es calcular los cálculos de nivel de detalle para el muestreo de textura y, en el caso del filtrado anisotrópico, seleccionar muestras a lo largo del eje de anisotropía. Normalmente, las implementaciones de hardware ejecutan el sombreador de píxeles en varios píxeles simultáneamente (por ejemplo, una cuadrícula de 2x2), de modo que los degradados de cantidades calculadas en el sombreador se pueden aproximar razonablemente como deltas de los valores en el mismo punto de ejecución en píxeles adyacentes.

Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden ejecutar rutas de acceso de control de flujo independientes. Por lo tanto, se considera que no es válido usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentre dentro de una construcción de control de flujo que podría variar en píxeles para que se rasterizase un primitivo determinado.

Todas las instrucciones del sombreador de píxeles se particionan en las operaciones que se permiten y en las que no se permiten dentro del control de flujo:

-   Escenario A: operaciones no permitidas dentro del control de flujo que podrían variar en los píxeles de un primitivo. Entre ellas se incluyen las operaciones enumeradas en la tabla siguiente. 

    | Instrucción                                                                                                      | Se permite en el control de flujo cuando:                       |
    |------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) y [texldp-PS](texldp---ps.md) | Se usa un registro temporal para la coordenada de textura. |
    | [DSX-PS](dsx---ps.md) y [DSY-PS](dsy---ps.md)                                                            | Se utiliza un registro temporal para el operando.            |

    

     

-   Escenario B: operaciones que se permiten en cualquier parte. Entre ellas se incluyen las operaciones enumeradas en la tabla siguiente. 

    | Instrucción                                                                                                      | Se permite en cualquier lugar cuando:                                                                                             |
    |------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
    | [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md) y [texldp-PS](texldp---ps.md) | Se utiliza una cantidad de solo lectura para la coordenada de textura (puede variar por píxel, como las coordenadas de textura interpoladas). |
    | [DSX-PS](dsx---ps.md) y [DSY-PS](dsy---ps.md)                                                            | Se utiliza una cantidad de solo lectura para el operando de entrada (puede variar por píxel, como las coordenadas de textura interpoladas).      |
    | [texldl-PS](texldl---ps.md)                                                                                   | El usuario proporciona el nivel de detalle como argumento, por lo que no hay degradados y, por tanto, no hay ningún problema con el control de flujo.       |
    | [texldd-PS](texldd---ps.md)                                                                                   | El usuario proporciona degradados como argumentos de entrada, por lo que no hay ningún problema con el control de flujo.                                 |

    

     

Estas restricciones se aplican estrictamente en la validación del sombreador. Los escenarios que tienen una condición de bifurcación que parece que se bifurcarían de forma coherente a través de un primitivo, aunque un operando de la expresión de condición sea una cantidad calculada por el sombreador de píxeles, sin embargo, todavía se encuentra en el escenario A y no se permiten. Del mismo modo, los escenarios en los que se solicitan degradados en algunas cantidades x calculadas por el sombreador desde dentro del control de flujo dinámico, pero donde parece que x no se modifica en ninguna de las bifurcaciones, aún en el escenario A y no se permiten.

Predication se incluye en estas restricciones en el control de flujo, de modo que las implementaciones permanecen gratis para intercambiar trivialmente la implementación de instrucciones de bifurcación con instrucciones de predicado.

El usuario puede usar las instrucciones de los escenarios A y B juntos. Por ejemplo, supongamos que el usuario necesita un ejemplo de textura anisotrópico dada una coordenada de textura calculada del sombreador; sin embargo, la carga de textura solo es necesaria para los píxeles que satisfacen alguna condición por píxel. Para cumplir estos requisitos, el usuario puede calcular la coordenada de textura de todos los píxeles, fuera del control de flujo variable por píxel, calculando inmediatamente los degradados mediante las instrucciones [DSX-PS](dsx---ps.md) y [DSY-PS](dsy---ps.md) . Después, en un bloque por píxel [si es bool-PS](if-bool---ps.md) / [endif-PS](endif---ps.md) , el usuario puede usar [texldd-PS](texldd---ps.md) (carga de textura con degradados proporcionados por el usuario), pasando los degradados precalculados. Otra manera de describir este patrón de uso es que, mientras que todos los píxeles de la primitiva tenían que calcular las coordenadas de textura y estar implicado en el cálculo del degradado, solo los píxeles que necesitaban muestrear realmente la textura.

Independientemente de estas reglas, la carga sigue siendo el usuario para asegurarse de que antes de calcular el degradado (o de realizar una muestra de textura que calcula implícitamente un degradado), el registro que contiene los datos de origen debe haberse inicializado para todas las rutas de acceso de ejecución de antemano. La inicialización de registros temporales no se valida ni se aplica en general.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




