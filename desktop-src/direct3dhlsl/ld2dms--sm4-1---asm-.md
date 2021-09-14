---
title: ld2dms (sm4.1 - asm)
description: Lee muestras individuales de texturas de 2 muestras multidimensionales.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964636"
---
# <a name="ld2dms-sm41---asm"></a>ld2dms (sm4.1 - asm)

Lee muestras individuales de texturas de 2 muestras multidimensionales.



| ld2dms \[ \_ aoffimmi(u,v) \] dest \[ .mask \] , srcAddress \[ .swdexle, \] srcResource \[ .swlinole \] , sampleIndex (operando escalar) |
|------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección del resultado de la operación. <br/>                                                                 |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Las coordenadas de textura necesarias para realizar el ejemplo.<br/>                                                    |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en Un registro de textura (t ) que se debe haber declarado identificando qué textura o búfer se \] \# va a capturar de<br/> |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[en \] Idendifies los ejemplos para leer de *srcResource*.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

Esta instrucción es una alternativa simplificada a la [instrucción de](sample--sm4---asm-.md) ejemplo. Captura datos de la textura especificada sin ningún filtrado (por ejemplo, muestreo de punto) mediante los enteros *srcAddress* y *sampleIndex proporcionados.*

*srcAddress proporciona* el conjunto de coordenadas de textura necesarias para realizar el ejemplo en forma de enteros sin signo. Si *srcAddress* está fuera del intervalo \[ 0...( \# Los elementos de textura de la dimensión -1), ld2dms siempre devuelven 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados \] (0,0,0,1.0f/0x00000001) para los componentes que faltan. 

*sampleIndex* no tiene que ser un literal. El recuento de varias muestras no tiene que especificarse en el recurso de textura y funciona con vistas de profundidad o galería de símbolos.

Una aplicación que quiera un control más flexible sobre  el comportamiento de las direcciones fuera del intervalo debe usar la instrucción de ejemplo en su lugar, ya que respeta el comportamiento de encapsulado de direcciones, reflejo, fijación o borde definido como estado del muestreador.

*srcAddress.b* (post-swconfle) se omite para Texture2Ds. Si el valor está fuera del intervalo de índices de matriz disponibles \[ 0...( array size-1) , then \] **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components( 0,0,0,1.0f/0x00000001) for missing components ( 0,0,0,1.0f/0x00000001) for missing components (0,0,0,1.0f/0x00000001) for missing components (0,0,0,1.0f/0x00000001) for missing components (0,0,0,1.0f/

En el caso de las matrices Texture2D, *srcAddress.b* (post-swconfle) proporciona el índice de la matriz. Tiene el mismo comportamiento que Texture2D.

*srcAddress.a* (posterior a swconfle) siempre se omite. El compilador HLSL nunca mostrará nada allí.

*srcResource es* un registro de textura (t ) que se debe haber declarado \# (22.3.11), que identifica de qué textura se va a capturar.

Al capturar desde t \# que no tiene nada enlazado, se devuelve 0 para todos los componentes.

### <a name="address-offset"></a>Desplazamiento de dirección

El sufijo \[ \_ opcional aoffimmi(u,v,w) (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura de \] los **ld2dm se** van a desplazar por un conjunto de valores constantes enteros de espacio de texel inmediato proporcionados. Los valores literales son un conjunto de números de complemento de 4 bits 2, con un intervalo entero \[ de -8,7. \]

Los desplazamientos se agregan a las coordenadas de textura, en el espacio de textura.

Los desplazamientos de dirección no se aplican a lo largo del eje de matriz de matrices Texture1D/2D.

Los *\_ componentes aoffimmi v,w* se omiten para Texture1Ds.

El *\_ componente aoffimmi w* se omite para Texture2Ds.

Dado que las coordenadas de textura para **ld2dms** son enteros sin signo, si el desplazamiento hace que la dirección sea inferior a cero, se ajustará a una dirección grande y dará como resultado un acceso fuera de límites, que como **ld** devuelve 0 en todos los componentes presentes en el formato del recurso, y los valores predeterminados (0,0,0,1,0f/0x00000001) para los componentes que faltan.

### <a name="sample-number"></a>Número de ejemplo

**ld2dms** está disponible para su uso en cualquier recurso. **ld2dms** funciona de forma idéntica a **ld,** excepto en recursos multsample 2D, mediante el operando *sampleIndex* adicional (basado en 0) para identificar qué muestra se va a leer del recurso.

El resultado de especificar un *sampleIndex* que supera el número de muestras del recurso es indefinido, pero no puede devolver datos fuera del espacio de direcciones del contexto del dispositivo.

### <a name="return-type-control"></a>Return Type (Control)

El formato de datos devuelto por **ld2dms** al registro de destino se determina de la misma manera que se describe para la **instrucción de** ejemplo. Se basa en el formato enlazado al *parámetro srcResource* (t \# ).

Al igual que con **la instrucción** de ejemplo, los valores devueltos para **ld2dms** son 4 vectores con valores predeterminados específicos del formato para los componentes que no están presentes en el formato. El swzzle en *srcResource* determina cómo deslizar el resultado de 4 componentes que vuelve de la carga de textura, después de lo cual .mask on *dest* determina qué componentes de *dest* se actualizan.

Cuando **ld2dms** lee un valor float de 32 bits en un registro de 32 bits, los bits no se tocan; Es decir, los valores desnormales siguen siendo desnormales. Esto es diferente de la **instrucción de** ejemplo.

### <a name="miscellaneous-details"></a>Detalles varios

Como no hay ningún filtrado asociado a esta instrucción, no se aplican conceptos como el sesgo de LOD. Por consiguiente, no hay ningún *parámetro de \# sampler.*

### <a name="restrictions"></a>Restricciones

-   *srcResource debe* ser un registro t \# y no un objeto TextureCube, Texture1D o Texture1DArray. *srcResource* no puede ser ConstantBuffer, que no se puede enlazar a registros \# t.
-   No se permite el direccionamiento relativo en *srcResource.*
-   *srcAddress* y *sampleIndex* deben ser un registro temp (r \# \# /x), constante (cb) o entrada \# \# (v).
-   *dest* debe ser un registro temporal (r \# /x) o de salida \# \* (o). \#

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





