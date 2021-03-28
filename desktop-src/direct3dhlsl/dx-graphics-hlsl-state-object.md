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
# <a name="state-objects"></a><span data-ttu-id="cf6e5-103">Objetos de estados</span><span class="sxs-lookup"><span data-stu-id="cf6e5-103">State Objects</span></span>

<span data-ttu-id="cf6e5-104">Con los modelos de sombreador 6,3 y versiones posteriores, las aplicaciones tienen la comodidad y la flexibilidad de poder definir objetos de estado DXR directamente en el código del sombreador HLSL además de usar las API de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-104">With shader models 6.3 and later, applications have the convenience and flexibility of being able to define DXR state objects directly in HLSL shader code in addition to using Direct3D 12 APIs.</span></span>

<span data-ttu-id="cf6e5-105">En HLSL, los objetos de estado se declaran con esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-105">In HLSL, state objects are declared with this syntax:</span></span>

``` syntax
Type Name = 
{ 
    Field1,
    Field2,
    ...
};
```



| <span data-ttu-id="cf6e5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6e5-106">Item</span></span>                                                                                         | <span data-ttu-id="cf6e5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6e5-107">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6e5-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Automáticamente**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="cf6e5-109">Identifica el tipo de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-109">Identifies the type of subobject.</span></span> <span data-ttu-id="cf6e5-110">Debe ser uno de los tipos de subobjeto HLSL admitidos.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-110">Must be one of the supported HLSL subobject types.</span></span><br/>     |
| <span data-ttu-id="cf6e5-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="cf6e5-112">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-112">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="cf6e5-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Campo [1, 2,...]**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-113"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>**Field[1, 2, ...]**</span></span><br/> | <span data-ttu-id="cf6e5-114">Campos del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-114">Fields of the subobject.</span></span> <span data-ttu-id="cf6e5-115">A continuación se describen los campos específicos de cada tipo de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-115">Specific fields for each type of subobject are described below.</span></span><br/> |




<span data-ttu-id="cf6e5-116">Lista de tipos de subobjeto:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-116">List of subobject types:</span></span>
-   [<span data-ttu-id="cf6e5-117">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="cf6e5-117">StateObjectConfig</span></span>](#stateobjectconfig)
-   [<span data-ttu-id="cf6e5-118">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="cf6e5-118">GlobalRootSignature</span></span>](#globalrootsignature)
-   [<span data-ttu-id="cf6e5-119">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="cf6e5-119">LocalRootSignature</span></span>](#localrootsignature)
-   [<span data-ttu-id="cf6e5-120">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="cf6e5-120">SubobjectToExportsAssocation</span></span>](#subobjecttoexportsassocation)
-   [<span data-ttu-id="cf6e5-121">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="cf6e5-121">RaytracingShaderConfig</span></span>](#raytracingshaderconfig)
-   [<span data-ttu-id="cf6e5-122">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="cf6e5-122">RaytracingPipelineConfig</span></span>](#raytracingpipelineconfig)
-   [<span data-ttu-id="cf6e5-123">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="cf6e5-123">TriangleHitGroup</span></span>](#trianglehitgroup)
-   [<span data-ttu-id="cf6e5-124">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="cf6e5-124">ProceduralPrimitiveHitGroup</span></span>](#proceduralprimitivehitgroup)

## <a name="stateobjectconfig"></a><span data-ttu-id="cf6e5-125">StateObjectConfig</span><span class="sxs-lookup"><span data-stu-id="cf6e5-125">StateObjectConfig</span></span>

<span data-ttu-id="cf6e5-126">El tipo de subobjeto StateObjectConfig corresponde a una estructura [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-126">The StateObjectConfig subobject type corresponds to a [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) structure.</span></span>

<span data-ttu-id="cf6e5-127">Tiene un campo, una marca bit a bit, que es uno de los dos tipos de</span><span class="sxs-lookup"><span data-stu-id="cf6e5-127">It has one field, a bitwise flag, which is one or both of</span></span>

* <span data-ttu-id="cf6e5-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span><span class="sxs-lookup"><span data-stu-id="cf6e5-128">STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS</span></span>
* <span data-ttu-id="cf6e5-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span><span class="sxs-lookup"><span data-stu-id="cf6e5-129">STATE_OBJECT_FLAGS_ALLOW_EXTERNAL_DEPENDENCIES_ON_LOCAL_DEFINITIONS</span></span>

<span data-ttu-id="cf6e5-130">o bien, cero para ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-130">or, zero for neither of them.</span></span>

<span data-ttu-id="cf6e5-131">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-131">Example:</span></span>

```
StateObjectConfig MyStateObjectConfig = 
{ 
    STATE_OBJECT_FLAGS_ALLOW_LOCAL_DEPENDENCIES_ON_EXTERNAL_DEFINITONS
};
```

## <a name="globalrootsignature"></a><span data-ttu-id="cf6e5-132">GlobalRootSignature</span><span class="sxs-lookup"><span data-stu-id="cf6e5-132">GlobalRootSignature</span></span>
<span data-ttu-id="cf6e5-133">Un GlobalRootSignature corresponde a una estructura de [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-133">A GlobalRootSignature corresponds to a [D3D12_GLOBAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_global_root_signature) structure.</span></span>

<span data-ttu-id="cf6e5-134">Los campos se componen de un número de cadenas que describen las partes de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-134">The fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="cf6e5-135">Como referencia sobre esto, consulte [especificar firmas de raíz en HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="cf6e5-135">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="cf6e5-136">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-136">Example:</span></span>
```
GlobalRootSignature MyGlobalRootSignature =
{
    "DescriptorTable(UAV(u0)),"                     // Output texture
    "SRV(t0),"                                      // Acceleration structure
    "CBV(b0),"                                      // Scene constants
    "DescriptorTable(SRV(t1, numDescriptors = 2))"  // Static index and vertex buffers.
};
```

## <a name="localrootsignature"></a><span data-ttu-id="cf6e5-137">LocalRootSignature</span><span class="sxs-lookup"><span data-stu-id="cf6e5-137">LocalRootSignature</span></span>
<span data-ttu-id="cf6e5-138">Un LocalRootSignature corresponde a una estructura de [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-138">A LocalRootSignature corresponds to a [D3D12_LOCAL_ROOT_SIGNATURE](/windows/win32/api/d3d12/ns-d3d12-d3d12_local_root_signature) structure.</span></span>

<span data-ttu-id="cf6e5-139">Al igual que el subobjeto de la firma raíz global, los campos se componen de un número de cadenas que describen las partes de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-139">Just like the global root signature subobject, the fields consist of some number of strings describing the parts of the root signature.</span></span> <span data-ttu-id="cf6e5-140">Como referencia sobre esto, consulte [especificar firmas de raíz en HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="cf6e5-140">For reference on this, see [Specifying Root Signatures in HLSL](../direct3d12/specifying-root-signatures-in-hlsl.md).</span></span>

<span data-ttu-id="cf6e5-141">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-141">Example:</span></span>
```
LocalRootSignature MyLocalRootSignature = 
{
    "RootConstants(num32BitConstants = 4, b1)"  // Cube constants 
};
```

## <a name="subobjecttoexportsassocation"></a><span data-ttu-id="cf6e5-142">SubobjectToExportsAssocation</span><span class="sxs-lookup"><span data-stu-id="cf6e5-142">SubobjectToExportsAssocation</span></span>
<span data-ttu-id="cf6e5-143">De forma predeterminada, un subobjeto que se declara simplemente en la misma biblioteca como una exportación puede aplicarse a esa exportación.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-143">By default, a subobject merely declared in the same library as an export is able to apply to that export.</span></span> <span data-ttu-id="cf6e5-144">Sin embargo, las aplicaciones tienen la capacidad de invalidarlo y obtener información específica sobre el subobjeto que va con la exportación.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-144">However, applications have the ability to override that and get specific about what subobject goes with which export.</span></span> <span data-ttu-id="cf6e5-145">En HLSL, esta "asociación explícita" se realiza mediante SubobjectToExportsAssocation.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-145">In HLSL, this "explicit association" is done using SubobjectToExportsAssocation.</span></span>

<span data-ttu-id="cf6e5-146">Un SubobjectToExportsAssocation corresponde a una estructura de [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-146">A SubobjectToExportsAssocation corresponds to a [D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION ](/windows/win32/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association) structure.</span></span>

<span data-ttu-id="cf6e5-147">Este subobjeto se declara con la sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf6e5-147">This subobject is declared with the syntax</span></span>

``` syntax
SubobjectToExportsAssocation Name = 
{ 
    SubobjectName,
    Exports
};
```

| <span data-ttu-id="cf6e5-148">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6e5-148">Item</span></span>                                                                                         | <span data-ttu-id="cf6e5-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6e5-149">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6e5-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-150"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="cf6e5-151">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-151">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="cf6e5-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-152"><span id="SubobjectName"></span><span id="subobjectname"></span><span id="SUBOBJECTNAME"></span>**SubobjectName**</span></span><br/>     | <span data-ttu-id="cf6e5-153">Cadena que identifica un subobjeto exportado.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-153">String which identifies an exported subobject.</span></span><br/> |
| <span data-ttu-id="cf6e5-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Port**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-154"><span id="Exports"></span><span id="exports"></span><span id="EXPORTS"></span>**Exports**</span></span><br/> | <span data-ttu-id="cf6e5-155">Cadena que contiene una lista delimitada por signos de punto y coma de exportaciones.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-155">String containing a semicolon-delimited list of exports.</span></span><br/> |


<span data-ttu-id="cf6e5-156">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-156">Example:</span></span>
```
SubobjectToExportsAssociation MyLocalRootSignatureAssociation =
{
    "MyLocalRootSignature",    // Subobject name
    "MyHitGroup;MyMissShader"  // Exports association 
};
```

<span data-ttu-id="cf6e5-157">Tenga en cuenta que ambos campos usan nombres *exportados* .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-157">Note that both fields use *exported* names.</span></span> <span data-ttu-id="cf6e5-158">Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación opta por hacer el cambio de nombre de exportación.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-158">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="raytracingshaderconfig"></a><span data-ttu-id="cf6e5-159">RaytracingShaderConfig</span><span class="sxs-lookup"><span data-stu-id="cf6e5-159">RaytracingShaderConfig</span></span>

<span data-ttu-id="cf6e5-160">Un RaytracingShaderConfig corresponde a una estructura de [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-160">A RaytracingShaderConfig corresponds to a [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) structure.</span></span>

<span data-ttu-id="cf6e5-161">Este subobjeto se declara con la sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf6e5-161">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingShaderConfig Name = 
{ 
    MaxPayloadSize,
    MaxAttributeSize
};
```

| <span data-ttu-id="cf6e5-162">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6e5-162">Item</span></span>                                                                                         | <span data-ttu-id="cf6e5-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6e5-163">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6e5-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="cf6e5-165">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-165">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="cf6e5-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-166"><span id="MaxPayloadSize"></span><span id="maxpayloadsize"></span><span id="MAXPAYLOADSIZE"></span>**MaxPayloadSize**</span></span><br/>     | <span data-ttu-id="cf6e5-167">Valor numérico para el almacenamiento máximo para los escalares (contados como 4 bytes cada uno) en las cargas de rayo para los sombreadores raytracing asociados.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-167">Numerical value for the maximum storage for scalars (counted as 4 bytes each) in ray payloads for associated raytracing shaders.</span></span><br/> |
| <span data-ttu-id="cf6e5-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-168"><span id="MaxAttributeSize"></span><span id="maxattributesize"></span><span id="MAXATTRIBUTESIZE"></span>**MaxAttributeSize**</span></span><br/> | <span data-ttu-id="cf6e5-169">Valor numérico para el número máximo de escalares (contados como 4 bytes cada uno) que se pueden usar para los atributos de los sombreadores raytracing asociados.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-169">Numerical value for the maximum number of scalars (counted as 4 bytes each) that can be used for attributes in associated raytracing shaders.</span></span> <span data-ttu-id="cf6e5-170">El valor no puede superar [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span><span class="sxs-lookup"><span data-stu-id="cf6e5-170">The value cannot exceed [D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES](../direct3d12/constants.md).</span></span><br/> |


<span data-ttu-id="cf6e5-171">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-171">Example:</span></span>
```
RaytracingShaderConfig MyShaderConfig =
{
    16,  // Max payload size
    8    // Max attribute size
};
```

## <a name="raytracingpipelineconfig"></a><span data-ttu-id="cf6e5-172">RaytracingPipelineConfig</span><span class="sxs-lookup"><span data-stu-id="cf6e5-172">RaytracingPipelineConfig</span></span>

<span data-ttu-id="cf6e5-173">Un RaytracingPipelineConfig corresponde a una estructura de [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-173">A RaytracingPipelineConfig corresponds to a [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) structure.</span></span>

<span data-ttu-id="cf6e5-174">Este subobjeto se declara con la sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf6e5-174">This subobject is declared with the syntax</span></span>

``` syntax
RaytracingPipelineConfig Name = 
{ 
    MaxTraceRecursionDepth
};
```

| <span data-ttu-id="cf6e5-175">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6e5-175">Item</span></span>                                                                                         | <span data-ttu-id="cf6e5-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6e5-176">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6e5-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-177"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="cf6e5-178">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-178">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="cf6e5-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-179"><span id="MaxTraceRecursionDepth"></span><span id="maxtracerecursiondepth"></span><span id="MAXTRACERECURSIONDEPTH"></span>**MaxTraceRecursionDepth**</span></span><br/>     | <span data-ttu-id="cf6e5-180">Límite numérico que se va a usar para la recursividad de rayo en la canalización raytracing.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-180">Numerical limit to use for ray recursion in the raytracing pipeline.</span></span> <span data-ttu-id="cf6e5-181">Es un número entre 0 y 31, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-181">It is a number between 0 and 31, inclusive.</span></span> <br/> |


<span data-ttu-id="cf6e5-182">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-182">Example:</span></span>
```
RaytracingPipelineConfig MyPipelineConfig =
{
    1  // Max trace recursion depth
};
```
<span data-ttu-id="cf6e5-183">Dado que hay un costo de rendimiento para raytracing la recursividad, las aplicaciones deben usar la profundidad de recursividad más baja necesaria para los resultados deseados.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-183">Since there is a performance cost to raytracing recursion, applications should use the lowest recursion depth needed for the desired results.</span></span>

<span data-ttu-id="cf6e5-184">Si las invocaciones del sombreador todavía no han alcanzado la profundidad de recursividad máxima, pueden llamar a [TraceRay](../direct3d12/traceray-function.md) cualquier número de veces.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-184">If shader invocations haven't yet reached the maximum recursion depth, they can call [TraceRay](../direct3d12/traceray-function.md) any number of times.</span></span> <span data-ttu-id="cf6e5-185">Pero si alcanzan o superan la profundidad de recursividad máxima, al llamar a TraceRay se quita el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-185">But if they reach or exceed the maximum recursion depth, calling TraceRay puts the device into removed state.</span></span> <span data-ttu-id="cf6e5-186">Por lo tanto, los sombreadores de raytracing deben tener cuidado de dejar de llamar a TraceRay si han alcanzado o superado la profundidad de recursividad máxima.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-186">Therefore, raytracing shaders should take care to stop calling TraceRay if they've met or exceeded the maximum recursion depth.</span></span>

## <a name="trianglehitgroup"></a><span data-ttu-id="cf6e5-187">TriangleHitGroup</span><span class="sxs-lookup"><span data-stu-id="cf6e5-187">TriangleHitGroup</span></span>

<span data-ttu-id="cf6e5-188">Un TriangleHitGroup corresponde a una estructura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cuyo campo de tipo se establece en [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="cf6e5-188">A TriangleHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="cf6e5-189">Este subobjeto se declara con la sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf6e5-189">This subobject is declared with the syntax</span></span>

``` syntax
TriangleHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader
};
```

| <span data-ttu-id="cf6e5-190">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6e5-190">Item</span></span>                                                                                         | <span data-ttu-id="cf6e5-191">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6e5-191">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6e5-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-192"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="cf6e5-193">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-193">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="cf6e5-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-194"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="cf6e5-195">Nombre de cadena del sombreador anyhit para el grupo de aciertos o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-195">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="cf6e5-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-196"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="cf6e5-197">Nombre de cadena del sombreador de posicionamiento más cercano para el grupo de visitas o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-197">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="cf6e5-198">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-198">Example:</span></span>
```
TriangleHitGroup MyHitGroup =
{
    "",                    // AnyHit
    "MyClosestHitShader",  // ClosestHit
};
```

<span data-ttu-id="cf6e5-199">Tenga en cuenta que ambos campos usan nombres *exportados* .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-199">Note that both fields use *exported* names.</span></span> <span data-ttu-id="cf6e5-200">Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación opta por hacer el cambio de nombre de exportación.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-200">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="proceduralprimitivehitgroup"></a><span data-ttu-id="cf6e5-201">ProceduralPrimitiveHitGroup</span><span class="sxs-lookup"><span data-stu-id="cf6e5-201">ProceduralPrimitiveHitGroup</span></span>

<span data-ttu-id="cf6e5-202">Un ProceduralPrimitiveHitGroup corresponde a una estructura de [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) cuyo campo de tipo se establece en [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span><span class="sxs-lookup"><span data-stu-id="cf6e5-202">A ProceduralPrimitiveHitGroup corresponds to a [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) structure whose Type field is set to [D3D12_HIT_GROUP_TYPE_PROCEDURAL_PRIMITIVE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type#constants).</span></span>

<span data-ttu-id="cf6e5-203">Este subobjeto se declara con la sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf6e5-203">This subobject is declared with the syntax</span></span>

``` syntax
ProceduralPrimitiveHitGroup Name = 
{ 
    AnyHitShader,
    ClosestHitShader,
    IntersectionShader
};
```

| <span data-ttu-id="cf6e5-204">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf6e5-204">Item</span></span>                                                                                         | <span data-ttu-id="cf6e5-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf6e5-205">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6e5-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-206"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="cf6e5-207">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-207">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="cf6e5-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-208"><span id="AnyHitShader"></span><span id="anyhitshader"></span><span id="ANYHITSHADER"></span>**AnyHitShader**</span></span><br/>     | <span data-ttu-id="cf6e5-209">Nombre de cadena del sombreador anyhit para el grupo de aciertos o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-209">String name of the anyhit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="cf6e5-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-210"><span id="ClosestHitShader"></span><span id="closesthitshader"></span><span id="CLOSESTHITSHADER"></span>**ClosestHitShader**</span></span><br/> | <span data-ttu-id="cf6e5-211">Nombre de cadena del sombreador de posicionamiento más cercano para el grupo de visitas o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-211">String name of the closest hit shader for the hit group, or an empty string.</span></span><br/> |
| <span data-ttu-id="cf6e5-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span><span class="sxs-lookup"><span data-stu-id="cf6e5-212"><span id="IntersectionShader"></span><span id="intersectionshader"></span><span id="INTERSECTIONSHADER"></span>**IntersectionShader**</span></span><br/> | <span data-ttu-id="cf6e5-213">Nombre de cadena del sombreador de intersección del grupo de visitas o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-213">String name of the intersection shader for the hit group, or an empty string.</span></span><br/> |


<span data-ttu-id="cf6e5-214">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cf6e5-214">Example:</span></span>
```
ProceduralPrimitiveHitGroup MyProceduralHitGroup
{
    "MyAnyHit",       // AnyHit
    "MyClosestHit",   // ClosestHit
    "MyIntersection"  // Intersection
};

```

<span data-ttu-id="cf6e5-215">Tenga en cuenta que los tres campos usan nombres *exportados* .</span><span class="sxs-lookup"><span data-stu-id="cf6e5-215">Note that the three fields use *exported* names.</span></span> <span data-ttu-id="cf6e5-216">Un nombre exportado puede ser diferente del nombre original en HLSL, si la aplicación opta por hacer el cambio de nombre de exportación.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-216">An exported name may be different from the original name in HLSL, if the application chooses to do export-renaming.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6e5-217">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf6e5-217">Remarks</span></span>

<span data-ttu-id="cf6e5-218">Los subobjetos tienen la noción de "Association" o "qué subobjeto va a partir de la exportación".</span><span class="sxs-lookup"><span data-stu-id="cf6e5-218">Subobjects have the notion of "association", or "which subobject goes with which export".</span></span>

<span data-ttu-id="cf6e5-219">Al especificar los subobjetos mediante el código del sombreador, la opción de "qué subobjeto se dirige a la exportación" sigue las reglas que se describen en la [especificación DXR](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span><span class="sxs-lookup"><span data-stu-id="cf6e5-219">When specifying subobjects through shader code, the choice of "which subobject goes with which export" follows the rules as outlined in the [DXR specification](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html#subobject-association-behavior).</span></span> <span data-ttu-id="cf6e5-220">En concreto, supongamos que una aplicación tiene alguna exportación.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-220">In particular, suppose an application has some export.</span></span> <span data-ttu-id="cf6e5-221">Si una aplicación asocia esa exportación con la firma raíz a mediante el código del sombreador y la firma raíz B a través del código de la aplicación, B es la que se usa.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-221">If an application associates that export with root signature A through shader-code and root signature B through application code, B is the one that gets used.</span></span> <span data-ttu-id="cf6e5-222">El diseño de "uso B" en lugar de "producir un error" proporciona a las aplicaciones la capacidad de invalidar las asociaciones de DXIL de forma cómoda mediante el código de aplicación, en lugar de forzarse a que vuelvan a compilar los sombreadores para resolver las cosas que no coinciden.</span><span class="sxs-lookup"><span data-stu-id="cf6e5-222">The design of "use B" instead of "produce an error" gives applications the ability to conveniently override DXIL associations using application code, rather than be forced to recompile shaders to resolve mismatching things.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf6e5-223">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf6e5-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf6e5-224">Publicación de blog para desarrolladores de DirectX "novedad en D3D12 – DirectX raytracing (DXR) ahora admite subobjetos de biblioteca"</span><span class="sxs-lookup"><span data-stu-id="cf6e5-224">DirectX Developer Blog post "New in D3D12 – DirectX Raytracing (DXR) now supports library subobjects"</span></span>](https://devblogs.microsoft.com/directx/dxr-library-subobjects/)

[<span data-ttu-id="cf6e5-225">Especificación funcional de DirectX raytracing (DXR)</span><span class="sxs-lookup"><span data-stu-id="cf6e5-225">DirectX Raytracing (DXR) Functional Spec</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[<span data-ttu-id="cf6e5-226">Ejemplo: D3D12RaytracingLibrarySubobjects</span><span class="sxs-lookup"><span data-stu-id="cf6e5-226">Sample: D3D12RaytracingLibrarySubobjects</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12Raytracing/src/D3D12RaytracingLibrarySubobjects)

</dt> </dl>