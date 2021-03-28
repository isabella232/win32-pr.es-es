---
title: ps_1_1__ps_1_2__ps_1_3__ps_1_4 registros
description: Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, de salida de datos de píxeles, para conservar los resultados temporales durante los cálculos y para identificar las fases de muestreo de textura.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- Registra ps_1_1 en ps_1_4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4525b6d3be2e9287f53edc1da0cd2fb188184a69
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487874"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros

Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, de salida de datos de píxeles, para conservar los resultados temporales durante los cálculos y para identificar las fases de muestreo de textura. Hay varios tipos de registros, cada uno con una funcionalidad única. Esta sección contiene información de referencia de los registros de entrada y salida implementados por el sombreador de píxeles versión 1 \_ X.

Registra los datos de retención para su uso por parte del sombreador de píxeles. Los registros se describen por completo en las secciones siguientes.

-   Tipos de registro describe los cuatro tipos de registros disponibles y sus propósitos.
-   El límite de puertos de lectura detalla las restricciones en el uso de varios registros en una sola instrucción.
-   Lectura y escritura de solo lectura describe los registros que se pueden usar para leer, escribir o ambos.
-   Range detalla el intervalo de los datos del componente.

## <a name="register-types"></a>Tipos de registro



|      |                    | Versiones |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nombre | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro de constantes  | 8        | 8    | 8    | 8            |
| c\#  | Registro temporal | 2        | 2    | 2    | 6            |
| h\#  | Registro de textura   | 4        | 4    | 4    | 6            |
| v\#  | Registro de color     | 2        | 2    | 2    | 2 en la fase 2 |



 

-   Los registros constantes contienen datos constantes. Los datos se pueden cargar en un registro constante mediante [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) o se pueden definir mediante [Def-PS](def---ps.md). Las instrucciones de dirección de textura no pueden usar registros de constantes. La única excepción es la instrucción [texm3x3spec-PS](texm3x3spec---ps.md) , que usa un registro constante para proporcionar un vector de rayo.
-   Los registros temporales se utilizan para almacenar resultados intermedios. R0 también actúa como salida del sombreador de píxeles. El valor de R0 al final del sombreador es el color de píxel para el sombreador.

    La validación del sombreador producirá un error en [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) en cualquier sombreador que intente leer un registro temporal que no se haya escrito en una instrucción anterior. [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) producirá un error de forma similar, suponiendo que la validación está habilitada (no use D3DXSHADER \_ SKIPVALIDATION).

-   Registros de textura

    Para el sombreador de píxeles versión 1 \_ 1 a 1 \_ 3, los registros de textura contienen datos de textura o coordenadas de textura. Los datos de textura se cargan en un registro de textura cuando se muestrea una textura. El muestreo de textura usa coordenadas de textura para buscar, o muestra, un valor de color en las coordenadas especificadas (u, v, w, q), teniendo en cuenta los atributos de estado de fase de textura. Los datos de coordenadas de textura se interpolan a partir de los datos de coordenadas de textura de vértices y se asocian a una fase de textura específica. Existe una asociación uno a uno predeterminada entre el número de fase de textura y el orden de las declaraciones de coordenadas de textura. De forma predeterminada, el primer conjunto de coordenadas de textura definido en el formato de vértice está asociado a la fase de textura 0.

    Para estas versiones de sombreador de píxeles, los registros de texturas se comportan igual que los registros temporales cuando se usan en Instrucciones aritméticas.

    Para el sombreador de píxeles versión 1 \_ 4, los registros de textura (t \# ) contienen datos de coordenadas de textura de solo lectura. Esto significa que el conjunto de coordenadas de textura y el número de fase de textura son independientes entre sí. El número de fase de textura (del que se muestra una textura) viene determinado por el número de registro de destino (R0 a R5). En el caso de la instrucción texld, el conjunto de coordenadas de textura viene determinado por el registro de origen (T0 a T5), por lo que el conjunto de coordenadas de textura se puede asignar a cualquier fase de textura. Además, el registro de origen (que especifica coordenadas de textura) para texld también puede ser un registro temporal (r \# ), en cuyo caso el contenido del registro temporal se utiliza como coordenadas de textura.

-   Los registros de color contienen valores de color por píxel. Los valores se obtienen mediante la iteración por píxel de los valores de color difuso y especular en los datos de vértice. En los sombreadores de la versión 1 4 del sombreador de píxeles \_ , los registros de color solo están disponibles durante la segunda fase.

    Si el modo de sombreado se establece en D3DSHADE \_ plano, la iteración de ambos colores de vértice (difuso y especular) está deshabilitada. Independientemente del modo de sombreado, la canalización seguirá iterando la niebla si está habilitada la niebla de píxeles. Tenga en cuenta que la niebla se aplica más adelante en la canalización que la u.

    Es habitual cargar el registro V0 con los datos de color difusos de vértices. También es común cargar el registro v1 con los datos de color especular de vértice.

    Los valores de datos del color de entrada se fijan (saturan) en el intervalo comprendido entre 0 y 1 porque es el intervalo de entrada válido para los registros de color del sombreador de píxeles.

    Los sombreadores de píxeles tienen acceso de solo lectura a los registros de color. El contenido de estos registros se repite en los valores, pero la iteración se puede realizar con mucha menor precisión que las coordenadas de textura.

## <a name="read-port-limit"></a>Límite de puerto de lectura

El límite de puerto de lectura especifica el número de registros diferentes de cada tipo de registro que se puede usar como registro de origen en una única instrucción.



|      |                    | Versiones |      |      |              |
|------|--------------------|----------|------|------|--------------|
| Nombre | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4         |
| c\#  | Registro de constantes  | 2        | 2    | 2    | 2            |
| c\#  | Registro temporal | 2        | 2    | 2    | 3            |
| h\#  | Registro de textura   | 2        | 3    | 3    | 1            |
| v\#  | Registro de color     | 2        | 2    | 2    | 2 en la fase 2 |



 

Por ejemplo, los registros de color de casi todas las versiones tienen un límite de puerto de lectura de dos. Esto significa que una sola instrucción puede utilizar un máximo de dos registros de color diferentes (V0 y V1 para la instancia) como registros de origen. En este ejemplo se muestran dos registros de color que se utilizan en la misma instrucción:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Solo lectura, lectura y escritura

Los tipos de registro se identifican según la capacidad de solo lectura (RO) o la capacidad de lectura y escritura (RW) en la tabla siguiente. Los registros de solo lectura solo se pueden usar como registros de origen en una instrucción; nunca se pueden usar como un registro de destino.



|      |                    | Versiones |      |      |                    |
|------|--------------------|----------|------|------|--------------------|
| Nombre | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registro de constantes  | RO       | RO   | RO   | RO                 |
| c\#  | Registro temporal | RW       | RW   | RW   | RW                 |
| h\#  | Registro de textura   | RW       | RW   | RW   | Vea la nota siguiente |
| v\#  | Registro de color     | RO       | RO   | RO   | RO                 |



 

Los registros que son compatibles con RW se pueden usar para almacenar resultados intermedios. Esto incluye los registros temporales y los registros de textura para algunas de las versiones del sombreador.

> [!Note]  
>
> -   Para el sombreador de píxeles versión 1 \_ 4, los registros de textura se cargan para las instrucciones de direccionamiento de textura y los registros de textura no se pueden leer ni escribir en Instrucciones aritméticas. Además, dado que los registros de textura se han convertido en registros de coordenadas de textura, tener acceso de RO no es una regresión de la funcionalidad anterior.

 

## <a name="range"></a>Intervalo

El intervalo es el valor de datos de registro máximo y mínimo. Los intervalos varían en función del tipo de registro. Los intervalos de algunos de los registros se pueden consultar desde las Cap del dispositivo mediante [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).



| Nombre | Tipo               | Intervalo                                               | Versiones     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registro de constantes  | de-1 a + 1                                            | Todas las versiones |
| c\#  | Registro temporal | \- PixelShader1xMaxValue + PixelShader1xMaxValue | Todas las versiones |
| h\#  | Registro de textura   | \- MaxTextureRepeat + MaxTextureRepeat           | Todas las versiones |
| v\#  | Registro de color     | de 0 a 1                                              | Todas las versiones |



 

El hardware del sombreador de píxeles temprano representa los datos de los registros utilizando un número de punto fijo. Esto limita la precisión a un máximo de aproximadamente ocho bits para la parte fraccionaria de un número. Tenga esto en cuenta al diseñar un sombreador.

Para el sombreador de píxeles versión 1 \_ 1 a 1 \_ 3, MaxTextureRepeat debe ser un mínimo de uno. Para 1 \_ 4, MaxTextureRepeat debe tener un mínimo de ocho.

Consulte [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para obtener más información sobre PixelShader1xMaxValue.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 