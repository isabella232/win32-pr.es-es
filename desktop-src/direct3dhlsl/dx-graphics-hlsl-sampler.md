---
title: Tipo de muestra
description: Use la siguiente sintaxis para declarar el estado de la muestra, así como el estado de la comparación de muestra.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Tipo de muestra HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe3cd51c81617632d240dd06df5c8f61b103bf91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077778"
---
# <a name="sampler-type"></a><span data-ttu-id="9dd5a-104">Tipo de muestra</span><span class="sxs-lookup"><span data-stu-id="9dd5a-104">Sampler Type</span></span>

<span data-ttu-id="9dd5a-105">Use la siguiente sintaxis para declarar el estado de la muestra, así como el estado de la comparación de muestra.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dd5a-106">Diferencias entre Direct3D 9 y Direct3D 10 y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="9dd5a-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="9dd5a-107">Esta es la sintaxis de una muestra en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dd5a-108"><em>nombre</em>de muestra  =  <em>SamplerType</em>{Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="9dd5a-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9dd5a-109">La sintaxis de una muestra en Direct3D 10 y versiones posteriores se cambia ligeramente para admitir objetos de textura y matrices de muestra.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dd5a-110"><em>SamplerType nombre [índice]</em>{[<em>state_name = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="9dd5a-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="9dd5a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dd5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd5a-112"><span id="sampler"></span><span id="SAMPLER"></span>muestras</span><span class="sxs-lookup"><span data-stu-id="9dd5a-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="9dd5a-113">Solo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-113">Direct3D 9 only.</span></span> <span data-ttu-id="9dd5a-114">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="9dd5a-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="9dd5a-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="9dd5a-116">Cadena ASCII que identifica de forma única el nombre de la variable de muestra.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="9dd5a-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Ajustar\]*</span><span class="sxs-lookup"><span data-stu-id="9dd5a-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="9dd5a-118">Solo Direct3D 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="9dd5a-119">Tamaño de matriz opcional; un entero positivo mayor o igual que 1.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9dd5a-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span><span class="sxs-lookup"><span data-stu-id="9dd5a-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="9dd5a-121">\[en \] el tipo de muestra, que es uno de los siguientes: *Sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *\_ State Sample*, *SamplerState*.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>



|                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd5a-122">Diferencias entre Direct3D 9 y Direct3D 10 y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="9dd5a-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="9dd5a-123">Direct3D 10 y versiones posteriores admiten un tipo de muestra adicional: *SamplerComparisonState*.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9dd5a-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*\_ variable de textura*>;</span><span class="sxs-lookup"><span data-stu-id="9dd5a-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="9dd5a-125">Solo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-125">Direct3D 9 only.</span></span> <span data-ttu-id="9dd5a-126">Una variable de textura.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-126">A texture variable.</span></span> <span data-ttu-id="9dd5a-127">La palabra clave *Texture* es obligatoria en el lado izquierdo; el nombre de la variable pertenece al lado derecho de la expresión dentro de los corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="9dd5a-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*nombre del estado \_ = \_ valor de estado*</span><span class="sxs-lookup"><span data-stu-id="9dd5a-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="9dd5a-129">\[en \] asignaciones de estado opcionales.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="9dd5a-130">La parte izquierda de una asignación es un nombre de estado, el lado derecho es el valor de estado.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="9dd5a-131">Todas las asignaciones de estado deben aparecer dentro de un bloque de instrucciones (entre llaves).</span><span class="sxs-lookup"><span data-stu-id="9dd5a-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="9dd5a-132">Cada instrucción se separa con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="9dd5a-133">En la tabla siguiente se enumeran los nombres de estado posibles.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-133">The following table lists the possible state names.</span></span>


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



<span data-ttu-id="9dd5a-134">El lado derecho de cada expresión es el valor asignado a cada Estado.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="9dd5a-135">Consulte la [**estructura \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) de la muestra de D3D11 para ver los valores de estado posibles para Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="9dd5a-136">Hay una relación de 1 a 1 entre los nombres de estado y los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="9dd5a-137">Consulte el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dd5a-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dd5a-138">Remarks</span></span>

<span data-ttu-id="9dd5a-139">Cuando se implementa un efecto, el estado de muestra es uno de los diversos tipos de estado que puede necesitar configurar en la canalización para la representación.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="9dd5a-140">Para obtener una lista de todos los Estados posibles que se pueden establecer en un efecto, vea:</span><span class="sxs-lookup"><span data-stu-id="9dd5a-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="9dd5a-141">Direct3D 10 usa [grupos de Estados](/windows/desktop/direct3d10/d3d10-effect-states).</span><span class="sxs-lookup"><span data-stu-id="9dd5a-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="9dd5a-142">Direct3D 9 usa [Estados](/windows/desktop/direct3d9/effect-states)individuales.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="9dd5a-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9dd5a-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dd5a-144">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9dd5a-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="9dd5a-145">Este es un ejemplo parcial de una muestra de Direct3D 9 de <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">ejemplo de BasicHLSL</a>.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="9dd5a-146">Este es un ejemplo parcial de una muestra de Direct3D 10 de <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">ejemplo de BasicHLSL10</a>.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9dd5a-147">Este es un ejemplo parcial de cómo declarar el estado de la comparación de muestra y llamar a una muestra de comparación en Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="9dd5a-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a><span data-ttu-id="9dd5a-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dd5a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd5a-149">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dd5a-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

