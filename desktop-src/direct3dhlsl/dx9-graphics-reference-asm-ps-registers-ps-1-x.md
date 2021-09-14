---
title: ps_1_1__ps_1_2__ps_1_3__ps_1_4 registros
description: Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, generar datos de píxeles, contener resultados temporales durante los cálculos e identificar fases de muestreo de textura.
ms.assetid: ca25a030-b4da-4893-b9f3-e3bb12f18d83
keywords:
- 'Registros: ps_1_1 para ps_1_4'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 68e3645c3e634c4e9cd886600977882dcc3e2018
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263959"
---
# <a name="ps_1_1__ps_1_2__ps_1_3__ps_1_4-registers"></a>ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers

Los sombreadores de píxeles dependen de los registros para obtener datos de vértices, generar datos de píxeles, contener resultados temporales durante los cálculos e identificar fases de muestreo de textura. Hay varios tipos de registros, cada uno con una funcionalidad única. Esta sección contiene información de referencia para los registros de entrada y salida implementados por el sombreador de píxeles versión 1 \_ X.

Los registros mantienen los datos para que los use el sombreador de píxeles. Los registros se describen por completo en las secciones siguientes.

-   Tipos de registro describe los cuatro tipos de registros disponibles y sus propósitos.
-   Lea El límite de puertos detalla las restricciones sobre el uso de varios registros en una sola instrucción.
-   Read only Read Write (Lectura de solo lectura) describe qué registros se pueden usar para leer, escribir o ambos.
-   El intervalo detalla el intervalo de los datos del componente.

## <a name="register-types"></a>Registrar tipos



| Nombre |  Tipo              | Versión 1 \_ 1 | Versión 1 \_ 2      | Versión 1 \_ 3     | Versión 1 \_ 4             |
|------|--------------------|----------|------|------|--------------|
| c\#  | Registro constante  | 8        | 8    | 8    | 8            |
| R\#  | Registro temporal | 2        | 2    | 2    | 6            |
| t\#  | Registro de textura   | 4        | 4    | 4    | 6            |
| V\#  | Registro de color     | 2        | 2    | 2    | 2 en la fase 2 |



 

-   Los registros constantes contienen datos constantes. Los datos se pueden cargar en un registro constante mediante [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) o se pueden definir [mediante def - ps](def---ps.md). Los registros constantes no son utilizables mediante instrucciones de dirección de textura. La única excepción es [la instrucción texm3x3spec - ps,](texm3x3spec---ps.md) que usa un registro constante para proporcionar un vector de rayos oculares.
-   Los registros temporales se usan para almacenar resultados intermedios. r0 sirve además como salida del sombreador de píxeles. El valor de r0 al final del sombreador es el color de píxel del sombreador.

    Se producirá un error en la validación del [**sombreador CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) en cualquier sombreador que intente leer desde un registro temporal que no haya sido escrito por una instrucción anterior. [**D3DXAssembleShader producirá**](/windows/desktop/direct3d9/d3dxassembleshader) un error similar, suponiendo que la validación esté habilitada (no use D3DXSHADER \_ SKIPVALIDATION).

-   Registros de textura

    En el caso del sombreador de píxeles \_ versión 1 1 a 1 3, los registros de textura contienen datos de textura \_ o coordenadas de textura. Los datos de textura se cargan en un registro de textura cuando se muestrea una textura. El muestreo de textura usa coordenadas de textura para buscar, o muestrear, un valor de color en las coordenadas especificadas (u,v,w,q) teniendo en cuenta los atributos de estado de la fase de textura. Los datos de coordenadas de textura se interpolan a partir de los datos de coordenadas de textura de vértice y se asocian a una fase de textura específica. Hay una asociación uno a uno predeterminada entre el número de fase de textura y el orden de declaración de coordenadas de textura. De forma predeterminada, el primer conjunto de coordenadas de textura definido en el formato de vértice está asociado a la fase de textura 0.

    Para estas versiones del sombreador de píxeles, los registros de textura se comportan igual que los registros temporales cuando se usan mediante instrucciones aritméticas.

    Para la versión 1 4 del sombreador de píxeles, los registros \_ de textura (t) contienen datos de coordenadas de textura de solo \# lectura. Esto significa que el conjunto de coordenadas de textura y el número de fase de textura son independientes entre sí. El número de fase de textura (del que se muestrea una textura) viene determinado por el número de registro de destino (de r0 a r5). Para la instrucción texld, el conjunto de coordenadas de textura viene determinado por el registro de origen (t0 a t5), por lo que el conjunto de coordenadas de textura se puede asignar a cualquier fase de textura. Además, el registro de origen (especificando coordenadas de textura) para texld también puede ser un registro temporal (r ), en cuyo caso el contenido del registro temporal se usa como coordenadas de \# textura.

-   Los registros de color contienen valores de color por píxel. Los valores se obtienen mediante la iteración por píxel de los valores de color difuso y especular en los datos del vértice. En el caso de los sombreadores de la versión 1 4 del sombreador de píxeles, los registros \_ de color solo están disponibles durante la segunda fase.

    Si el modo de sombreado se establece en D3DSHADE FLAT, la iteración de ambos colores de vértice (difuso y \_ especular) está deshabilitada. Independientemente del modo de sombreado, la canalización seguirá iterada por la canalización si está habilitada la matriz de píxeles. Tenga en cuenta que la sombra se aplica más adelante en la canalización que el efecto pixelshader.

    Es habitual cargar el registro v0 con los datos de color difuso del vértice. También es habitual cargar el registro v1 con los datos de color especular de vértice.

    Los valores de datos de color de entrada están unidos (saturados) al intervalo de 0 a 1 porque este es el intervalo de entrada válido para los registros de color en el sombreador de píxeles.

    Los sombreadores de píxeles tienen acceso de solo lectura a los registros de color. El contenido de estos registros son valores iterados, pero la iteración se puede realizar con una precisión mucho menor que las coordenadas de textura.

## <a name="read-port-limit"></a>Leer límite de puertos

El límite de puerto de lectura especifica el número de registros diferentes de cada tipo de registro que se pueden usar como registro de origen en una sola instrucción.



| Nombre     | Tipo                   | Versión 1 \_ 1 | Versión 1 \_ 2      | Versión 1 \_ 3     | Versión 1 \_ 4             |
|------|--------------------|----------|------|------|--------------|
| c\#  | Registro constante  | 2        | 2    | 2    | 2            |
| R\#  | Registro temporal | 2        | 2    | 2    | 3            |
| t\#  | Registro de textura   | 2        | 3    | 3    | 1            |
| V\#  | Registro de color     | 2        | 2    | 2    | 2 en la fase 2 |



 

Por ejemplo, los registros de color para casi todas las versiones tienen un límite de puerto de lectura de dos. Esto significa que una sola instrucción puede usar un máximo de dos registros de color diferentes (v0 y v1, por ejemplo) como registros de origen. En este ejemplo se muestran dos registros de color que se usan en la misma instrucción:


```
mad r0, v1, c2, v0
```



## <a name="read-only-readwrite"></a>Solo lectura, lectura y escritura

Los tipos de registro se identifican según la funcionalidad de solo lectura (RO) o la funcionalidad de lectura y escritura (RW) de la tabla siguiente. Los registros de solo lectura solo se pueden usar como registros de origen en una instrucción; nunca se pueden usar como registro de destino.



| Nombre     |  Tipo                  | Versión 1 \_ 1 | Versión 1 \_ 2     | Versión 1 \_ 3     | Versión 1 \_ 4 |
|------|--------------------|----------|------|------|--------------------|
| Nombre | Tipo               | 1\_1     | 1\_2 | 1 \_ 3 | 1\_4               |
| c\#  | Registro constante  | RO       | RO   | RO   | RO                 |
| R\#  | Registro temporal | RW       | RW   | RW   | RW                 |
| t\#  | Registro de textura   | RW       | RW   | RW   | Consulte la nota siguiente. |
| V\#  | Registro de color     | RO       | RO   | RO   | RO                 |



 

Los registros que son compatibles con RW se pueden usar para almacenar resultados intermedios. Esto incluye los registros temporales y los registros de textura para algunas de las versiones del sombreador.

> [!Note]  
>
> -   Para la versión 1 4 del sombreador de píxeles, los registros de textura son RO para las instrucciones de direccionamiento de textura y los registros de textura no se pueden leer ni escribir en mediante instrucciones \_ aritméticas. Además, dado que los registros de textura se han convertido en registros de coordenadas de textura, tener acceso a RO no es una regresión de la funcionalidad anterior.

 

## <a name="range"></a>Intervalo

El intervalo es el valor de datos de registro máximo y mínimo. Los intervalos varían en función del tipo de registro. Los intervalos de algunos de los registros se pueden consultar desde los límites del dispositivo mediante [**GetDeviceCaps.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps)



| Nombre | Tipo               | Intervalo                                               | Versiones     |
|------|--------------------|-----------------------------------------------------|--------------|
| c\#  | Registro constante  | -1 a +1                                            | Todas las versiones |
| R\#  | Registro temporal | \- PixelShader1xMaxValue a + PixelShader1xMaxValue | Todas las versiones |
| t\#  | Registro de textura   | \- MaxTextureRepeat a + MaxTextureRepeat           | Todas las versiones |
| V\#  | Registro de color     | De 0 a 1                                              | Todas las versiones |



 

El hardware del sombreador de píxeles temprano representa los datos de los registros mediante un número de punto fijo. Esto limita la precisión a un máximo de aproximadamente ocho bits para la parte fraccionera de un número. Tenga esto en cuenta al diseñar un sombreador.

Para el sombreador de píxeles versión \_ 1 1 \_ a 1 3, MaxTextureRepeat debe ser un mínimo de uno. Para 1 \_ 4, MaxTextureRepeat debe ser un mínimo de ocho.

Consulte [**D3DCAPS9 para**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) obtener más información sobre PixelShader1xMaxValue.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 
