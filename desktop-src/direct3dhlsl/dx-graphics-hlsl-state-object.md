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
ms.openlocfilehash: 53bfc903f8bc1be56962e912b1c82f02faaf0c44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998009"
---
# <a name="state-objects"></a>Objetos de estados

Con los modelos de sombreador 6,3 y versiones posteriores, las aplicaciones tienen la comodidad y la flexibilidad de poder definir objetos de estado DXR directamente en el código del sombreador HLSL además de usar las API de Direct3D 12.

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
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Automáticamente**<br/>     | Identifica el tipo de subobjeto. Debe ser uno de los tipos de subobjeto HLSL admitidos.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo [1, 2,...]**<br/> | Campos del subobjeto. A continuación se describen los campos específicos de cada tipo de subobjeto.<br/> |




Lista de tipos de subobjeto:
-   [StateObjectConfig](#stateobjectconfig)
-   [GlobalRootSignature](#globalrootsignature)
-   [LocalRootSignature](#localrootsignature)
-   [SubobjectToExportsAssocation](#subobjecttoexportsassocation)
-   [RaytracingShaderConfig](#raytracingshaderconfig)
-   [RaytracingPipelineConfig](#raytracingpipelineconfig)
-   [TriangleHitGroup](#trianglehitgroup)
-   [ProceduralPrimitiveHitGroup](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a>StateObjectConfig

El tipo de subobjeto StateObjectConfig corresponde a una estructura [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .

Tiene un campo, una marca bit a bit, que es uno de los dos tipos de

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
Un GlobalRootSignature corresponde a una estructura de [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .

Los campos se componen de un número de cadenas que describen las partes de la firma raíz. Como referencia sobre esto, consulte [especificar firmas de raíz en HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

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
Un LocalRootSignature corresponde a una estructura de [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .

Al igual que el subobjeto de la firma raíz global, los campos se componen de un número de cadenas que describen las partes de la firma raíz. Como referencia sobre esto, consulte [especificar firmas de raíz en HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).

Ejemplo:
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a>SubobjectToExportsAssocation
De forma predeterminada, un subobjeto que se declara simplemente en la misma biblioteca como una exportación puede aplicarse a esa exportación. Sin embargo, las aplicaciones tienen la capacidad de invalidarlo y obtener información específica sobre el subobjeto que va con la exportación. En HLSL, esta "asociación explícita" se realiza mediante SubobjectToExportsAssocation.

Un SubobjectToExportsAssocation corresponde a una estructura de [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .

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
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**<br/>     | Cadena que identifica un subobjeto exportado.<br/> |
| <span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Port**<br/> | Cadena que contiene una lista delimitada por signos de punto y coma de exportaciones.<br/> |


Ejemplo:
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

Tenga en cuenta que ambos campos usan nombres *exportados* . Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación opta por hacer el cambio de nombre de exportación.

## <a name="raytracingshaderconfig"></a>RaytracingShaderConfig

Un RaytracingShaderConfig corresponde a una estructura de [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .

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
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**<br/>     | Valor numérico para el almacenamiento máximo para los escalares (contados como 4 bytes cada uno) en las cargas de rayo para los sombreadores raytracing asociados.<br/> |
| <span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**<br/> | Valor numérico para el número máximo de escalares (contados como 4 bytes cada uno) que se pueden usar para los atributos de los sombreadores raytracing asociados. El valor no puede superar [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).<br/> |


Ejemplo:
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a>RaytracingPipelineConfig

Un RaytracingPipelineConfig corresponde a una estructura de [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .

Este subobjeto se declara con la sintaxis

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| Elemento                                                                                         | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**<br/>     | Límite numérico que se va a usar para la recursividad de rayo en la canalización raytracing. Es un número entre 0 y 31, ambos inclusive. <br/> |


Ejemplo:
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
Dado que hay un costo de rendimiento para raytracing la recursividad, las aplicaciones deben usar la profundidad de recursividad más baja necesaria para los resultados deseados.

Si las invocaciones del sombreador todavía no han alcanzado la profundidad de recursividad máxima, pueden llamar a [TraceRay](../direct3d12/traceray-function.md) cualquier número de veces. Pero si alcanzan o superan la profundidad de recursividad máxima, al llamar a TraceRay se quita el estado del dispositivo. Por lo tanto, los sombreadores de raytracing deben tener cuidado de dejar de llamar a TraceRay si han alcanzado o superado la profundidad de recursividad máxima.

## <a name="trianglehitgroup"></a>TriangleHitGroup

Un TriangleHitGroup corresponde a una estructura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cuyo campo de tipo se establece en [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

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
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nombre de cadena del sombreador anyhit para el grupo de aciertos o una cadena vacía.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nombre de cadena del sombreador de posicionamiento más cercano para el grupo de visitas o una cadena vacía.<br/> |


Ejemplo:
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

Tenga en cuenta que ambos campos usan nombres *exportados* . Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación opta por hacer el cambio de nombre de exportación.

## <a name="proceduralprimitivehitgroup"></a>ProceduralPrimitiveHitGroup

Un ProceduralPrimitiveHitGroup corresponde a una estructura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cuyo campo de tipo se establece en [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).

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
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**<br/>     | Cadena ASCII que identifica de forma única el nombre de la variable.<br/>                 |
| <span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**<br/>     | Nombre de cadena del sombreador anyhit para el grupo de aciertos o una cadena vacía.<br/> |
| <span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**<br/> | Nombre de cadena del sombreador de posicionamiento más cercano para el grupo de visitas o una cadena vacía.<br/> |
| <span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**<br/> | Nombre de cadena del sombreador de intersección del grupo de visitas o una cadena vacía.<br/> |


Ejemplo:
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

Tenga en cuenta que los tres campos usan nombres *exportados* . Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación opta por hacer el cambio de nombre de exportación.

## <a name="remarks"></a>Observaciones

Los subobjetos tienen la noción de "Association" o "qué subobjeto va a partir de la exportación".

Al especificar los subobjetos mediante el código del sombreador, la opción de "qué subobjeto se dirige a la exportación" sigue las reglas que se describen en la [especificación DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior). En concreto, supongamos que una aplicación tiene alguna exportación. Si una aplicación asocia esa exportación con la firma raíz a mediante el código del sombreador y la firma raíz B a través del código de la aplicación, B es la que se usa. El diseño de "uso B" en lugar de "producir un error" proporciona a las aplicaciones la capacidad de invalidar las asociaciones de DXIL de forma cómoda mediante el código de aplicación, en lugar de forzarse a que vuelvan a compilar los sombreadores para resolver las cosas que no coinciden.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Publicación de blog para desarrolladores de DirectX "novedad en D3D12 – DirectX raytracing (DXR) ahora admite subobjetos de biblioteca"](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[Especificación funcional de DirectX raytracing (DXR)](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[Ejemplo: D3D12RaytracingLibrarySubobjects](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>