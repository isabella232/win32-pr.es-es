---
title: Constantes de sombreador (HLSL)
description: En El modelo de sombreador 4, las constantes del sombreador se almacenan en uno o varios recursos de búfer en memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- búfer constante
- búfer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f314be4b8da98ff80bd7404c270479855e13fb6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129964"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="d41a1-107">Constantes de sombreador (HLSL)</span><span class="sxs-lookup"><span data-stu-id="d41a1-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="d41a1-108">En El modelo de sombreador 4, las constantes del sombreador se almacenan en uno o varios recursos de búfer en memoria.</span><span class="sxs-lookup"><span data-stu-id="d41a1-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="d41a1-109">Se pueden organizar en dos tipos de búferes: búferes constantes (cbuffers) y búferes de textura (tbuffers).</span><span class="sxs-lookup"><span data-stu-id="d41a1-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="d41a1-110">Los búferes constantes están optimizados para el uso constante-variable, que se caracteriza por el acceso de menor latencia y una actualización más frecuente desde la CPU.</span><span class="sxs-lookup"><span data-stu-id="d41a1-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="d41a1-111">Por este motivo, se aplican restricciones de tamaño, diseño y acceso adicionales a estos recursos.</span><span class="sxs-lookup"><span data-stu-id="d41a1-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="d41a1-112">Se accede a los búferes de textura como texturas y se realiza mejor para los datos indexados arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="d41a1-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="d41a1-113">Independientemente del tipo de recurso que use, no hay ningún límite en el número de búferes constantes o búferes de textura que una aplicación puede crear.</span><span class="sxs-lookup"><span data-stu-id="d41a1-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="d41a1-114">Declarar un búfer constante o un búfer de textura se parece mucho a una declaración de estructura en C, con la adición de las palabras clave **register** y **packoffset** para asignar manualmente registros o empaquetar datos.</span><span class="sxs-lookup"><span data-stu-id="d41a1-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d41a1-115">*BufferType* \[ *Nombre* \] \[: **register**(b \# ) { \] *VariableDeclaration* \[ : **packoffset**(c \# .xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="d41a1-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d41a1-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d41a1-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41a1-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="d41a1-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="d41a1-118">\[en \] El tipo de búfer.</span><span class="sxs-lookup"><span data-stu-id="d41a1-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="d41a1-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="d41a1-119">BufferType</span></span> | <span data-ttu-id="d41a1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d41a1-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="d41a1-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="d41a1-121">cbuffer</span></span>    | <span data-ttu-id="d41a1-122">búfer constante</span><span class="sxs-lookup"><span data-stu-id="d41a1-122">constant buffer</span></span> |
| <span data-ttu-id="d41a1-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="d41a1-123">tbuffer</span></span>    | <span data-ttu-id="d41a1-124">búfer de textura</span><span class="sxs-lookup"><span data-stu-id="d41a1-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d41a1-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*</span><span class="sxs-lookup"><span data-stu-id="d41a1-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="d41a1-126">\[en \] Cadena ASCII opcional que contiene un nombre de búfer único.</span><span class="sxs-lookup"><span data-stu-id="d41a1-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="d41a1-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )</span><span class="sxs-lookup"><span data-stu-id="d41a1-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="d41a1-128">\[en \] la palabra clave Optional, se usa para empaquetar manualmente los datos constantes.</span><span class="sxs-lookup"><span data-stu-id="d41a1-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="d41a1-129">Las constantes se pueden empaquetar en un registro solo en un búfer constante, donde el registro inicial lo da el número de registro ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="d41a1-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="d41a1-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="d41a1-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="d41a1-131">\[en \] Declaración de variable, similar a una declaración de miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="d41a1-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="d41a1-132">Puede ser cualquier tipo HLSL o objeto de efecto (excepto una textura o un objeto sampler).</span><span class="sxs-lookup"><span data-stu-id="d41a1-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="d41a1-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)</span><span class="sxs-lookup"><span data-stu-id="d41a1-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="d41a1-134">\[en \] la palabra clave Optional, se usa para empaquetar manualmente los datos constantes.</span><span class="sxs-lookup"><span data-stu-id="d41a1-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="d41a1-135">Las constantes se pueden empaquetar en cualquier búfer constante, donde el número de registro lo da ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="d41a1-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="d41a1-136">El empaquetado de sub component (con xyzw swling) está disponible para las constantes cuyo tamaño cabe dentro de un único registro (no cruza un límite de registro).</span><span class="sxs-lookup"><span data-stu-id="d41a1-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="d41a1-137">Por ejemplo, no se pudo empaquetar float4 en un único registro a partir del componente y porque no cabría en un registro de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="d41a1-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d41a1-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d41a1-138">Remarks</span></span>

<span data-ttu-id="d41a1-139">Los búferes constantes reducen el ancho de banda necesario para actualizar las constantes del sombreador, ya que permiten agrupar y confirmar constantes de sombreador al mismo tiempo en lugar de realizar llamadas individuales para confirmar cada constante por separado.</span><span class="sxs-lookup"><span data-stu-id="d41a1-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="d41a1-140">Un búfer constante es un recurso de búfer especializado al que se accede como un búfer.</span><span class="sxs-lookup"><span data-stu-id="d41a1-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="d41a1-141">Cada búfer constante puede contener hasta 4096 [vectores](dx-graphics-hlsl-vector.md); cada vector contiene hasta cuatro valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d41a1-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="d41a1-142">Puede enlazar hasta 14 búferes constantes por fase de canalización (2 ranuras adicionales están reservadas para uso interno).</span><span class="sxs-lookup"><span data-stu-id="d41a1-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="d41a1-143">Un búfer de textura es un recurso de búfer especializado al que se accede como una textura.</span><span class="sxs-lookup"><span data-stu-id="d41a1-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="d41a1-144">El acceso de textura (en comparación con el acceso al búfer) puede tener un mejor rendimiento para los datos indexados arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="d41a1-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="d41a1-145">Puede enlazar hasta 128 búferes de textura por fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="d41a1-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="d41a1-146">Un recurso de búfer está diseñado para minimizar la sobrecarga de establecer constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d41a1-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="d41a1-147">El marco de trabajo de efectos (vea [**Id3D10Effect Interface)**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)administrará la actualización de búferes de constantes y texturas, o puede usar la API de Direct3D para actualizar los búferes (consulte Copiar y acceder a los datos de recursos [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obtener información).</span><span class="sxs-lookup"><span data-stu-id="d41a1-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="d41a1-148">Una aplicación también puede copiar datos de otro búfer (como un destino de representación o un destino de salida de flujo) en un búfer constante.</span><span class="sxs-lookup"><span data-stu-id="d41a1-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="d41a1-149">Para obtener más información sobre el uso de búferes constantes en una aplicación D3D10, vea Tipos de [recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) y Creación de recursos de [búfer (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)</span><span class="sxs-lookup"><span data-stu-id="d41a1-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="d41a1-150">Para obtener más información sobre el uso de búferes constantes en una aplicación D3D11, vea Introducción a los búferes en [Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) y [Cómo:](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)Crear un búfer constante .</span><span class="sxs-lookup"><span data-stu-id="d41a1-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="d41a1-151">Un búfer constante no requiere que [una vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) esté enlazada a la canalización.</span><span class="sxs-lookup"><span data-stu-id="d41a1-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="d41a1-152">Sin embargo, un búfer de textura requiere una vista y debe enlazarse a una ranura de textura (o debe enlazarse con [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) cuando se usa un efecto).</span><span class="sxs-lookup"><span data-stu-id="d41a1-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="d41a1-153">Hay dos maneras de empaquetar datos de constantes: mediante las palabras clave [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) y [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)</span><span class="sxs-lookup"><span data-stu-id="d41a1-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>

<span data-ttu-id="d41a1-154">Diferencias entre Direct3D 9 y Direct3D 10 y 11:</span><span class="sxs-lookup"><span data-stu-id="d41a1-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span>

- <span data-ttu-id="d41a1-155">A diferencia de la asignación automática de constantes en Direct3D 9, que no realizaba el empaquetado y, en su lugar, asignaba cada variable a un conjunto de registros float4, las variables constantes HLSL siguen las reglas de empaquetado en Direct3D 10 y 11.</span><span class="sxs-lookup"><span data-stu-id="d41a1-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span>



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="d41a1-156">Organización de búferes constantes</span><span class="sxs-lookup"><span data-stu-id="d41a1-156">Organizing constant buffers</span></span>

<span data-ttu-id="d41a1-157">Los búferes constantes reducen el ancho de banda necesario para actualizar las constantes del sombreador, ya que permiten agrupar y confirmar constantes de sombreador al mismo tiempo en lugar de realizar llamadas individuales para confirmar cada constante por separado.</span><span class="sxs-lookup"><span data-stu-id="d41a1-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="d41a1-158">La mejor forma de usar búferes de constantes con eficiencia es organizar las variables de sombreador en búferes de constantes según su frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="d41a1-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="d41a1-159">Esto permite que una aplicación minimice el ancho de banda necesario para actualizar las constantes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d41a1-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="d41a1-160">Por ejemplo, un sombreador podría declarar dos búferes constantes y organizar los datos en cada uno en función de su frecuencia de actualización: los datos que deben actualizarse por objeto (como una matriz mundial) se agrupan en un búfer constante que se puede actualizar para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="d41a1-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="d41a1-161">Esto es independiente de los datos que caracteriza una escena y, por tanto, es probable que se actualice con mucha menos frecuencia (cuando cambia la escena).</span><span class="sxs-lookup"><span data-stu-id="d41a1-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


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



### <a name="default-constant-buffers"></a><span data-ttu-id="d41a1-162">Búferes constantes predeterminados</span><span class="sxs-lookup"><span data-stu-id="d41a1-162">Default constant buffers</span></span>

<span data-ttu-id="d41a1-163">Hay dos búferes de constantes predeterminados disponibles, $Global y $Param.</span><span class="sxs-lookup"><span data-stu-id="d41a1-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="d41a1-164">Las variables que se colocan en el ámbito global se agregan implícitamente al $Global, con el mismo método de empaquetado que se usa para los búferes de carga.</span><span class="sxs-lookup"><span data-stu-id="d41a1-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="d41a1-165">Los parámetros uniformes de la lista de parámetros de una función aparecen en $Param búfer constante cuando se compila un sombreador fuera del marco de efectos.</span><span class="sxs-lookup"><span data-stu-id="d41a1-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="d41a1-166">Cuando se compilan dentro del marco de efectos, todos los uniformes deben resolverse en variables definidas en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="d41a1-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="d41a1-167">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d41a1-167">Examples</span></span>

<span data-ttu-id="d41a1-168">Este es un ejemplo de [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que es un búfer de textura que se forma con una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="d41a1-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="d41a1-169">Esta declaración de ejemplo asigna manualmente un búfer constante para iniciarse en un registro determinado y también empaqueta elementos determinados por subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="d41a1-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="d41a1-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d41a1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d41a1-171">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="d41a1-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

