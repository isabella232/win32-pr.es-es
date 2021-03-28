---
title: ld2dms (SM 4.1-ASM)
description: Lee ejemplos individuales de texturas de varios ejemplos bidimensionales.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148997"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (SM 4.1-ASM)

Lee ejemplos individuales de texturas de varios ejemplos bidimensionales.



| ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] las coordenadas de textura necesarias para realizar el ejemplo.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura (t \# ), que se debe haber declarado que identifica la textura o el búfer del que se va a capturar<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[en \] Idendifies los ejemplos que se van a leer desde *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

Esta instrucción es una alternativa simplificada a la instrucción de [ejemplo](sample--sm4---asm-.md) . Captura los datos de la textura especificada sin ningún filtro (por ejemplo, el muestreo de puntos) mediante el entero proporcionado *srcAddress* y *sampleIndex*.

*srcAddress* proporciona el conjunto de coordenadas de textura necesarias para realizar el ejemplo en forma de enteros sin signo. Si *srcAddress* está fuera del intervalo \[ 0... ( \# textura en Dimension-1) \] , **ld2dms** siempre devuelve 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados (0, 0, 0, 1.0 f/0x00000001) para los componentes que faltan.

*sampleIndex* no tiene que ser un literal. No es necesario especificar el número de muestras múltiples en el recurso de textura y funciona con vistas de profundidad o de estarcido.

Una aplicación que desee tener un control más flexible sobre el comportamiento de la dirección fuera del intervalo debería usar la instrucción de **ejemplo** en su lugar, ya que respeta el comportamiento de la dirección, el reflejo, la abrazadera y el borde definidos como estado de muestra.

*srcAddress. b* (post-swizzle) se omite para Texture2Ds. Si el valor está fuera del intervalo de índices de matriz disponibles \[ 0... ( tamaño de matriz: 1) \] , **ld2dms** siempre devuelve 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados (0, 0, 0, 1.0 f/0x00000001) para los componentes que faltan.

En el caso de las matrices Texture2D, *srcAddress. b* (post-swizzle) proporciona el índice de la matriz. Oherwise tiene el mismo comportamiento que Texture2D.

*srcAddress. a* (post-swizzle) siempre se omite. El compilador de HLSL nunca generará nada.

*srcResource* es un registro de textura (t \# ) que se debe haber declarado (22.3.11), que identifica la textura de la que se va a capturar.

La captura de t \# que no tiene nada enlazado devuelve 0 para todos los componentes.

### <a name="address-offset"></a>Desplazamiento de dirección

El \[ \_ sufijo aoffimmi (u, v, w) opcional \] (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura de **ld2dms** se van a desplazar mediante un conjunto de valores de constante de entero de espacio textura inmediato proporcionado. Los valores literales son un conjunto de números complementarios de 4 bits 2 que tienen un intervalo \[ de enteros de 8 a 7 \] .

Los desplazamientos se agregan a las coordenadas de textura, en el espacio textura.

Los desplazamientos de direcciones no se aplican a lo largo del eje de matriz de matrices Texture1D/2D.

Los componentes de *\_ aoffimmi v, w* se omiten para Texture1Ds.

El componente *\_ aoffimmi w* se omite para Texture2Ds.

Dado que las coordenadas de textura para **ld2dms** son enteros sin signo, si el desplazamiento hace que la dirección quede por debajo de cero, se ajustará a una dirección grande y se producirá un acceso fuera del límite, que es como **LD** devuelve 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados (0, 0, 0, 1,0 f/0x00000001) para los componentes

### <a name="sample-number"></a>Número de muestra

**ld2dms** está disponible para su uso en cualquier recurso. **ld2dms** funciona de forma idéntica a **LD** , excepto en los recursos de multsample 2D, mediante el uso del operando de *sampleIndex* adicional (basado en 0) para identificar qué ejemplo se debe leer del recurso.

El resultado de especificar un *sampleIndex* que supera el número de muestras del recurso es indefinido, pero no puede devolver datos fuera del espacio de direcciones del contexto del dispositivo.

### <a name="return-type-control"></a>Tipo de valor devuelto

El formato de datos devuelto por **ld2dms** al registro de destino se determina de la misma manera que se describe para la instrucción de **ejemplo** . Se basa en el formato enlazado al parámetro *srcResource* (t \# ).

Al igual que con la instrucción de **ejemplo** , los valores devueltos para **ld2dms** son de 4 vectores con valores predeterminados específicos del formato para los componentes que no están presentes en el formato. El swizzle en *srcResource* determina cómo swizzle el resultado de 4 componentes que se devolverá de la carga de textura, después del cual. Mask en *dest* determina qué componentes de *dest* se actualizan.

Cuando **ld2dms** Lee un valor float de 32 bits en un registro de 32 bits, los bits no se tocan; es decir, los valores desnormalizados permanecen desnormalizados. Esto no es lo mismo que la instrucción de **ejemplo** .

### <a name="miscellaneous-details"></a>Detalles varios

Como no hay ningún filtrado asociado a esta instrucción, no se aplican conceptos como la diferencia de LOD. En consecuencia, no hay ningún parámetro *Samples \#* .

### <a name="restrictions"></a>Restricciones

-   *srcResource* debe ser un \# registro t y no un TextureCube, Texture1D o Texture1DArray. *srcResource* no puede ser ConstantBuffer, que no se puede enlazar a \# registros t.
-   No se permite el direccionamiento relativo en *srcResource* .
-   *srcAddress* y *sampleIndex* deben ser un registro Temp (r \# /x \# ), Constant (CB \# ) o INPUT (v \# ).
-   *dest* debe ser un registro Temp (r \# /x \# ) o Output (o \* \# ).

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





