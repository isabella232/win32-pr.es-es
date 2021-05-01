---
title: Creación de una firma raíz
description: Las firmas raíz son una estructura de datos compleja que contiene estructuras anidadas.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3705f4e1a0a88841560d67d5904e0f1b5dabd3f8
ms.sourcegitcommit: a0cb986d5694b69d4a65b7d42a22694d02a6e83a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108296340"
---
# <a name="creating-a-root-signature"></a><span data-ttu-id="279fc-103">Creación de una firma raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-103">Creating a Root Signature</span></span>

<span data-ttu-id="279fc-104">Las firmas raíz son una estructura de datos compleja que contiene estructuras anidadas.</span><span class="sxs-lookup"><span data-stu-id="279fc-104">Root signatures are a complex data structure containing nested structures.</span></span> <span data-ttu-id="279fc-105">Se pueden definir mediante programación mediante la definición de estructura de datos siguiente (que incluye métodos para ayudar a inicializar miembros).</span><span class="sxs-lookup"><span data-stu-id="279fc-105">These can be defined programmatically using the data structure definition below (which includes methods to help initialize members).</span></span> <span data-ttu-id="279fc-106">Como alternativa, se pueden crear en lenguaje de sombreado de alto nivel (HLSL), lo que ofrece la ventaja de que el compilador validará pronto que el diseño es compatible con el sombreador.</span><span class="sxs-lookup"><span data-stu-id="279fc-106">Alternatively, they can be authored in High Level Shading Language (HLSL) – giving the advantage that the compiler will validate early that the layout is compatible with the shader.</span></span>

<span data-ttu-id="279fc-107">La API para crear una firma raíz toma una versión serializada (independiente, sin puntero) de la descripción del diseño que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="279fc-107">The API for creating a root signature takes in a serialized (self contained, pointer free) version of the layout description described below.</span></span> <span data-ttu-id="279fc-108">Se proporciona un método para generar esta versión serializada a partir de la estructura de datos de C++, pero otra manera de obtener una definición de firma raíz serializada es recuperarla de un sombreador compilado con una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-108">A method is provided for generating this serialized version from the C++ data structure, but another way to obtain a serialized root signature definition is to retrieve it from a shader that has been compiled with a root signature.</span></span>

<span data-ttu-id="279fc-109">Si desea aprovechar las optimizaciones de controladores para los datos y descriptores de firma raíz, consulte [Root Signature Version 1.1 (Versión de firma raíz 1.1).](root-signature-version-1-1.md)</span><span class="sxs-lookup"><span data-stu-id="279fc-109">If you wish to take advantage of driver optimizations for root signature descriptors and data, refer to [Root Signature Version 1.1](root-signature-version-1-1.md)</span></span>

-   [<span data-ttu-id="279fc-110">Tipos de enlace de tabla descriptor</span><span class="sxs-lookup"><span data-stu-id="279fc-110">Descriptor Table Bind Types</span></span>](#descriptor-table-bind-types)
-   [<span data-ttu-id="279fc-111">Intervalo de descriptor</span><span class="sxs-lookup"><span data-stu-id="279fc-111">Descriptor Range</span></span>](#descriptor-range)
-   [<span data-ttu-id="279fc-112">Diseño de tabla descriptor</span><span class="sxs-lookup"><span data-stu-id="279fc-112">Descriptor Table Layout</span></span>](#descriptor-table-layout)
-   [<span data-ttu-id="279fc-113">Constantes raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-113">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="279fc-114">Descriptor raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-114">Root Descriptor</span></span>](#root-descriptor)
-   [<span data-ttu-id="279fc-115">Visibilidad del sombreador</span><span class="sxs-lookup"><span data-stu-id="279fc-115">Shader Visibility</span></span>](#shader-visibility)
-   [<span data-ttu-id="279fc-116">Definición de firma raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-116">Root Signature Definition</span></span>](#root-signature-definition)
-   [<span data-ttu-id="279fc-117">Serialización y deserialización de la estructura de datos de firma raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-117">Root Signature Data Structure Serialization / Deserialization</span></span>](/windows)
-   [<span data-ttu-id="279fc-118">API de creación de firmas raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-118">Root Signature Creation API</span></span>](#root-signature-creation-api)
-   [<span data-ttu-id="279fc-119">Firma raíz en objetos de estado de canalización</span><span class="sxs-lookup"><span data-stu-id="279fc-119">Root Signature in Pipeline State Objects</span></span>](#root-signature-in-pipeline-state-objects)
-   [<span data-ttu-id="279fc-120">Código para definir una firma raíz de la versión 1.1</span><span class="sxs-lookup"><span data-stu-id="279fc-120">Code for Defining a Version 1.1 Root Signature</span></span>](#code-for-defining-a-version-11-root-signature)
-   [<span data-ttu-id="279fc-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="279fc-121">Related topics</span></span>](#related-topics)

## <a name="descriptor-table-bind-types"></a><span data-ttu-id="279fc-122">Tipos de enlace de tabla descriptor</span><span class="sxs-lookup"><span data-stu-id="279fc-122">Descriptor Table Bind Types</span></span>

<span data-ttu-id="279fc-123">La enumeración [**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) define los tipos de descriptores a los que se puede hacer referencia como parte de una definición de diseño de tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="279fc-123">The enum [**D3D12\_DESCRIPTOR\_RANGE\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) defines the types of descriptors that can be referenced as part of a descriptor table layout definition.</span></span>

<span data-ttu-id="279fc-124">Es un intervalo para que, por ejemplo, si parte de una tabla de descriptores tiene 100 SRV, ese intervalo se puede declarar en una entrada en lugar de en 100.</span><span class="sxs-lookup"><span data-stu-id="279fc-124">It is a range so that, for example if part of a descriptor table has 100 SRVs, that range can be declared in one entry rather than 100.</span></span> <span data-ttu-id="279fc-125">Por lo tanto, una definición de tabla de descriptores es una colección de intervalos.</span><span class="sxs-lookup"><span data-stu-id="279fc-125">So a descriptor table definition is a collection of ranges.</span></span>

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a><span data-ttu-id="279fc-126">Intervalo de descriptores</span><span class="sxs-lookup"><span data-stu-id="279fc-126">Descriptor Range</span></span>

<span data-ttu-id="279fc-127">La [**estructura D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) define un intervalo de descriptores de un tipo determinado (como SRV) dentro de una tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="279fc-127">The [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) structure defines a range of descriptors of a given type (such as SRVs) within a descriptor table.</span></span>

<span data-ttu-id="279fc-128">La `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro se puede usar normalmente para el parámetro de `OffsetInDescriptorsFromTableStart` [**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span><span class="sxs-lookup"><span data-stu-id="279fc-128">The `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro can typically be used for the `OffsetInDescriptorsFromTableStart` parameter of [**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range).</span></span> <span data-ttu-id="279fc-129">Esto significa anexar el intervalo de descriptor que se define después del anterior en la tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="279fc-129">This means append the descriptor range being defined after the previous one in the descriptor table.</span></span> <span data-ttu-id="279fc-130">Si la aplicación quiere usar descriptores de alias o, por algún motivo, quiere omitir ranuras, puede establecer en el `OffsetInDescriptorsFromTableStart` desplazamiento deseado.</span><span class="sxs-lookup"><span data-stu-id="279fc-130">If the application wants to alias descriptors or for some reason wants to skip slots, it can set `OffsetInDescriptorsFromTableStart` to whatever offset is desired.</span></span> <span data-ttu-id="279fc-131">La definición de intervalos superpuestos de distintos tipos no es válida.</span><span class="sxs-lookup"><span data-stu-id="279fc-131">Defining overlapping ranges of different types is invalid.</span></span>

<span data-ttu-id="279fc-132">El conjunto de registros de sombreador especificados por la combinación de , , y no puede tener conflictos ni superponerse entre las declaraciones de una firma raíz que tengan Visibilidad común del sombreador `RangeType` `NumDescriptors` `BaseShaderRegister` `RegisterSpace` [**\_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (consulte la sección de visibilidad del sombreador siguiente).</span><span class="sxs-lookup"><span data-stu-id="279fc-132">The set of shader registers specified by the combination of `RangeType`, `NumDescriptors`, `BaseShaderRegister`, and `RegisterSpace` cannot conflict or overlap across any declarations in a root signature that have common [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) (refer to the shader visibility section below).</span></span>

## <a name="descriptor-table-layout"></a><span data-ttu-id="279fc-133">Diseño de tabla de descriptores</span><span class="sxs-lookup"><span data-stu-id="279fc-133">Descriptor Table Layout</span></span>

<span data-ttu-id="279fc-134">La [**estructura D3D12 \_ ROOT DESCRIPTOR \_ \_ TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) declara el diseño de una tabla de descriptores como una colección de intervalos de descriptores que aparecen uno tras otro en un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="279fc-134">The [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure declares the layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap.</span></span> <span data-ttu-id="279fc-135">No se permiten muestreadores en la misma tabla de descriptores que CBV/UAV/SRV.</span><span class="sxs-lookup"><span data-stu-id="279fc-135">Samplers are not allowed in the same descriptor table as CBV/UAV/SRVs.</span></span>

<span data-ttu-id="279fc-136">Esta estructura se usa cuando el tipo de ranura de firma raíz se establece en `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .</span><span class="sxs-lookup"><span data-stu-id="279fc-136">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE`.</span></span>

<span data-ttu-id="279fc-137">Para establecer una tabla de descriptores de gráficos (CBV, SRV, UAV, Sampler), use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="279fc-137">To set a graphics (CBV, SRV, UAV, Sampler) descriptor table, use [**ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).</span></span>

<span data-ttu-id="279fc-138">Para establecer una tabla de descriptores de proceso, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span><span class="sxs-lookup"><span data-stu-id="279fc-138">To set a compute descriptor table, use [**ID3D12GraphicsCommandList::SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).</span></span>

## <a name="root-constants"></a><span data-ttu-id="279fc-139">Constantes raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-139">Root Constants</span></span>

<span data-ttu-id="279fc-140">La [**estructura D3D12 \_ ROOT \_ CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) declara constantes insertadas en la firma raíz que aparecen en los sombreadores como un búfer constante.</span><span class="sxs-lookup"><span data-stu-id="279fc-140">The [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure declares constants inline in the root signature that appear in shaders as one constant buffer.</span></span>

<span data-ttu-id="279fc-141">Esta estructura se usa cuando el tipo de ranura de firma raíz se establece en `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .</span><span class="sxs-lookup"><span data-stu-id="279fc-141">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS`.</span></span>

## <a name="root-descriptor"></a><span data-ttu-id="279fc-142">Descriptor raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-142">Root Descriptor</span></span>

<span data-ttu-id="279fc-143">La [**estructura D3D12 \_ ROOT \_ DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) declara descriptores (que aparecen en sombreadores) en línea en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-143">The [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure declares descriptors (that appear in shaders) inline in the root signature.</span></span>

<span data-ttu-id="279fc-144">Esta estructura se usa cuando el tipo de ranura de firma raíz se establece en `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` o `D3D12_ROOT_PARAMETER_TYPE_UAV` .</span><span class="sxs-lookup"><span data-stu-id="279fc-144">This struct is used when the root signature slot type is set to `D3D12_ROOT_PARAMETER_TYPE_CBV`, `D3D12_ROOT_PARAMETER_TYPE_SRV` or `D3D12_ROOT_PARAMETER_TYPE_UAV`.</span></span>

## <a name="shader-visibility"></a><span data-ttu-id="279fc-145">Visibilidad del sombreador</span><span class="sxs-lookup"><span data-stu-id="279fc-145">Shader Visibility</span></span>

<span data-ttu-id="279fc-146">El miembro de la enumeración [**\_ SHADER \_ VISIBILITY de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) establecida en el parámetro de visibilidad del sombreador [**de D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina qué sombreadores ven el contenido de una ranura de firma raíz determinada.</span><span class="sxs-lookup"><span data-stu-id="279fc-146">The member of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) enum set into the shader visibility parameter of [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determines which shaders see the contents of a given root signature slot.</span></span> <span data-ttu-id="279fc-147">El proceso siempre \_ usa ALL (ya que solo hay una fase activa).</span><span class="sxs-lookup"><span data-stu-id="279fc-147">Compute always uses \_ALL (since there is only one active stage).</span></span> <span data-ttu-id="279fc-148">Los gráficos pueden elegir, pero si usa ALL, todas las fases del \_ sombreador ven lo que está enlazado en la ranura de firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-148">Graphics can choose, but if it uses \_ALL, all shader stages see whatever is bound at the root signature slot.</span></span>

<span data-ttu-id="279fc-149">Un uso de la visibilidad del sombreador es ayudar con los sombreadores creados que esperan enlaces diferentes por fase de sombreador mediante un espacio de nombres superpuesto.</span><span class="sxs-lookup"><span data-stu-id="279fc-149">One use of shader visibility is to help with shaders that are authored expecting different bindings per shader stage using an overlapping namespace.</span></span> <span data-ttu-id="279fc-150">Por ejemplo, un sombreador de vértices puede declarar:</span><span class="sxs-lookup"><span data-stu-id="279fc-150">For example, a vertex shader may declare:</span></span>

```hlsl
Texture2D foo : register(t0);
```

<span data-ttu-id="279fc-151">y el sombreador de píxeles también puede declarar:</span><span class="sxs-lookup"><span data-stu-id="279fc-151">and the pixel shader may also declare:</span></span>

```hlsl
Texture2D bar : register(t0);
```

<span data-ttu-id="279fc-152">Si la aplicación realiza un enlace de firma raíz a t0 VISIBILITY \_ ALL, ambos sombreadores verán la misma textura.</span><span class="sxs-lookup"><span data-stu-id="279fc-152">If the application makes a root signature binding to t0 VISIBILITY\_ALL, both shaders see the same texture.</span></span> <span data-ttu-id="279fc-153">Si el sombreador define realmente quiere que cada sombreador vea texturas diferentes, puede definir 2 ranuras de firma raíz con \_ VISIBILITY VERTEX y \_ PIXEL.</span><span class="sxs-lookup"><span data-stu-id="279fc-153">If the shader defines actually wants each shader to see different textures, it can define 2 root signature slots with VISIBILITY\_VERTEX and \_PIXEL.</span></span> <span data-ttu-id="279fc-154">Independientemente de la visibilidad que tenga una ranura de firma raíz, siempre tiene el mismo costo (solo en función de lo que sea SlotType) hacia un tamaño de firma raíz máximo fijo.</span><span class="sxs-lookup"><span data-stu-id="279fc-154">No matter what the visibility is on a root signature slot, it always has the same cost (cost only depending on what the SlotType is) towards one fixed maximum root signature size.</span></span>

<span data-ttu-id="279fc-155">En el hardware D3D11 de gama baja, SHADER VISIBILITY también se tiene en cuenta al validar los tamaños de las tablas descriptores en un diseño raíz, ya que algún hardware D3D11 solo puede admitir una cantidad máxima de enlaces por \_ fase.</span><span class="sxs-lookup"><span data-stu-id="279fc-155">On low end D3D11 hardware, SHADER\_VISIBILITY is also taken into account used when validating the sizes of descriptor tables in a root layout, since some D3D11 hardware can only support a maximum amount of bindings per-stage.</span></span> <span data-ttu-id="279fc-156">Estas restricciones solo se imponen cuando se ejecutan en hardware de bajo nivel y no limitan el hardware más moderno en absoluto.</span><span class="sxs-lookup"><span data-stu-id="279fc-156">These restrictions are only imposed when running on low tier hardware and do not limit more modern hardware at all.</span></span>

<span data-ttu-id="279fc-157">Si una firma raíz tiene varias tablas descriptoras definidas que se superponen entre sí en el espacio de nombres (los enlaces de registro al sombreador) y cualquiera de ellas especifica ALL para la visibilidad, el diseño no es válido (se producirá un error en la \_ creación).</span><span class="sxs-lookup"><span data-stu-id="279fc-157">If a root signature has multiple descriptor tables defined that overlap each other in namespace (the register bindings to the shader) and any one of them specifies \_ALL for visibility, the layout is invalid (creation will fail).</span></span>

## <a name="root-signature-definition"></a><span data-ttu-id="279fc-158">Definición de firma raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-158">Root Signature Definition</span></span>

<span data-ttu-id="279fc-159">La estructura [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) puede contener tablas de descriptores y constantes insertadas, cada tipo de ranura definido por la estructura ROOT PARAMETER de [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) y la enumeración [**D3D12 \_ ROOT PARAMETER \_ \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span><span class="sxs-lookup"><span data-stu-id="279fc-159">The [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure can contain descriptor tables and inline constants, each slot type defined by the [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure and the enum [**D3D12\_ROOT\_PARAMETER\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type).</span></span>

<span data-ttu-id="279fc-160">Para iniciar una ranura de firma raíz, consulte los métodos **SetComputeRoot \* \* \*** y **\* \* \* SetGraphicsRoot** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="279fc-160">To initiate a root signature slot, refer to the **SetComputeRoot\*\*\*** and **SetGraphicsRoot\*\*\*** methods of [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

<span data-ttu-id="279fc-161">Los muestreadores estáticos se describen en la firma raíz mediante la estructura [**D3D12 \_ STATIC \_ SAMPLER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="279fc-161">Static samplers are described in the root signature using the [**D3D12\_STATIC\_SAMPLER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

<span data-ttu-id="279fc-162">Una serie de marcas limitan el acceso de determinados sombreadores a la firma raíz; consulte [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="279fc-162">A number of flags limit the access of certain shaders to the root signature, refer to [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

## <a name="root-signature-data-structure-serialization--deserialization"></a><span data-ttu-id="279fc-163">Serialización y deserialización de la estructura de datos de firma raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-163">Root Signature Data Structure Serialization / Deserialization</span></span>

<span data-ttu-id="279fc-164">Los métodos descritos en esta sección se exportan mediante D3D12Core.dll y proporcionan métodos para serializar y deserializar una estructura de datos de firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-164">The methods described in this section are exported by D3D12Core.dll and provide methods for serializing and deserializing a root signature data structure.</span></span>

<span data-ttu-id="279fc-165">El formulario serializado es lo que se pasa a la API al crear una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-165">The serialized form is what is passed into the API when creating a root signature.</span></span> <span data-ttu-id="279fc-166">Si se ha creado un sombreador con una firma raíz en él (cuando se agrega esa funcionalidad), el sombreador compilado ya contendrá una firma raíz serializada en él.</span><span class="sxs-lookup"><span data-stu-id="279fc-166">If a shader has been authored with a root signature in it (when that capability is added), then the compiled shader will contain a serialized root signature in it already.</span></span>

<span data-ttu-id="279fc-167">Si una aplicación genera por procedimientos una estructura de datos [**D3D12 \_ ROOT \_ SIGNATURE \_ DESC,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) debe crear el formulario serializado mediante [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span><span class="sxs-lookup"><span data-stu-id="279fc-167">If an application procedurally generates a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure, it must make the serialized form using [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature).</span></span> <span data-ttu-id="279fc-168">Salida de que se puede pasar a [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="279fc-168">The output of that can be passed into [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span>

<span data-ttu-id="279fc-169">Si una aplicación ya tiene una firma raíz serializada o tiene un sombreador compilado que contiene una firma raíz y desea detectar mediante programación la definición de diseño (conocida como "reflexión"), se puede llamar a [**D3D12CreateRootSignatureDeserializer.**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer)</span><span class="sxs-lookup"><span data-stu-id="279fc-169">If an application has a serialized root signature already, or has a compiled shader that contains a root signature and wishes to programmatically discover the layout definition (known as "reflection"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) can be called.</span></span> <span data-ttu-id="279fc-170">Esto genera una interfaz [**ID3D12RootSignatureDeserializer,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) que contiene un método para devolver la estructura de datos [**D3D12 \_ ROOT SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) deserialización.</span><span class="sxs-lookup"><span data-stu-id="279fc-170">This generates an [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) interface, which contains a method to return the deserialized [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) data structure.</span></span> <span data-ttu-id="279fc-171">La interfaz posee la duración de la estructura de datos deserialización.</span><span class="sxs-lookup"><span data-stu-id="279fc-171">The interface owns the lifetime of the deserialized data structure.</span></span>

## <a name="root-signature-creation-api"></a><span data-ttu-id="279fc-172">API de creación de firmas raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-172">Root Signature Creation API</span></span>

<span data-ttu-id="279fc-173">La API [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) toma una versión serializada de una firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-173">The [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) API takes in a serialized version of a root signature.</span></span>

## <a name="root-signature-in-pipeline-state-objects"></a><span data-ttu-id="279fc-174">Firma raíz en objetos de estado de canalización</span><span class="sxs-lookup"><span data-stu-id="279fc-174">Root Signature in Pipeline State Objects</span></span>

<span data-ttu-id="279fc-175">Los métodos para crear el estado de canalización ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) toman una interfaz [**OPCIONAL ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) como parámetro de entrada (almacenado en una estructura [**\_ \_ \_ \_ DESC DESC DE ESTADO DE CANALIZACIÓN DE GRÁFICOS D3D12).**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)</span><span class="sxs-lookup"><span data-stu-id="279fc-175">The methods to create pipeline state ([**ID3D12Device::CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) and [**ID3D12Device::CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) take an optional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) interface as an input parameter (stored in a [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) structure).</span></span> <span data-ttu-id="279fc-176">Esto invalidará cualquier firma raíz que ya se encuentra en los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="279fc-176">This will override any root signature already in the shaders.</span></span>

<span data-ttu-id="279fc-177">Si se pasa una firma raíz a uno de los métodos de estado de la canalización de creación, esta firma raíz se valida con todos los sombreadores del PSO por razones de compatibilidad y se le da al controlador que se va a usar con todos los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="279fc-177">If a root signature is passed into one of the create pipeline state methods, this root signature is validated against all the shaders in the PSO for compatibility and given to the driver to use with all the shaders.</span></span> <span data-ttu-id="279fc-178">Si alguno de los sombreadores tiene una firma raíz diferente, se reemplaza por la firma raíz que se pasa en la API.</span><span class="sxs-lookup"><span data-stu-id="279fc-178">If any of the shaders has a different root signature in it, it gets replaced by the root signature passed in at the API.</span></span> <span data-ttu-id="279fc-179">Si no se pasa una firma raíz, todos los sombreadores pasados deben tener una firma raíz y deben coincidir; esto se le dará al controlador.</span><span class="sxs-lookup"><span data-stu-id="279fc-179">If a root signature is not passed in, all shaders passed in must have a root signature and they must match – this will be given to the driver.</span></span> <span data-ttu-id="279fc-180">Establecer un PSO en una lista o agrupación de comandos no cambia la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="279fc-180">Setting a PSO on a command list or bundle does not change the root signature.</span></span> <span data-ttu-id="279fc-181">Esto se logra mediante los [**métodos SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) y [**SetComputeRootSignature.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)</span><span class="sxs-lookup"><span data-stu-id="279fc-181">That is accomplished by the methods [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) and [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature).</span></span> <span data-ttu-id="279fc-182">En el momento en que se invoca draw(graphics)/dispatch(compute), la aplicación debe asegurarse de que el PSO actual coincide con la firma raíz actual. de lo contrario, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="279fc-182">By the time draw(graphics)/dispatch(compute) is invoked, the application must ensure that the current PSO matches the current root signature; otherwise, the behavior is undefined.</span></span>

## <a name="code-for-defining-a-version-11-root-signature"></a><span data-ttu-id="279fc-183">Código para definir una firma raíz de la versión 1.1</span><span class="sxs-lookup"><span data-stu-id="279fc-183">Code for Defining a Version 1.1 Root Signature</span></span>

<span data-ttu-id="279fc-184">En el ejemplo siguiente se muestra cómo crear una firma raíz con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="279fc-184">The example below shows how to create a root signature with the following format:</span></span>



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="279fc-185">**RootParameterIndex**</span><span class="sxs-lookup"><span data-stu-id="279fc-185">**RootParameterIndex**</span></span> | <span data-ttu-id="279fc-186">**Contents**</span><span class="sxs-lookup"><span data-stu-id="279fc-186">**Contents**</span></span>                                   |                                              |
| <span data-ttu-id="279fc-187">\[0\]</span><span class="sxs-lookup"><span data-stu-id="279fc-187">\[0\]</span></span>                  | <span data-ttu-id="279fc-188">Constantes raíz: { b2 }</span><span class="sxs-lookup"><span data-stu-id="279fc-188">Root constants: { b2 }</span></span>                         | <span data-ttu-id="279fc-189">(1 CBV)</span><span class="sxs-lookup"><span data-stu-id="279fc-189">(1 CBV)</span></span>                                      |
| <span data-ttu-id="279fc-190">\[1\]</span><span class="sxs-lookup"><span data-stu-id="279fc-190">\[1\]</span></span>                  | <span data-ttu-id="279fc-191">Tabla de descriptores: { t2-t7, u0-u3 }</span><span class="sxs-lookup"><span data-stu-id="279fc-191">Descriptor table: { t2-t7, u0-u3 }</span></span>             | <span data-ttu-id="279fc-192">(6 SRV + 4 UAV)</span><span class="sxs-lookup"><span data-stu-id="279fc-192">(6 SRVs + 4 UAVs)</span></span>                            |
| <span data-ttu-id="279fc-193">\[2\]</span><span class="sxs-lookup"><span data-stu-id="279fc-193">\[2\]</span></span>                  | <span data-ttu-id="279fc-194">CBV raíz: { b0 }</span><span class="sxs-lookup"><span data-stu-id="279fc-194">Root CBV: { b0 }</span></span>                               | <span data-ttu-id="279fc-195">(1 CBV, datos estáticos)</span><span class="sxs-lookup"><span data-stu-id="279fc-195">(1 CBV, static data)</span></span>                         |
| <span data-ttu-id="279fc-196">\[3\]</span><span class="sxs-lookup"><span data-stu-id="279fc-196">\[3\]</span></span>                  | <span data-ttu-id="279fc-197">Tabla de descriptores: { s0-s1 }</span><span class="sxs-lookup"><span data-stu-id="279fc-197">Descriptor table: { s0-s1 }</span></span>                    | <span data-ttu-id="279fc-198">(2 muestreadores)</span><span class="sxs-lookup"><span data-stu-id="279fc-198">(2 Samplers)</span></span>                                 |
| <span data-ttu-id="279fc-199">\[4\]</span><span class="sxs-lookup"><span data-stu-id="279fc-199">\[4\]</span></span>                  | <span data-ttu-id="279fc-200">Tabla de descriptores: { t8 - sin enlazar }</span><span class="sxs-lookup"><span data-stu-id="279fc-200">Descriptor table: { t8 - unbounded }</span></span>           | <span data-ttu-id="279fc-201">(sin enlazar \# de SRV, descriptores volátiles)</span><span class="sxs-lookup"><span data-stu-id="279fc-201">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="279fc-202">\[5\]</span><span class="sxs-lookup"><span data-stu-id="279fc-202">\[5\]</span></span>                  | <span data-ttu-id="279fc-203">Tabla de descriptores: { (t0, space1) - unbounded }</span><span class="sxs-lookup"><span data-stu-id="279fc-203">Descriptor table: { (t0, space1) - unbounded }</span></span> | <span data-ttu-id="279fc-204">(sin enlazar \# de SRV, descriptores volátiles)</span><span class="sxs-lookup"><span data-stu-id="279fc-204">(unbounded \# of SRVs, volatile descriptors)</span></span> |
| <span data-ttu-id="279fc-205">\[6\]</span><span class="sxs-lookup"><span data-stu-id="279fc-205">\[6\]</span></span>                  | <span data-ttu-id="279fc-206">Tabla de descriptores: { b1 }</span><span class="sxs-lookup"><span data-stu-id="279fc-206">Descriptor table: { b1 }</span></span>                       | <span data-ttu-id="279fc-207">(1 CBV, datos estáticos)</span><span class="sxs-lookup"><span data-stu-id="279fc-207">(1 CBV, static data)</span></span>                         |



 

<span data-ttu-id="279fc-208">Si la mayoría de las partes de la firma raíz se usan la mayoría del tiempo, puede ser mejor que tener que cambiar la firma raíz con demasiada frecuencia.</span><span class="sxs-lookup"><span data-stu-id="279fc-208">If most parts of the root signature get used most of the time it can be better than having to switch the root signature too frequently.</span></span> <span data-ttu-id="279fc-209">Las aplicaciones deben ordenar las entradas de la firma raíz de cambiar con más frecuencia a menos.</span><span class="sxs-lookup"><span data-stu-id="279fc-209">Applications should sort entries in the root signature from most frequently changing to least.</span></span> <span data-ttu-id="279fc-210">Cuando una aplicación cambia los enlaces a cualquier parte de la firma raíz, es posible que el controlador tenga que realizar una copia de parte o de todo el estado de la firma raíz, lo que puede convertirse en un costo notrivial cuando se multiplica entre muchos cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="279fc-210">When an app changes the bindings to any part of the root signature, the driver may have to make a copy of some or all of root signature state, which can become a nontrivial cost when multiplied across many state changes.</span></span>

<span data-ttu-id="279fc-211">Además, la firma raíz definirá un muestreador estático que realiza el filtrado de textura anisotropica en el registro de sombreador s3.</span><span class="sxs-lookup"><span data-stu-id="279fc-211">In addition, the root signature will define a static sampler that does anisotropic texture filtering at shader register s3.</span></span>

<span data-ttu-id="279fc-212">Una vez enlazada esta firma raíz, se pueden asignar tablas de descriptores, CBV raíz y constantes al \[ espacio de parámetros 0..6. \]</span><span class="sxs-lookup"><span data-stu-id="279fc-212">After this root signature is bound, descriptor tables, root CBV and constants can be assigned to the \[0..6\] parameter space.</span></span> <span data-ttu-id="279fc-213">Por ejemplo, las tablas de descriptores (intervalos en un montón de descriptores) se pueden enlazar en cada uno de los parámetros raíz 1 y \[ \] \[ 3..6 \] .</span><span class="sxs-lookup"><span data-stu-id="279fc-213">e.g. descriptor tables (ranges in a descriptor heap) can be bound at each of root parameters \[1\] and \[3..6\].</span></span>

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

<span data-ttu-id="279fc-214">El código siguiente muestra cómo se podría usar la firma raíz anterior en una lista de comandos gráficos.</span><span class="sxs-lookup"><span data-stu-id="279fc-214">The following code illustrates how the above root signature might be used on a graphics command list.</span></span>

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a><span data-ttu-id="279fc-215">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="279fc-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="279fc-216">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-216">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="279fc-217">Especificación de firmas de raíz en HLSL</span><span class="sxs-lookup"><span data-stu-id="279fc-217">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="279fc-218">Uso de una firma raíz</span><span class="sxs-lookup"><span data-stu-id="279fc-218">Using a Root Signature</span></span>](using-a-root-signature.md)
</dt> </dl>

 

 
