---
title: Especificación de firmas de raíz en HLSL
description: Especificar firmas raíz en el modelo de sombreador de HLSL 5,1 es una alternativa a especificarlas en código de C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549073"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Especificación de firmas de raíz en HLSL

Especificar firmas raíz en el modelo de sombreador de HLSL 5,1 es una alternativa a especificarlas en código de C++.

-   [Una firma raíz HLSL de ejemplo](#an-example-hlsl-root-signature)
    -   [Versión de firma raíz 1,0](#root-signature-version-10)
    -   [Versión de firma raíz 1,1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Constantes raíz](#root-constants)
-   [Visibilidad](#visibility)
-   [CBV de nivel de raíz](#root-level-cbv)
-   [SRV de nivel de raíz](#root-level-srv)
-   [UAV de nivel de raíz](#root-level-uav)
-   [Tabla de descriptores](#descriptor-table)
-   [Muestra estática](#static-sampler)
-   [Compilar una firma raíz HLSL](#compiling-an-hlsl-root-signature)
-   [Manipular firmas raíz con el compilador FXC](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Notas](#notes)
-   [Temas relacionados](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Una firma raíz HLSL de ejemplo

Se puede especificar una firma raíz en HLSL como una cadena. La cadena contiene una colección de cláusulas separadas por comas que describen los componentes constituyentes de la firma raíz. La firma raíz debe ser idéntica en los distintos sombreadores de cualquier objeto de estado de canalización (PSO). Este es un ejemplo:

### <a name="root-signature-version-10"></a>Versión de firma raíz 1,0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

### <a name="root-signature-version-11"></a>Versión de firma raíz 1,1

La [versión 1,1 de la firma raíz](root-signature-version-1-1.md) habilita las optimizaciones del controlador en los datos y los descriptores de la firma raíz.

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Esta definición proporcionaría la siguiente firma raíz:

-   El uso de parámetros predeterminados.
-   B0 y (b0, Space = 1) no entran en conflicto
-   U0 solo es visible para el sombreador de geometría
-   U4 y U5 tienen un alias en el mismo descriptor de un montón

![una firma raíz especificada mediante el lenguaje de sombreador de alto nivel](images/hlsl-root-signature.png)

El lenguaje de firma raíz de HLSL se corresponde estrechamente con las API de firma raíz de C++ y tiene una potencia expresiva equivalente. La firma raíz se especifica como una secuencia de cláusulas, separadas por comas. El orden de las cláusulas es importante, ya que el orden de análisis determina la posición de la ranura en la firma raíz. Cada cláusula toma uno o varios parámetros con nombre. Sin embargo, el orden de los parámetros no es importante.

## <a name="rootflags"></a>RootFlags

La cláusula *RootFlags* opcional toma 0 (el valor predeterminado para indicar que no hay marcas) o uno o varios valores de marcas de raíz predefinidos, conectados mediante el \| operador o ' '. Los valores de marca de raíz permitidos se definen mediante [**\_ \_ \_ marcas de firma raíz de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Por ejemplo:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Constantes raíz

La cláusula *RootConstants* especifica las constantes raíz en la firma raíz. Dos parámetros obligatorios son: *num32BitConstants* y *bReg* (el registro correspondiente a *BaseShaderRegister* en las API de C++) de *CBuffer*. Los parámetros Space (*RegisterSpace* en las API de c++) y Visibility (*ShaderVisibility* en c++) son opcionales y los valores predeterminados son:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Por ejemplo:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Visibilidad

Visibility es un parámetro opcional que puede tener uno de los valores de [**la \_ \_ visibilidad del sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

\_La visibilidad del sombreador \_ difunde los argumentos raíz a todos los sombreadores. En algunos equipos, esto no tiene ningún costo, pero en otro hardware hay un costo para bifurcar los datos a todas las fases del sombreador. La configuración de una de las opciones, como \_ el vértice de visibilidad del sombreador \_ , limita el argumento raíz a una sola etapa del sombreador.

Establecer los argumentos raíz en fases del sombreador único permite usar el mismo nombre de enlace en diferentes fases. Por ejemplo, un enlace SRV de `t0,SHADER_VISIBILITY_VERTEX` y el enlace SRV de `t0,SHADER_VISIBILITY_PIXEL` serían válidos. Pero si la configuración de visibilidad era `t0,SHADER_VISIBILITY_ALL` para uno de los enlaces, la signatura raíz no sería válida.

## <a name="root-level-cbv"></a>CBV de nivel de raíz

La `CBV` cláusula (vista de búfer de constantes) especifica una entrada de registro del búfer de constantes de nivel de raíz. Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV de nivel de raíz

La `SRV` cláusula (vista de recursos del sombreador) especifica una entrada de registro de registro t-Register SRV de nivel de raíz. Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV de nivel de raíz

La `UAV` cláusula (vista de acceso desordenado) especifica una entrada de registro de UAV u-Register reg de nivel de raíz. Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Por ejemplo:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Tabla de descriptores

La `DescriptorTable` cláusula es en sí misma una lista de cláusulas de tabla de descriptores separadas por comas, así como un parámetro de visibilidad opcional. Las cláusulas *DescriptorTable* incluyen CBV, SRV, UAV y muestreador. Tenga en cuenta que sus parámetros difieren de los de las cláusulas de nivel de raíz.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

La tabla de descriptores `CBV` tiene la siguiente sintaxis:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Por ejemplo:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

El parámetro obligatorio *bReg* especifica el REG de inicio del intervalo de CBuffer. El parámetro *numDescriptors* especifica el número de descriptores en el intervalo de CBuffer contiguo; el valor predeterminado es 1. La entrada declara un intervalo CBuffer ` [Reg, Reg + numDescriptors - 1]` , cuando *numDescriptors* es un número. Si *numDescriptors* es igual a "unbounded", el intervalo es `[Reg, UINT_MAX]` , lo que significa que la aplicación debe asegurarse de que no hace referencia a un área fuera de los límites. El campo *offset* representa el parámetro *OffsetInDescriptorsFromTableStart* en las API de C++, es decir, el desplazamiento (en descriptores) desde el inicio de la tabla. Si el desplazamiento se establece en descriptor de \_ desplazamiento de intervalo \_ \_ Append (el valor predeterminado), significa que el intervalo está justo después del intervalo anterior. Sin embargo, la especificación de desplazamientos específicos permite que los intervalos se superpongan entre sí, lo que permite el alias del registro.

La tabla de descriptores `SRV` tiene la siguiente sintaxis:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Esto es similar a la entrada de la tabla de descriptores `CBV` , salvo que el intervalo especificado es para las vistas de recursos del sombreador.

La tabla de descriptores `UAV` tiene la siguiente sintaxis:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Esto es similar a la entrada de la tabla de descriptores `CBV` , salvo que el intervalo especificado es para las vistas de acceso desordenado.

La tabla de descriptores `Sampler` tiene la siguiente sintaxis:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Esto es similar a la entrada de la tabla de descriptores `CBV` , salvo que el intervalo especificado es para los muestreadores de sombreador. Tenga en cuenta que los muestreadores no se pueden combinar con otros tipos de descriptores en la misma tabla de descriptores (ya que se encuentran en un montón descriptor independiente).

## <a name="static-sampler"></a>Muestra estática

La muestra estática representa la estructura DESC de la [**\_ \_ muestra \_ estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) . El parámetro obligatorio para *StaticSampler* es un valor escalar de muestra s-Register reg. Otros parámetros son opcionales con los valores predeterminados que se muestran a continuación. La mayoría de los campos aceptan un conjunto de enumeraciones predefinidas.

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

Por ejemplo:

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

Las opciones de parámetro son muy similares a las llamadas de la API de C++, a excepción de *BorderColor*, que está restringida a una enumeración en HLSL.

El campo de filtro puede ser uno de [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).

Los campos de dirección pueden ser uno de [**los \_ \_ \_ modos de dirección de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

La función de comparación puede ser una de [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).

El campo de color del borde puede ser [**un \_ \_ \_ color de borde estático de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

La visibilidad puede ser una de las D3D12 de la [**\_ \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

## <a name="compiling-an-hlsl-root-signature"></a>Compilar una firma raíz HLSL

Hay dos mecanismos para compilar una firma raíz de HLSL. En primer lugar, es posible adjuntar una cadena de firma raíz a un sombreador determinado a través del atributo *RootSignature* (en el ejemplo siguiente, mediante el punto de entrada **MyRS1** ):

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

El compilador creará y comprobará el BLOB de firma raíz para el sombreador y lo incrustará junto con el código de byte del sombreador en el BLOB de sombreador. El compilador admite la sintaxis de firma raíz para el modelo de sombreador 5,0 y versiones posteriores. Si una firma raíz está incrustada en un sombreador modelo de sombreador 5,0 y ese sombreador se envía al tiempo de ejecución de D3D11, en lugar de D3D12, la parte de la firma raíz se omitirá de forma silenciosa por D3D11.

El otro mecanismo consiste en crear un BLOB de firma raíz independiente, quizás para reutilizarlo con un gran conjunto de sombreadores, lo que ahorra espacio. La [herramienta de compilador de efectos](/windows/desktop/direct3dtools/fxc) (FXC) admite los modelos de sombreador **rootsig \_ 1 \_ 0** y **rootsig \_ 1 \_ 1** . El nombre de la cadena de definición se especifica mediante el argumento/E habitual. Por ejemplo:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Tenga en cuenta que la definición de la cadena de firma raíz también se puede pasar en la línea de comandos, por ejemplo,/D MyRS1 = "...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Manipular firmas raíz con el compilador FXC

El compilador FXC crea el código de bytes del sombreador desde los archivos de código fuente HLSL. Hay muchos parámetros opcionales para este compilador, consulte la herramienta de [compilador de efectos](/windows/desktop/direct3dtools/fxc).

Para administrar las firmas de raíz creadas por HLSL, en la tabla siguiente se proporcionan algunos ejemplos del uso de FXC.



| Línea | Línea de comandos                                                                 | Descripción                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Compila un sombreador para el destino del sombreador de píxeles 5,1, el origen del sombreador se encuentra en el archivo shaderWithRootSig. HLSL, que incluye una firma raíz. El sombreador y la firma raíz se compilan como Blobs independientes en el archivo binario RS1. FXO.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Extrae la firma raíz del archivo creado por la línea 1, por lo que el archivo RS1. RS. FXO contiene solo una firma raíz.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Quita la firma raíz del archivo creado por la línea 1, por lo que el archivo RS1. unsumed. FXO contiene un sombreador sin firma raíz.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Combina un sombreador y una firma raíz que se encuentran en archivos independientes en un archivo binario que contiene ambos BLOBs. En este ejemplo, RS1. New. FX0 sería idéntico a RS1. FX0 en la línea 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Crea un archivo binario de firma raíz independiente a partir de un origen que puede contener más de una firma raíz. Observe el \_ \_ destino de rootsig 1 0 y que RS1 es el nombre de la cadena de macro de la firma raíz ( \# define) en el archivo HLSL. |



 

La funcionalidad disponible a través de FXC también está disponible mediante programación con la función [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) . Esta llamada compila un sombreador con una firma raíz o una firma raíz independiente (estableciendo el \_ destino rootsig 1 \_ 0). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) y [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) pueden extraer y adjuntar firmas raíz a un BLOB existente.\_La firma de raíz de blobs D3D \_ \_ se usa para especificar el tipo de parte del BLOB de firma raíz. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) quita la firma raíz (mediante la marca de la \_ \_ firma raíz D3DCOMPILER \_ ) del BLOB.

## <a name="notes"></a>Notas

> [!Note]  
> Mientras que la compilación sin conexión de los sombreadores es muy recomendable, si los sombreadores deben compilarse en tiempo de ejecución, consulte la sección Comentarios de [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> No es necesario cambiar los recursos de HLSL existentes para controlar las firmas raíz que se usarán con ellos.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexado dinámico mediante HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Características del modelo de sombreador de HLSL 5,1 para Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> <dt>

[Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> <dt>

[Modelo de sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valor de referencia de estarcido del sombreador especificado](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Cargas de vista de acceso no ordenada con tipo](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 