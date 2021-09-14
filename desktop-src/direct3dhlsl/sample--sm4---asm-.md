---
title: sample (sm4 - asm)
description: Muestrea los datos del elemento o textura especificados mediante la dirección especificada y el modo de filtrado identificado por el muestreador especificado. | sample (sm4 - asm)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240824"
---
# <a name="sample-sm4---asm"></a>sample (sm4 - asm)

Muestrea los datos del elemento o textura especificados mediante la dirección especificada y el modo de filtrado identificado por el muestreador especificado.



| sample \[ \_ aoffimmi(u,v,w) \] dest \[ .mask \] , srcAddress \[ .swzzle, \] srcResource \[ .swzzle \] , srcSampler |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección del resultado de la operación.<br/>                                      |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Un conjunto de coordenadas de textura. Para más información, vea la sección **Comentarios**.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de textura. Para más información, vea la sección **Comentarios**.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler. Para más información, vea la sección **Comentarios**.<br/>           |



 

## <a name="remarks"></a>Observaciones

Los datos de origen pueden proceden de cualquier tipo de recurso, que no sea Búferes.

*srcAddress proporciona* el conjunto de coordenadas de textura necesarias para realizar el ejemplo, como valores de punto flotante que hacen referencia al espacio normalizado en la textura. Los modos de ajuste de direcciones (encapsulado, reflejo, fijación, borde, etc.) se aplican a las coordenadas de textura fuera del intervalo 0...1, tomados del estado del muestreador (s) y aplicados después de aplicar cualquier desplazamiento de dirección a las coordenadas de \[ \] \# textura.

*srcResource es* un registro de textura (t \# ). Se trata simplemente de un marcador de posición para una textura, incluido el tipo de datos devuelto del recurso que se muestrea. Toda esta información se declara en el preámbulo Sombreador. El recurso real que se va a muestrear está enlazado al sombreador externamente en la ranura \# (para t \# ).

*srcSampler es* un registro (s) de muestreador. Se trata simplemente de un marcador de posición para una colección de controles de filtrado, como controles de ajuste de punto frente a lineales, mipmapping y de ajuste de direcciones.

El conjunto de información necesaria para que el hardware realice el muestreo se divide en dos partes ortogonales. En primer lugar, el registro de textura proporciona información de tipo de datos de origen que incluye, por ejemplo, información sobre si la textura contiene datos SRGB. También hace referencia a la memoria real que se muestrea. En segundo lugar, el registro de sampler define el modo de filtrado que se aplicará.

### <a name="array-resources"></a>Recursos de matriz

Para matrices Texture1D, el componente *srcAddress* g (POS-swzzle) selecciona de qué segmento de matriz se va a capturar. Esto siempre se trata como un valor float escalado, en lugar del espacio normalizado para las coordenadas de textura estándar, y se aplica una operación de ida y vuelta a la más cercana incluso en el valor, seguida de una fijación al intervalo BufferArray disponible.

En el caso de las matrices Texture2D, el componente *srcAddress* b (POS-swzzle) selecciona de qué segmento de matriz se va a capturar; de lo contrario, usa la misma semántica descrita para matrices Texture1D.

### <a name="address-offset"></a>Desplazamiento de dirección

El sufijo \[ \_ opcional aoffimmi(u,v,w) (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura de la muestra se van a desplazar por un conjunto de valores constantes enteros de espacio de textura inmediato \] proporcionados. Los valores literales son un conjunto de números de complemento de 4 bits 2, con un intervalo entero \[ de -8,7 \] . Este modificador se define para todos los recursos, incluidas las matrices Texture1D/2D y Texture3D, pero no está definido para TextureCube.

El hardware puede aprovechar el conocimiento inmediato de que un recorrido sobre alguna superficie de texturas sobre una ubicación común se realiza mediante un conjunto de instrucciones de ejemplo. Esto se puede transmitir mediante \_ aoffimmi(u,v,w).

Los desplazamientos se agregan a las coordenadas de textura, en el espacio de textura, en relación con cada miplevel al que se accede. Por lo tanto, aunque las coordenadas de textura se proporcionan como valores float normalizados, el desplazamiento aplica un desplazamiento entero de espacio de texel.

Los desplazamientos de dirección no se aplican a lo largo del eje de matriz de matrices Texture1D/2D.

\_Los componentes aoffimmi v,w se omiten para Texture1D.

\_El componente aoffimmi w se omite para Texture2Ds.

Los modos de ajuste de direcciones (encapsulado, reflejo, fijación, borde, etc.) del estado del muestreador (s) se aplican después de aplicar cualquier desplazamiento de dirección a las coordenadas \# de textura.

### <a name="return-type-control"></a>Return Type (Control)

El formato de datos devuelto por el ejemplo al registro de destino viene determinado por el formato de recurso (DXGI FORMAT) enlazado al \_ \* parámetro *srcResource* (t \# ). Por ejemplo, si el t especificado se enlazaba con un recurso con formato \# DXGI \_ FORMAT A8B8G8R8 UNORM SRGB, la operación de muestreo convertirá los elementos de textura muestreados de \_ \_ gamma 2.0 a 1.0, aplicará el filtrado y el resultado se escribirá en el registro de destino como valores de punto flotante en el intervalo \_ \[ 0..1. \]

Los valores devueltos son 4 vectores (con valores predeterminados específicos del formato para los componentes que no están presentes en el formato). El swzzle en *srcResource* determina cómo deslizar el resultado de 4 componentes procedente de la muestra o filtro de textura, después de lo cual .mask en *dest* determina qué componentes *de dest* se actualizan.

Cuando  el ejemplo lee un valor float de 32 bits en un registro de 32 bits, con muestreo de punto (sin filtrado), puede o no vaciar valores desnormales, pero, de lo contrario, los números no se modificarán. Si la incertidumbre con los valores desnormales de muestreo de punto es un problema para una aplicación, use la instrucción [ld,](ld--sm4---asm-.md) que garantiza que los valores float de 32 bits se leen sin modificar.

### <a name="lod-calculation"></a>Cálculo de LOD

Para obtener más información sobre cómo se calculan los derivados en el proceso de determinar el LOD para el filtrado, vea [deriv \_ rtx](deriv-rtx--sm4---asm-.md) y [deriv \_ rty](deriv-rty--sm4---asm-.md). La **instrucción** de ejemplo calcula implícitamente derivados de las coordenadas de textura con la misma definición que usan las instrucciones **del sombreador** de derivación. Esto no se aplica a las [instrucciones \_ de ejemplo l](sample-l--sm4---asm-.md) o [ \_ d.](sample-d--sm4---asm-.md) Para esas instrucciones, la aplicación proporciona directamente loD o derivados.

Para  la instrucción de ejemplo, las implementaciones pueden optar por compartir el mismo cálculo de LOD en los 4 píxeles de una marca de 2x2 (pero sin área mayor) o realizar cálculos de LOD por píxel.

### <a name="miscellaneous-details"></a>Detalles varios

Para buffer & Texture1D, se omiten los componentes .gba de *srcAddress* (POS-swzzle). En el caso de las matrices Texture1D, se omiten los componentes .ba de *srcAddress* (POS-swzzle). Para Texture2Ds, se omite el componente *srcAddress* .a (POS-swzzle).

Al capturar desde una ranura de entrada que no tiene nada enlazado, se devuelve 0 para todos los componentes.

### <a name="restrictions"></a>Restricciones

-   *srcResource debe* ser un registro \# t. *srcResource* no puede ser ConstantBuffer, que no se puede enlazar a registros \# t.
-   *srcSampler* debe ser un registro \# s.
-   No se permite el direccionamiento relativo en *srcResource* o *srcSampler.*
-   *srcAddress* debe ser un registro temporal (r \# \# /x), constantBuffer (cb), \# entrada \# (v) o valores inmediatos.
-   *dest* debe ser un registro temporal (r \# \# /x) o de salida (o). \* \#
-   \_no se permite aoffimmi(u,v,w) para TextureCubes.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





