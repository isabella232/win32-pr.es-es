---
title: Constantes de sombreador (HLSL)
description: En el modelo de sombreador 4, las constantes de sombreador se almacenan en uno o varios recursos de búfer en la memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- búfer de constantes
- búfer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800722"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="82ad2-107">Constantes de sombreador (HLSL)</span><span class="sxs-lookup"><span data-stu-id="82ad2-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="82ad2-108">En el modelo de sombreador 4, las constantes de sombreador se almacenan en uno o varios recursos de búfer en la memoria.</span><span class="sxs-lookup"><span data-stu-id="82ad2-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="82ad2-109">Se pueden organizar en dos tipos de búferes: búferes de constantes (cbuffers) y búferes de textura (tbuffers).</span><span class="sxs-lookup"><span data-stu-id="82ad2-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="82ad2-110">Los búferes de constantes están optimizados para el uso de variables constantes, que se caracteriza por un acceso de baja latencia y una actualización más frecuente de la CPU.</span><span class="sxs-lookup"><span data-stu-id="82ad2-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="82ad2-111">Por esta razón, se aplican restricciones de acceso, diseño y tamaño adicionales a estos recursos.</span><span class="sxs-lookup"><span data-stu-id="82ad2-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="82ad2-112">Se tiene acceso a los búferes de texturas como las texturas y funcionan mejor para los datos indexados de forma arbitraria.</span><span class="sxs-lookup"><span data-stu-id="82ad2-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="82ad2-113">Independientemente del tipo de recurso que use, no hay límite para el número de búferes de constantes o de texturas que puede crear una aplicación.</span><span class="sxs-lookup"><span data-stu-id="82ad2-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="82ad2-114">Declarar un búfer de constantes o un búfer de textura es muy similar a una declaración de estructura en C, con la adición de las palabras clave **Register** y **packoffset** para asignar manualmente los registros o empaquetar los datos.</span><span class="sxs-lookup"><span data-stu-id="82ad2-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ad2-115">*BufferType* \[ *Nombre* \] de \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="82ad2-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="82ad2-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82ad2-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ad2-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="82ad2-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="82ad2-118">\[en \] el tipo de búfer.</span><span class="sxs-lookup"><span data-stu-id="82ad2-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="82ad2-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="82ad2-119">BufferType</span></span> | <span data-ttu-id="82ad2-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ad2-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="82ad2-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="82ad2-121">cbuffer</span></span>    | <span data-ttu-id="82ad2-122">búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="82ad2-122">constant buffer</span></span> |
| <span data-ttu-id="82ad2-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="82ad2-123">tbuffer</span></span>    | <span data-ttu-id="82ad2-124">búfer de textura</span><span class="sxs-lookup"><span data-stu-id="82ad2-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="82ad2-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="82ad2-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="82ad2-126">\[en \] una cadena ASCII opcional que contiene un nombre de búfer único.</span><span class="sxs-lookup"><span data-stu-id="82ad2-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="82ad2-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**registro**(b \# )</span><span class="sxs-lookup"><span data-stu-id="82ad2-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="82ad2-128">\[en la \] palabra clave opcional, se usa para empaquetar manualmente los datos constantes.</span><span class="sxs-lookup"><span data-stu-id="82ad2-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="82ad2-129">Las constantes se pueden empaquetar en un registro solo en un búfer de constantes, donde el registro de inicio se proporciona mediante el número de registro ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="82ad2-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="82ad2-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="82ad2-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="82ad2-131">\[en \] la declaración de variable, similar a una declaración de miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="82ad2-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="82ad2-132">Puede ser cualquier objeto de tipo HLSL o de efecto (excepto una textura o un objeto de muestra).</span><span class="sxs-lookup"><span data-stu-id="82ad2-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="82ad2-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)</span><span class="sxs-lookup"><span data-stu-id="82ad2-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="82ad2-134">\[en la \] palabra clave opcional, se usa para empaquetar manualmente los datos constantes.</span><span class="sxs-lookup"><span data-stu-id="82ad2-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="82ad2-135">Las constantes se pueden empaquetar en cualquier búfer de constantes, donde () proporciona el número de registro *\#* .</span><span class="sxs-lookup"><span data-stu-id="82ad2-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="82ad2-136">El empaquetado de subcomponentes (con xyzw permutación) está disponible para las constantes cuyo tamaño cabe en un solo registro (no cruce un límite de registro).</span><span class="sxs-lookup"><span data-stu-id="82ad2-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="82ad2-137">Por ejemplo, una FLOAT4 no se pudo empaquetar en un solo registro a partir del componente y porque no cabe en un registro de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="82ad2-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82ad2-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82ad2-138">Remarks</span></span>

<span data-ttu-id="82ad2-139">Los búferes de constantes reducen el ancho de banda necesario para actualizar las constantes de sombreador al permitir que las constantes de sombreador se agrupen y se confirmen al mismo tiempo, en lugar de realizar llamadas individuales para confirmar cada constante por separado.</span><span class="sxs-lookup"><span data-stu-id="82ad2-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="82ad2-140">Un búfer de constantes es un recurso de búfer especializado al que se tiene acceso como un búfer.</span><span class="sxs-lookup"><span data-stu-id="82ad2-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="82ad2-141">Cada búfer de constantes puede contener hasta 4096 [vectores](dx-graphics-hlsl-vector.md); cada vector contiene valores de hasta 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="82ad2-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="82ad2-142">Puede enlazar hasta 14 búferes de constantes por fase de canalización (2 ranuras adicionales se reservan para uso interno).</span><span class="sxs-lookup"><span data-stu-id="82ad2-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="82ad2-143">Un búfer de textura es un recurso de búfer especializado al que se tiene acceso como una textura.</span><span class="sxs-lookup"><span data-stu-id="82ad2-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="82ad2-144">El acceso de textura (en comparación con el acceso al búfer) puede mejorar el rendimiento de los datos indexados de forma arbitraria.</span><span class="sxs-lookup"><span data-stu-id="82ad2-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="82ad2-145">Puede enlazar hasta 128 búferes de textura por fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="82ad2-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="82ad2-146">Un recurso de búfer está diseñado para minimizar la sobrecarga que supone establecer constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82ad2-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="82ad2-147">El marco de efecto (consulte la [**interfaz ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) administrará los búferes de constante y de textura, o puede usar la API de Direct3D para actualizar los búferes (consulte [copia y acceso a los datos de recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obtener información).</span><span class="sxs-lookup"><span data-stu-id="82ad2-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="82ad2-148">Una aplicación también puede copiar datos de otro búfer (como un destino de representación o un destino de flujo de salida) en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="82ad2-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="82ad2-149">Para obtener más información sobre el uso de búferes de constantes en una aplicación D3D10, consulte [tipos de recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) y [creación de recursos de búfer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="82ad2-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="82ad2-150">Para obtener información sobre Morel sobre el uso de búferes de constantes en una aplicación de D3D11, vea [Introducción a los búferes en Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) y [Cómo: crear un búfer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="82ad2-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="82ad2-151">Un búfer de constantes no requiere que una [vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) esté enlazada a la canalización.</span><span class="sxs-lookup"><span data-stu-id="82ad2-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="82ad2-152">Sin embargo, un búfer de textura requiere una vista y debe estar enlazada a una ranura de textura (o debe estar enlazada con [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) cuando se usa un efecto).</span><span class="sxs-lookup"><span data-stu-id="82ad2-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="82ad2-153">Hay dos maneras de empaquetar datos de constantes: mediante las palabras clave [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) y [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="82ad2-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ad2-154">Diferencias entre Direct3D 9 y Direct3D 10 y 11:</span><span class="sxs-lookup"><span data-stu-id="82ad2-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span><br/> <span data-ttu-id="82ad2-155">A diferencia de la asignación automática de constantes en Direct3D 9, que no realizaban el empaquetado y, en su lugar, asignaba cada variable a un conjunto de registros de FLOAT4, las variables de constantes de HLSL siguen las reglas de empaquetado en Direct3D 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="82ad2-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span><br/> |



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="82ad2-156">Organizar búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="82ad2-156">Organizing constant buffers</span></span>

<span data-ttu-id="82ad2-157">Los búferes de constantes reducen el ancho de banda necesario para actualizar las constantes de sombreador al permitir que las constantes de sombreador se agrupen y se confirmen al mismo tiempo, en lugar de realizar llamadas individuales para confirmar cada constante por separado.</span><span class="sxs-lookup"><span data-stu-id="82ad2-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="82ad2-158">La mejor forma de usar búferes de constantes con eficiencia es organizar las variables de sombreador en búferes de constantes según su frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="82ad2-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="82ad2-159">Esto permite a una aplicación minimizar el ancho de banda necesario para actualizar las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82ad2-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="82ad2-160">Por ejemplo, un sombreador podría declarar dos búferes de constantes y organizar los datos en cada uno de ellos según su frecuencia de actualización: los datos que deben actualizarse por objeto (como una matriz universal) se agrupan en un búfer de constantes que se puede actualizar para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="82ad2-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="82ad2-161">Esto es independiente de los datos que caracterizan una escena y, por tanto, es probable que se actualice con mucha menos frecuencia (cuando cambie la escena).</span><span class="sxs-lookup"><span data-stu-id="82ad2-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="82ad2-162">Búferes de constantes predeterminados</span><span class="sxs-lookup"><span data-stu-id="82ad2-162">Default constant buffers</span></span>

<span data-ttu-id="82ad2-163">Hay dos búferes de constantes predeterminados disponibles, $Global y $Param.</span><span class="sxs-lookup"><span data-stu-id="82ad2-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="82ad2-164">Las variables que se colocan en el ámbito global se agregan implícitamente al $Global CBuffer, mediante el mismo método de empaquetado que se usa para cbuffers.</span><span class="sxs-lookup"><span data-stu-id="82ad2-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="82ad2-165">Los parámetros uniformes en la lista de parámetros de una función aparecen en el búfer de constantes de $Param cuando un sombreador se compila fuera del marco de trabajo de efectos.</span><span class="sxs-lookup"><span data-stu-id="82ad2-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="82ad2-166">Cuando se compilan dentro del marco de trabajo de Effects, todos los uniformes deben resolverse en las variables definidas en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="82ad2-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="82ad2-167">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82ad2-167">Examples</span></span>

<span data-ttu-id="82ad2-168">Este es un ejemplo de ejemplo de [Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que es un búfer de textura que se compone de una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="82ad2-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="82ad2-169">Esta declaración de ejemplo asigna manualmente un búfer de constantes para que se inicie en un registro determinado y también empaqueta elementos determinados por subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="82ad2-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="82ad2-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82ad2-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82ad2-171">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="82ad2-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

