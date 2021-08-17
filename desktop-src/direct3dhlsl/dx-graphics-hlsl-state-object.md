---
title: Objetos de estados
description: Use HLSL para definir objetos de estado.
ms.assetid: a02432dc-f354-48c0-a7ac-1ff502f3b1d1
ms.topic: article
ms.date: 2/2/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70ff3ca1fb2509cd5f788cc1965920c46af5791bec10bb833df19f4b4f9be533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119939"
---
# <a name="state-objects"></a>Objetos de estados

Con los modelos de sombreador 6.3 y versiones posteriores, las aplicaciones tienen la comodidad y flexibilidad de poder definir objetos de estado DXR directamente en el código del sombreador HLSL, además de usar las API de Direct3D 12.

En HLSL, los objetos de estado se declaran con esta sintaxis:

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**<br/>     | Identifica el tipo de subobjeto. Debe ser uno de los tipos de subobjeto HLSL admitidos.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo[1, 2, ...]**<br/> | Campos del subobjeto. A continuación se describen campos específicos para cada tipo de subobjeto.<br/> |




Lista de tipos de subobjetos:
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

El tipo de subobjeto StateObjectConfig corresponde a una [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) estructura.

Tiene un campo, una marca bit a bit, que es uno o ambos de

* STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
* STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS

o bien, cero para ninguno de ellos.

Ejemplo:

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a>GlobalRootSignature
GlobalRootSignature corresponde a una [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) estructura.

Los campos constan de un número de cadenas que describen las partes de la firma raíz. Para obtener referencia sobre esto, vea [Especificar firmas raíz en HLSL.](../direct3d12/specifying-root-signatures-in-hlsl.md)

Ejemplo:
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a>LocalRootSignature
LocalRootSignature corresponde a una [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) estructura.

Al igual que el subobjeto de firma raíz global, los campos constan de un número de cadenas que describen las partes de la firma raíz. Para obtener referencia sobre esto, vea [Especificar firmas raíz en HLSL.](../direct3d12/specifying-root-signatures-in-hlsl.md)

Ejemplo:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
De forma predeterminada, un subobjeto simplemente declarado en la misma biblioteca que una exportación puede aplicarse a esa exportación. Sin embargo, las aplicaciones tienen la capacidad de invalidarlo y obtener información específica sobre qué subobjeto va con qué exportación. En HLSL, esta "asociación explícita" se realiza mediante SubobjectToExportsAssocation.

Un subobjetoToExportsAssocation corresponde a una [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) estructura.

Este subobjeto se declara con la sintaxis

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**<br/>     | Cadena que identifica un subobjeto exportado.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exportaciones**<br/> | Cadena que contiene una lista delimitada por punto y coma de exportaciones.<br/> |


Ejemplo:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Tenga en cuenta que ambos campos usan *nombres exportados.* Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación decide realizar el cambio de nombre de exportación.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

RaytracingShaderConfig corresponde a una [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) estructura.

Este subobjeto se declara con la sintaxis

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Valor numérico para el almacenamiento máximo para escalares (se cuenta como 4 bytes cada uno) en cargas de rayos para sombreadores de rayos asociados.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Valor numérico para el número máximo de escalares (se cuentan como 4 bytes cada uno) que se pueden usar para los atributos de los sombreadores de trazado de rayos asociados. El valor no puede superar [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Ejemplo:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

RaytracingPipelineConfig corresponde a una [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) estructura.

Este subobjeto se declara con la sintaxis

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Límite numérico que se usará para la recursión de rayos en la canalización de rayos. Es un número entre 0 y 31, ambos inclusive. <br/> |


Ejemplo:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Dado que hay un costo de rendimiento para la recursividad prolongada, las aplicaciones deben usar la profundidad de recursividad más baja necesaria para los resultados deseados.

Si las invocaciones de sombreador aún no han alcanzado la profundidad máxima de recursión, pueden llamar a [TraceRay](../direct3d12/traceray-function.md) varias veces. Pero si alcanzan o superan la profundidad máxima de recursión, al llamar a TraceRay se coloca el dispositivo en estado eliminado. Por lo tanto, los sombreadores de seguimiento de rayos deben tener cuidado de dejar de llamar a TraceRay si han cumplido o superado la profundidad máxima de recursión.

## <a name="trianglehitgroup"></a>TriangleHitGroup

Un TriangleHitGroup corresponde a una [estructura D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cuyo campo Type está establecido [en D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Este subobjeto se declara con la sintaxis

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nombre de cadena del sombreador anyhit para el grupo de operaciones o una cadena vacía.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nombre de cadena del sombreador de pulsaciones más cercano para el grupo de operaciones o una cadena vacía.<br/> |


Ejemplo:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Tenga en cuenta que ambos campos usan *nombres exportados.* Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación decide realizar el cambio de nombre de exportación.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Un objeto ProceduralPrimitiveHitGroup corresponde a una [estructura D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cuyo campo Type está establecido [en D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

Este subobjeto se declara con la sintaxis

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nombre de cadena del sombreador anyhit para el grupo de impacto o una cadena vacía.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nombre de cadena del sombreador de pulsaciones más cercano para el grupo de impacto o una cadena vacía.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Nombre de cadena del sombreador de intersección para el grupo de impacto o una cadena vacía.<br/> |


Ejemplo:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Tenga en cuenta que los tres campos usan *nombres exportados.* Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación decide realizar el cambio de nombre de exportación.

## <a name="remarks"></a>Comentarios

Los subobjetos tienen la noción de "asociación" o "qué subobjeto va con qué exportación".

Al especificar subobjetos a través del código del [sombreador,](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior)la elección de "qué subobjeto va con qué exportación" sigue las reglas como se describe en la especificación DXR . En concreto, suponga que una aplicación tiene alguna exportación. Si una aplicación asocia esa exportación con la firma raíz A a través del código de sombreador y la firma raíz B a través del código de aplicación, B es la que se usa. El diseño de "usar B" en lugar de "generar un error" ofrece a las aplicaciones la capacidad de invalidar cómodamente las asociaciones DXIL mediante código de aplicación, en lugar de forzarse a volver a compilar sombreadores para resolver los errores de coincidencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Entrada de blog para desarrolladores de DirectX "Novedades de D3D12: DirectX Raytracing (DXR) ahora admite subobjetos de biblioteca"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Especificación funcional de DirectX Raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Ejemplo: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>