---
title: ejemplo (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | ejemplo (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003655"
---
# <a name="sample-sm4---asm"></a>ejemplo (SM4-ASM)

Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.



| ejemplo \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] un conjunto de coordenadas de textura. Para más información, vea la sección **Comentarios**.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura. Para más información, vea la sección **Comentarios**.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra. Para más información, vea la sección **Comentarios**.<br/>           |



 

## <a name="remarks"></a>Observaciones

Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea de búferes.

*srcAddress* proporciona el conjunto de coordenadas de textura necesarias para realizar el ejemplo, como valores de punto flotante que hacen referencia al espacio normalizado en la textura. Los modos de ajuste de direcciones (Wrap/Mirror/Clamp/Border, etc.) se aplican a las coordenadas de textura fuera del \[ intervalo 0... 1 \] , se toman de los Estados de muestra \# y se aplican después de que se aplique cualquier desplazamiento de dirección a las coordenadas de textura.

*srcResource* es un registro de textura (t \# ). Esto es simplemente un marcador de posición para una textura, incluido el tipo de datos devuelto del recurso que se muestra. Toda esta información se declara en el preámbulo del sombreador. El recurso real que se va a muestrear se enlaza al sombreador externamente en la ranura \# (para t \# ).

*srcSampler* es un registro de muestra. Esto es simplemente un marcador de posición para una colección de controles de filtrado, como los controles de punto frente a lineal, mipmapping y ajuste de direcciones.

El conjunto de información necesario para que el hardware realice el muestreo se divide en dos partes ortogonales. En primer lugar, el registro de textura proporciona información de tipo de datos de origen, como por ejemplo, información sobre si la textura contiene datos SRGB. También hace referencia a la memoria real que se muestra. En segundo lugar, el registro de muestra define el modo de filtrado que se va a aplicar.

### <a name="array-resources"></a>Recursos de matriz

En el caso de las matrices Texture1D, el componente *srcAddress* g (pos-swizzle) selecciona en qué segmento de la matriz se va a capturar. Siempre se trata como un valor de punto flotante escalado, en lugar del espacio normalizado para las coordenadas de textura estándar, y se aplica una operación de ida a vuelta más cercana al valor, seguida de una abrazadera al intervalo de BufferArray disponible.

En el caso de las matrices de Texture2D, el componente b de *srcAddress* (pos-swizzle) selecciona el segmento de matriz del que se va a capturar; de lo contrario, se usa la misma semántica descrita para las matrices de Texture1D.

### <a name="address-offset"></a>Desplazamiento de dirección

El \[ \_ sufijo aoffimmi (u, v, w) opcional \] (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura para el ejemplo se van a desplazar por un conjunto de valores de constantes de tipo entero de espacio de textura inmediato proporcionado. Los valores literales son un conjunto de números complementarios de 4 bits 2 que tienen un intervalo \[ de enteros de 8 a 7 \] . Este modificador se define para todos los recursos, incluidas las matrices Texture1D/2D y Texture3D, pero no está definido para TextureCube.

El hardware puede aprovechar el conocimiento inmediato de que un recorrido de una determinada superficie de textura sobre una ubicación común se realiza mediante un conjunto de instrucciones de ejemplo. Esto se puede transmitir mediante \_ aoffimmi (u, v, w).

Los desplazamientos se agregan a las coordenadas de textura, en el espacio textura, con respecto a cada miplevel al que se tiene acceso. Por lo tanto, aunque las coordenadas de textura se proporcionan como valores Float normalizados, el desplazamiento aplica un desplazamiento de entero de espacio textura.

Los desplazamientos de direcciones no se aplican a lo largo del eje de matriz de matrices Texture1D/2D.

\_los componentes de aoffimmi v, w se omiten para Texture1Ds.

\_el componente aoffimmi w se omite para Texture2Ds.

Los modos de ajuste de direcciones (Wrap, Mirror, Clamp/Border, etc.) de los Estados de muestra \# se aplican después de que se aplique cualquier desplazamiento de dirección a las coordenadas de textura.

### <a name="return-type-control"></a>Tipo de valor devuelto

El formato de los datos que devuelve el ejemplo al registro de destino viene determinado por el formato de recursos (formato de DXGI \_ \* ) enlazado al parámetro *srcResource* (t \# ). Por ejemplo, si el t especificado \# estaba enlazado con un recurso con el formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, la operación de muestreo convertirá el textura muestreado de gamma 2,0 a 1,0, aplicará el filtrado y el resultado se escribirá en el registro de destino como valores de punto flotante en el intervalo \[ 0.. 1 \] .

Los valores devueltos son los vectores 4 (con valores predeterminados específicos del formato para los componentes que no están presentes en el formato). El swizzle en *srcResource* determina cómo swizzle el resultado de 4 componentes que se devolverá del ejemplo de textura o filtro, después del cual. Mask en *dest* determina qué componentes de *dest* se actualizan.

Cuando **Sample** Lee un valor float de 32 bits en un registro de 32 bits, con muestreo de punto (sin filtrado), puede o no vaciar los valores desnormalizados, pero de lo contrario no se modifican los números. Si la incertidumbre con valores desnormalizados de muestreo de puntos es un problema para una aplicación, use la instrucción [LD](ld--sm4---asm-.md) , que garantiza que los valores float de 32 bits se lean sin modificar.

### <a name="lod-calculation"></a>Cálculo de LOD

Para obtener información detallada sobre cómo se calculan los derivados en el proceso de determinación de LOD para el filtrado, vea [derive \_ RTX](deriv-rtx--sm4---asm-.md) y [derive \_ propiedad](deriv-rty--sm4---asm-.md). La instrucción de **ejemplo** calcula implícitamente los derivados de las coordenadas de textura usando la misma definición que usan las instrucciones de sombreador **derivadas** . Esto no se aplica a las instrucciones de [ejemplo \_ l](sample-l--sm4---asm-.md) o [ \_ d](sample-d--sm4---asm-.md) . En el caso de estas instrucciones, la aplicación proporciona directamente el LOD o los derivados.

En el caso de la instrucción de **ejemplo** , las implementaciones pueden optar por compartir el mismo cálculo de LOD en los 4 píxeles de una marca de 2x2 (pero sin área más grande) o realizar cálculos de LOD por píxel.

### <a name="miscellaneous-details"></a>Detalles varios

Para buffer & Texture1D, se omiten los componentes *srcAddress* . GBA (pos-swizzle). En el caso de las matrices Texture1D, se omiten los componentes de *srcAddress* . BA (pos-swizzle). En el caso de Texture2Ds, se omite el componente *srcAddress* . a (pos-swizzle).

La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.

### <a name="restrictions"></a>Restricciones

-   *srcResource* debe ser un \# registro t. *srcResource* no puede ser ConstantBuffer, que no se puede enlazar a \# registros t.
-   *srcSampler* debe ser un \# registro s.
-   No se permite el direccionamiento relativo en *srcResource* o *srcSampler* .
-   *srcAddress* debe ser un registro Temp (r \# /X \# ), constantBuffer (CB \# ), INPUT (v \# ) o un valor inmediato (s).
-   *dest* debe ser un registro Temp (r \# /x \# ) o Output (o \* \# ).
-   \_aoffimmi (u, v, w) no se permite para TextureCubes.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





