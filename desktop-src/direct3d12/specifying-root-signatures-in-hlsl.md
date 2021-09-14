---
title: Especificación de firmas de raíz en HLSL
description: Especificar firmas raíz en el modelo de sombreador HLSL 5.1 es una alternativa a especificarlas en código de C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072871"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Especificación de firmas de raíz en HLSL

Especificar firmas raíz en el modelo de sombreador HLSL 5.1 es una alternativa a especificarlas en código de C++.

-   [Una firma raíz HLSL de ejemplo](#an-example-hlsl-root-signature)
    -   [Firma raíz versión 1.0](#root-signature-version-10)
    -   [Versión 1.1 de la firma raíz](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Constantes raíz](#root-constants)
-   [Visibilidad](#visibility)
-   [CBV de nivel raíz](#root-level-cbv)
-   [SRV de nivel raíz](#root-level-srv)
-   [UAV de nivel de raíz](#root-level-uav)
-   [Tabla descriptora](#descriptor-table)
-   [Sampler estático](#static-sampler)
-   [Compilación de una firma raíz HLSL](#compiling-an-hlsl-root-signature)
-   [Manipulación de firmas raíz con el compilador fxc](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Notas](#notes)
-   [Temas relacionados](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Una firma raíz HLSL de ejemplo

Una firma raíz se puede especificar en HLSL como una cadena. La cadena contiene una colección de cláusulas separadas por comas que describen los componentes constituyentes de la firma raíz. La firma raíz debe ser idéntica entre sombreadores para cualquier objeto de estado de canalización (PSO). Este es un ejemplo:

### <a name="root-signature-version-10"></a>Firma raíz versión 1.0

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

Esta definición proporcionaría la siguiente firma raíz, y se debe hacer lo siguiente:

-   El uso de parámetros predeterminados.
-   b0 y (b0, space=1) no están en conflicto
-   u0 solo es visible para el sombreador de geometría
-   u4 y u5 tienen alias para el mismo descriptor en un montón

![una firma raíz especificada mediante el lenguaje de sombreador de alto nivel](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a>Versión 1.1 de la firma raíz

[Root Signature Version 1.1 habilita](root-signature-version-1-1.md) las optimizaciones de controladores en los descriptores de firma raíz y los datos.

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

El lenguaje de firma raíz HLSL se corresponde estrechamente con las API de firma raíz de C++ y tiene una potencia expresiva equivalente. La firma raíz se especifica como una secuencia de cláusulas, separadas por comas. El orden de las cláusulas es importante, ya que el orden de análisis determina la posición de la ranura en la firma raíz. Cada cláusula toma uno o varios parámetros con nombre. Sin embargo, el orden de los parámetros no es importante.

## <a name="rootflags"></a>RootFlags

La *cláusula RootFlags* opcional toma 0 (el valor predeterminado para indicar que no hay marcas) o uno o varios de los valores de marcas raíz predefinidos, conectados a través del operador OR ' \| '. Los valores de marca raíz permitidos se definen mediante [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Por ejemplo:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Constantes raíz

La *cláusula RootConstants* especifica las constantes raíz en la firma raíz. Dos parámetros obligatorios son: *num32BitConstants* y *bReg* (el registro correspondiente a *BaseShaderRegister* en las API de C++) del *cbuffer*. Los parámetros space *(RegisterSpace* en las API de C++) y *visibility (ShaderVisibility* en C++) son opcionales y los valores predeterminados son:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Por ejemplo:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Visibilidad

Visibility es un parámetro opcional que puede tener uno de los valores de [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

SHADER \_ VISIBILITY \_ ALL difunde los argumentos raíz a todos los sombreadores. En algún hardware esto no tiene ningún costo, pero en otro hardware hay un costo para bifurcar los datos a todas las fases del sombreador. Al establecer una de las opciones, como SHADER VISIBILITY VERTEX, se limita \_ el argumento raíz a una sola fase del \_ sombreador.

Establecer argumentos raíz en fases de sombreador único permite usar el mismo nombre de enlace en distintas fases. Por ejemplo, un enlace SRV de `t0,SHADER_VISIBILITY_VERTEX` y un enlace SRV de sería `t0,SHADER_VISIBILITY_PIXEL` válido. Pero si la configuración de `t0,SHADER_VISIBILITY_ALL` visibilidad fuera para uno de los enlaces, la firma raíz no sería válida.

## <a name="root-level-cbv"></a>CBV de nivel raíz

La cláusula (vista de búfer constante) especifica una entrada reg de búfer constante de nivel `CBV` raíz b-register. Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV de nivel raíz

La `SRV` cláusula (vista de recursos del sombreador) especifica una entrada SRV t-register Reg de nivel raíz. Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV de nivel de raíz

La `UAV` cláusula (vista de acceso desordenado) especifica una entrada UAV u-register Reg de nivel raíz. Tenga en cuenta que se trata de una entrada escalar; no es posible especificar un intervalo para el nivel raíz.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Por ejemplo:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Tabla descriptora

La cláusula es en sí misma una lista de cláusulas de tabla de descriptores separadas por comas, así como `DescriptorTable` un parámetro de visibilidad opcional. Las *cláusulas descriptorTable* incluyen CBV, SRV, UAV y Sampler. Tenga en cuenta que sus parámetros difieren de los de las cláusulas de nivel raíz.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

La tabla descriptor `CBV` tiene la sintaxis siguiente:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Por ejemplo:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

El parámetro obligatorio *bReg* especifica el reg inicial del intervalo de cbuffer. El *parámetro numDescriptors* especifica el número de descriptores en el intervalo de cbuffer contiguo; el valor predeterminado es 1. La entrada declara un intervalo de cbuffer ` [Reg, Reg + numDescriptors - 1]` cuando *numDescriptors* es un número. Si *numDescriptors* es igual a "sin enlazar", el intervalo es , lo que significa que la aplicación debe asegurarse de que no hace referencia a un área fuera de `[Reg, UINT_MAX]` límites. El *campo offset* representa el parámetro *OffsetInDescriptorsFromTableStart* en las API de C++, es decir, el desplazamiento (en descriptores) desde el principio de la tabla. Si el desplazamiento se establece en DESCRIPTOR \_ RANGE \_ OFFSET APPEND (valor predeterminado), significa que el intervalo está directamente después \_ del intervalo anterior. Sin embargo, la especificación de desplazamientos específicos permite que los intervalos se superpongan entre sí, lo que permite el alias de registro.

La tabla descriptor `SRV` tiene la sintaxis siguiente:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Esto es similar a la entrada de la tabla descriptor, salvo que el intervalo especificado es para las vistas de recursos `CBV` de sombreador.

La tabla descriptor `UAV` tiene la sintaxis siguiente:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Esto es similar a la entrada de la tabla descriptor, salvo que `CBV` el intervalo especificado es para vistas de acceso no ordenado.

La tabla descriptor `Sampler` tiene la sintaxis siguiente:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Esto es similar a la entrada de la tabla descriptor, salvo que el intervalo especificado es para los `CBV` muestreadores de sombreador. Tenga en cuenta que los muestreadores no se pueden mezclar con otros tipos de descriptores en la misma tabla de descriptores (ya que están en un montón de descriptores independiente).

## <a name="static-sampler"></a>Sampler estático

El sampler estático representa la [**estructura D3D12 \_ STATIC \_ SAMPLER \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) El parámetro obligatorio para *StaticSampler* es un valor escalar, sampler s-register Reg. Otros parámetros son opcionales con los valores predeterminados que se muestran a continuación. La mayoría de los campos aceptan un conjunto de enumeraciones predefinidas.

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

Las opciones de parámetro son muy similares a las llamadas API de C++, excepto *borderColor*, que está restringida a una enumeración en HLSL.

El campo de filtro puede ser uno de [**D3D12 \_ FILTER.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)

Los campos de dirección pueden ser uno de [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

La función de comparación puede ser una de las funciones [**\_ \_ FUNC COMPARISON de D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

El campo de color del borde puede ser uno de [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

La visibilidad puede ser una de las [**VISIBILIDAD DEL \_ SOMBREADOR \_ de D3D12.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)

## <a name="compiling-an-hlsl-root-signature"></a>Compilación de una firma raíz HLSL

Hay dos mecanismos para compilar una firma raíz HLSL. En primer lugar, es posible adjuntar una cadena de firma raíz a un sombreador determinado mediante el atributo *RootSignature* (en el ejemplo siguiente, mediante el punto de entrada **MyRS1):**

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

El compilador creará y comprobará el blob de firma raíz para el sombreador e insertará junto con el código de bytes del sombreador en el blob del sombreador. El compilador admite la sintaxis de firma raíz para el modelo de sombreador 5.0 y superior. Si una firma raíz está incrustada en un sombreador del modelo 5.0 del sombreador y ese sombreador se envía al entorno de ejecución D3D11, en lugar de D3D12, D3D11 omitirá silenciosamente la parte de la firma raíz.

El otro mecanismo es crear un blob de firma raíz independiente, quizás para reutilizarlo con un gran conjunto de sombreadores, lo que ahorra espacio. [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) admite los modelos de sombreador **rootsig \_ 1 \_ 0** y **rootsig \_ \_ 1 1.** El nombre de la cadena de definición se especifica a través del argumento /E habitual. Por ejemplo:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Tenga en cuenta que la definición de la cadena de firma raíz también se puede pasar en la línea de comandos, por ejemplo, /D MyRS1="...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Manipulación de firmas raíz con el compilador FXC

El compilador FXC crea código de bytes de sombreador a partir de archivos de código fuente HLSL. Hay una gran cantidad de parámetros opcionales para este compilador; consulte [la herramienta Effect-Compiler .](/windows/desktop/direct3dtools/fxc)

Para administrar firmas raíz de HLSL, en la tabla siguiente se proporcionan algunos ejemplos del uso de FXC.



| Línea | Línea de comandos                                                                 | Descripción                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Compila un sombreador para el destino del sombreador de píxeles 5.1; el origen del sombreador está en el archivo shaderWithRootSig.hlsl, que incluye una firma raíz. El sombreador y la firma raíz se compilan como blobs independientes en el archivo binario rs1.fxo.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Extrae la firma raíz del archivo creado por la línea 1, por lo que el archivo rs1.rs.fxo contiene solo una firma raíz.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Quita la firma raíz del archivo creado por la línea 1, por lo que el archivo rs1.striped.fxo contiene un sombreador sin firma raíz.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Combina un sombreador y una firma raíz que están en archivos independientes en un archivo binario que contiene ambos blobs. En este ejemplo, rs1.new.fx0 sería idéntico a rs1.fx0 en la línea 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Crea un archivo binario de firma raíz independiente a partir de un origen que puede contener algo más que una firma raíz. Observe el destino rootsig 1 0 y que RS1 es el nombre de la cadena de macro de firma raíz (definir) en el \_ \_ archivo \# HLSL. |



 

La funcionalidad disponible a través de FXC también está disponible mediante programación mediante la [**función D3DCompile.**](/windows/desktop/direct3dhlsl/d3dcompile) Esta llamada compila un sombreador con una firma raíz o una firma raíz independiente (estableciendo el destino rootsig \_ \_ 1 0). [**D3DGetBlobPart y**](/windows/desktop/direct3dhlsl/d3dgetblobpart) [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) pueden extraer y adjuntar firmas raíz a un blob existente.  D3D \_ BLOB ROOT SIGNATURE se usa para especificar el tipo de elemento de blob de firma \_ \_ raíz. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) quita la firma raíz (mediante la marca D3DCOMPILER \_ STRIP \_ ROOT \_ SIGNATURE) del blob.

## <a name="notes"></a>Notas

> [!Note]  
> Mientras que se recomienda encarecidamente la compilación sin conexión de sombreadores, si los sombreadores tienen que compilarse en tiempo de ejecución, consulte los comentarios de [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> No es necesario cambiar los recursos HLSL existentes para controlar las firmas raíz que se usarán con ellos.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexado dinámico mediante HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Características del modelo de sombreador HLSL 5.1 para Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> <dt>

[Enlace de recursos en HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> <dt>

[Modelo de sombreador 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valor de la referencia de galería de símbolos especificado por el sombreador](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Cargas de la vista de acceso sin ordenar con tipo](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
