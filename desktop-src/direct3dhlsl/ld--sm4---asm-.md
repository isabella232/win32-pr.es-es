---
title: LD (SM4-ASM)
description: Recupera los datos del búfer o la textura especificados sin ningún filtrado (por ejemplo, el muestreo de puntos) mediante la dirección de entero proporcionada. Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358488"
---
# <a name="ld-sm4---asm"></a>LD (SM4-ASM)

Recupera los datos del búfer o la textura especificados sin ningún filtrado (por ejemplo, el muestreo de puntos) mediante la dirección de entero proporcionada. Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea TextureCube.



| LD \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación.<br/>                                                               |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] las coordenadas de textura necesarias para realizar el ejemplo.<br/>                                                     |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura (t \# ), que se debe haber declarado para identificar la textura o el búfer del que se va a capturar.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción es una alternativa simplificada a la instrucción de [ejemplo](sample--sm4---asm-.md) . A diferencia del **ejemplo**, **LD** también es capaz de capturar datos de búferes. **LD** también se puede recuperar de recursos de varios ejemplos (solo en el sombreador de píxeles).

*srcAddress* proporciona el conjunto de coordenadas de textura necesarias para realizar el ejemplo en forma de enteros sin signo. Si *srcAddress* está fuera del intervalo \[ 0... ( \# textura en dimensión-1) \] , se invoca el comportamiento fuera del límite, donde **LD** devuelve 0 en todos los componentes que no faltan del formato de *srcResource* y el valor predeterminado para los componentes que faltan. Una aplicación que desee tener un control más flexible sobre el comportamiento de la dirección fuera del intervalo debería usar la instrucción de **ejemplo** en su lugar, ya que respeta el comportamiento de la dirección, el reflejo, la abrazadera y el borde definidos como estado de muestra.

*srcAddress. a* (pos-swizzle) siempre proporciona un nivel de mipmap entero sin signo. Si el valor está fuera del intervalo \[ 0... ( Num miplevels in Resource-1) \] ), se invoca el comportamiento fuera de los límites. Si el recurso es un búfer, que no puede tener ningún MIP, se omite *srcAddress. a*

*srcAddress. GB* (pos-swizzle) se omite para los búferes y texture1D (no matrices). *srcAddress. b* (pos-swizzle) se omite para las matrices de Texture1D y texture2Ds.

En el caso de las matrices texture1D, *srcAddress. g* (pos-swizzle) proporciona el índice de matriz como un entero sin signo. Si el valor está fuera del intervalo de índices de matriz disponibles \[ 0... ( tamaño de matriz: 1) \] , se invoca el comportamiento fuera de los límites.

En el caso de las matrices texture2D, *srcAddress. b* (pos-swizzle) proporciona el índice de la matriz, de lo contrario con la misma semántica que para texture1D.

La captura de *t \#* que no tiene nada enlazado devuelve 0 para todos los componentes.

### <a name="address-offset"></a>Desplazamiento de dirección

El \[ \_ sufijo aoffimmi (u, v, w) opcional \] (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura para la **LD** se van a desplazar por un conjunto de valores constantes de tipo entero de espacio de textura proporcionado. Los valores literales son un conjunto de números complementarios de 4 bits 2 que tienen un intervalo \[ de enteros de 8 a 7 \] . Este modificador solo se define para texture1D/2D/3D, incluidas las matrices, y no para los búferes.

Los desplazamientos se agregan a las coordenadas de textura, en el espacio textura, con respecto a la miplevel a la que obtiene acceso el **LD**.

Los desplazamientos de direcciones no se aplican a lo largo del eje de matriz de matrices texture1D/2D.

Los componentes de *\_ aoffimmi v, w* se omiten para texture1Ds.

El componente *\_ aoffimmi w* se omite para texture2Ds.

Dado que las coordenadas de textura para **LD** son enteros sin signo, si el desplazamiento hace que la dirección pase por debajo de cero, se ajustará a una dirección grande y se producirá un acceso fuera de los límites.

### <a name="return-type-control"></a>Tipo de valor devuelto

El formato de datos que devuelve **LD** al registro de destino se determina de la misma manera que se describe para la instrucción de **ejemplo** . se basa en el formato enlazado al parámetro *srcResource* (*t \#*).

Al igual que con la instrucción de **ejemplo** , los valores devueltos para **LD** son de 4 vectores con valores predeterminados específicos del formato para los componentes que no están presentes en el formato. El swizzle en *srcResource* determina cómo swizzle el resultado de 4 componentes que se devolverá de la carga de textura, después del cual. Mask en *dest* determina qué componentes de *dest* se actualizan.

Cuando se lee un valor *float de 32 bits en un* registro de 32 bits, los bits no se tocan; es decir, los valores desnormalizados permanecen desnormalizados. Esto no es lo mismo que la instrucción de **ejemplo** .

### <a name="miscellaneous-details"></a>Detalles varios

Como no hay ningún filtrado asociado a la instrucción **LD** , los conceptos como la diferencia de LOD no se aplican a **LD**. En consecuencia, no hay *ningún \# parámetro* samples.

### <a name="restrictions"></a>Restricciones

-   *srcResource* debe ser un \# registro t y no un TextureCube. *srcResource* no puede ser constantbuffer, que no se puede enlazar a \# registros t.
-   No se permite el direccionamiento relativo en *srcResource* .
-   *srcAddress* debe ser un registro Temp (r \# /x \# ), Constant (CB \# ) o INPUT (v \# ).
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
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





