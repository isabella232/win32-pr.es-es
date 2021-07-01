---
title: Geometry-Shader objeto
description: Un objeto de sombreador de geometría procesa primitivas enteras. Use la sintaxis siguiente para declarar un objeto de sombreador de geometría.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120620"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="722a6-105">Geometry-Shader objeto</span><span class="sxs-lookup"><span data-stu-id="722a6-105">Geometry-Shader Object</span></span>

<span data-ttu-id="722a6-106">Un objeto de sombreador de geometría procesa primitivas enteras.</span><span class="sxs-lookup"><span data-stu-id="722a6-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="722a6-107">Use la sintaxis siguiente para declarar un objeto de sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="722a6-107">Use the following syntax to declare a geometry-shader object.</span></span>

<span data-ttu-id="722a6-108">\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, inout *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="722a6-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="722a6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="722a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="722a6-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="722a6-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="722a6-111">\[en \] Declaración para el número máximo de vértices que se crearán.</span><span class="sxs-lookup"><span data-stu-id="722a6-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="722a6-112">\[maxvertexcount(): palabra clave obligatoria; los corchetes y paréntesis son caracteres \] necesarios para la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="722a6-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="722a6-113">*NumVerts:* número entero que representa el número de vértices.</span><span class="sxs-lookup"><span data-stu-id="722a6-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="722a6-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="722a6-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="722a6-115">\[en \] Una cadena ASCII que contiene un nombre único para la función geometry-shader.</span><span class="sxs-lookup"><span data-stu-id="722a6-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="722a6-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="722a6-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="722a6-117">*PrimitiveType:* tipo primitivo, que determina el orden de los datos primitivos.</span><span class="sxs-lookup"><span data-stu-id="722a6-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="722a6-118">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="722a6-118">Primitive Type</span></span> | <span data-ttu-id="722a6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="722a6-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="722a6-120">*Punto*</span><span class="sxs-lookup"><span data-stu-id="722a6-120">*point*</span></span>        | <span data-ttu-id="722a6-121">Lista de puntos</span><span class="sxs-lookup"><span data-stu-id="722a6-121">Point list</span></span>                                                    |
| <span data-ttu-id="722a6-122">*Línea*</span><span class="sxs-lookup"><span data-stu-id="722a6-122">*line*</span></span>         | <span data-ttu-id="722a6-123">Lista de líneas o franja de líneas</span><span class="sxs-lookup"><span data-stu-id="722a6-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="722a6-124">*Triángulo*</span><span class="sxs-lookup"><span data-stu-id="722a6-124">*triangle*</span></span>     | <span data-ttu-id="722a6-125">Lista de triángulos o franja de triángulos</span><span class="sxs-lookup"><span data-stu-id="722a6-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="722a6-126">*ydj*</span><span class="sxs-lookup"><span data-stu-id="722a6-126">*lineadj*</span></span>      | <span data-ttu-id="722a6-127">Lista de líneas con adyacencia o franja de líneas con adyacencia</span><span class="sxs-lookup"><span data-stu-id="722a6-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="722a6-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="722a6-128">*triangleadj*</span></span>  | <span data-ttu-id="722a6-129">Lista de triángulos con adyacencia o franja de triángulo con adyacencia</span><span class="sxs-lookup"><span data-stu-id="722a6-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="722a6-130">*DataType*  -  \[ en \] Un tipo de datos de entrada; puede ser cualquier tipo de datos [HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="722a6-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="722a6-131">*Nombre:* nombre del argumento; se trata de una cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="722a6-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="722a6-132">*NumElements:* tamaño de matriz de la entrada, que depende de *PrimitiveType,* como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="722a6-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="722a6-133">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="722a6-133">Primitive Type</span></span> | <span data-ttu-id="722a6-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="722a6-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="722a6-135">*Punto*</span><span class="sxs-lookup"><span data-stu-id="722a6-135">*point*</span></span>        | <span data-ttu-id="722a6-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="722a6-136">\[1\]</span></span><br/> <span data-ttu-id="722a6-137">Solo se trabaja en un punto a la vez.</span><span class="sxs-lookup"><span data-stu-id="722a6-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="722a6-138">*Línea*</span><span class="sxs-lookup"><span data-stu-id="722a6-138">*line*</span></span>         | <span data-ttu-id="722a6-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="722a6-139">\[2\]</span></span><br/> <span data-ttu-id="722a6-140">Una línea requiere dos vértices.</span><span class="sxs-lookup"><span data-stu-id="722a6-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="722a6-141">*Triángulo*</span><span class="sxs-lookup"><span data-stu-id="722a6-141">*triangle*</span></span>     | <span data-ttu-id="722a6-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="722a6-142">\[3\]</span></span><br/> <span data-ttu-id="722a6-143">Un triángulo requiere tres vértices.</span><span class="sxs-lookup"><span data-stu-id="722a6-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="722a6-144">*ydj*</span><span class="sxs-lookup"><span data-stu-id="722a6-144">*lineadj*</span></span>      | <span data-ttu-id="722a6-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="722a6-145">\[4\]</span></span><br/> <span data-ttu-id="722a6-146">Un resalte tiene dos extremos: por lo tanto, requiere cuatro vértices.</span><span class="sxs-lookup"><span data-stu-id="722a6-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="722a6-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="722a6-147">*triangleadj*</span></span>  | <span data-ttu-id="722a6-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="722a6-148">\[6\]</span></span><br/> <span data-ttu-id="722a6-149">Un triánguloadj bordea tres triángulos más; por lo tanto, requiere seis vértices.</span><span class="sxs-lookup"><span data-stu-id="722a6-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="722a6-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="722a6-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="722a6-151">Declaración del objeto [stream-output](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="722a6-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="722a6-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="722a6-152">Return Value</span></span>

<span data-ttu-id="722a6-153">None</span><span class="sxs-lookup"><span data-stu-id="722a6-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="722a6-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="722a6-154">Remarks</span></span>

<span data-ttu-id="722a6-155">En el diagrama siguiente se muestran los distintos tipos primitivos para un objeto de sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="722a6-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![ilustración de los distintos tipos primitivos para un objeto de sombreador de geometría](images/d3d11-gsinputs1.png)

<span data-ttu-id="722a6-157">En el diagrama siguiente se muestran las invocaciones del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="722a6-157">The following diagram shows geometry shader invocations.</span></span>

![ilustración de las invocaciones del sombreador de geometría](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="722a6-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="722a6-159">Examples</span></span>

<span data-ttu-id="722a6-160">Este ejemplo es del ejercicio 1 del taller [Direct3D 10 Shader Model 4.0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="722a6-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="722a6-161">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="722a6-161">Minimum Shader Model</span></span>

<span data-ttu-id="722a6-162">Este objeto se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="722a6-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="722a6-163">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="722a6-163">Shader Model</span></span>                                                        | <span data-ttu-id="722a6-164">Compatible</span><span class="sxs-lookup"><span data-stu-id="722a6-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="722a6-165">[Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores</span><span class="sxs-lookup"><span data-stu-id="722a6-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="722a6-166">Sí</span><span class="sxs-lookup"><span data-stu-id="722a6-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="722a6-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="722a6-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="722a6-168">Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="722a6-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





