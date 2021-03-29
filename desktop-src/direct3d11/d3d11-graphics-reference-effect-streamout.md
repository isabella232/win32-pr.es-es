---
title: Sintaxis de Stream out
description: Un sombreador de geometría con Stream out se declara con una sintaxis determinada.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996764"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="a939d-103">Sintaxis de Stream out</span><span class="sxs-lookup"><span data-stu-id="a939d-103">Stream Out Syntax</span></span>

<span data-ttu-id="a939d-104">Un sombreador de geometría con Stream out se declara con una sintaxis determinada.</span><span class="sxs-lookup"><span data-stu-id="a939d-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="a939d-105">En este tema se describe la sintaxis de.</span><span class="sxs-lookup"><span data-stu-id="a939d-105">This topic describes the syntax.</span></span> <span data-ttu-id="a939d-106">En el tiempo de ejecución del efecto, esta sintaxis se convertirá en una llamada a [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span><span class="sxs-lookup"><span data-stu-id="a939d-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="a939d-107">Sintaxis de construcción</span><span class="sxs-lookup"><span data-stu-id="a939d-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="a939d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="a939d-108">Name</span></span>                   | <span data-ttu-id="a939d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a939d-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a939d-110">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="a939d-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="a939d-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a939d-111">Optional.</span></span> <span data-ttu-id="a939d-112">Cadena de ASCI que identifica de forma única el nombre de una variable de sombreador de geometría con transmisión por secuencias. Esto es opcional porque ConstructGSWithSO puede colocarse directamente en una llamada a SetGeometryShader o BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="a939d-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="a939d-113">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="a939d-113">**ShaderVar**</span></span>          | <span data-ttu-id="a939d-114">Sombreador de geometría o variable de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="a939d-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="a939d-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="a939d-115">**OutputDecl0**</span></span>        | <span data-ttu-id="a939d-116">Una cadena que define qué salidas del sombreador en el flujo 0 se transmiten por secuencias. Vea a continuación la sintaxis de.</span><span class="sxs-lookup"><span data-stu-id="a939d-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="a939d-117">Esta es la sintaxis que se definió \_ en \_ los archivos FX 4 0.</span><span class="sxs-lookup"><span data-stu-id="a939d-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="a939d-118">Tenga en cuenta que en los \_ \_ sombreadores GS 4 0 y vs \_ x, solo hay un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="a939d-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="a939d-119">El sombreador resultante generará un flujo para la unidad de salida de flujo y la unidad de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="a939d-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="a939d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a939d-120">Name</span></span>                   | <span data-ttu-id="a939d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a939d-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a939d-122">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="a939d-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="a939d-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a939d-123">Optional.</span></span> <span data-ttu-id="a939d-124">Cadena de ASCI que identifica de forma única el nombre de una variable de sombreador de geometría con transmisión por secuencias. Esto es opcional porque ConstructGSWithSO puede colocarse directamente en una llamada a SetGeometryShader o BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="a939d-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="a939d-125">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="a939d-125">**ShaderVar**</span></span>          | <span data-ttu-id="a939d-126">Sombreador de geometría o variable de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="a939d-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="a939d-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="a939d-127">**OutputDecl0**</span></span>        | <span data-ttu-id="a939d-128">Una cadena que define qué salidas del sombreador en el flujo 0 se transmiten por secuencias. Vea a continuación la sintaxis de.</span><span class="sxs-lookup"><span data-stu-id="a939d-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="a939d-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="a939d-129">**OutputDecl1**</span></span>        | <span data-ttu-id="a939d-130">Una cadena que define qué salidas del sombreador en Stream 1 se transmiten por secuencias. Vea a continuación la sintaxis de.</span><span class="sxs-lookup"><span data-stu-id="a939d-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="a939d-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="a939d-131">**OutputDecl2**</span></span>        | <span data-ttu-id="a939d-132">Una cadena que define qué salidas del sombreador en Stream 2 se transmiten por secuencias. Vea a continuación la sintaxis de.</span><span class="sxs-lookup"><span data-stu-id="a939d-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="a939d-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="a939d-133">**OutputDecl3**</span></span>        | <span data-ttu-id="a939d-134">Una cadena que define qué salidas del sombreador en Stream 3 se transmiten por secuencias. Vea a continuación la sintaxis de.</span><span class="sxs-lookup"><span data-stu-id="a939d-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="a939d-135">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="a939d-135">**RasterizedStream**</span></span>   | <span data-ttu-id="a939d-136">Entero que especifica la secuencia que se enviará al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="a939d-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="a939d-137">Tenga en cuenta que los \_ \_ sombreadores GS 5 0 pueden definir hasta cuatro flujos de datos.</span><span class="sxs-lookup"><span data-stu-id="a939d-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="a939d-138">El sombreador resultante generará una secuencia de salida para cada declaración de salida que no sea **null** y una secuencia la unidad de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="a939d-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="a939d-139">Sintaxis de la declaración out de Stream</span><span class="sxs-lookup"><span data-stu-id="a939d-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="a939d-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="a939d-140">Name</span></span>              | <span data-ttu-id="a939d-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="a939d-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a939d-142">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="a939d-142">**Buffer**</span></span>        | <span data-ttu-id="a939d-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a939d-143">Optional.</span></span> <span data-ttu-id="a939d-144">Entero, 0 <= búfer < 4, que especifica a qué búfer de salida de flujo se va a pasar el valor.</span><span class="sxs-lookup"><span data-stu-id="a939d-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="a939d-145">**Semántica**</span><span class="sxs-lookup"><span data-stu-id="a939d-145">**Semantic**</span></span>      | <span data-ttu-id="a939d-146">Una cadena, junto con SemanticIndex, que especifica el valor que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="a939d-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="a939d-147">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="a939d-147">**SemanticIndex**</span></span> | <span data-ttu-id="a939d-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a939d-148">Optional.</span></span> <span data-ttu-id="a939d-149">Índice asociado a Semantic.</span><span class="sxs-lookup"><span data-stu-id="a939d-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="a939d-150">**Máscara**</span><span class="sxs-lookup"><span data-stu-id="a939d-150">**Mask**</span></span>          | <span data-ttu-id="a939d-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a939d-151">Optional.</span></span> <span data-ttu-id="a939d-152">Máscara de componente, que indica los componentes del valor que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="a939d-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="a939d-153">Hay una semántica especial, etiquetada como "$SKIP" que indica una semántica vacía, sin tocar la memoria correspondiente en el búfer de flujo de salida.</span><span class="sxs-lookup"><span data-stu-id="a939d-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="a939d-154">La semántica $SKIP no puede tener un SemanticIndex, pero puede tener una máscara.</span><span class="sxs-lookup"><span data-stu-id="a939d-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="a939d-155">La declaración out completa de la secuencia puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a939d-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="a939d-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a939d-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a939d-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a939d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a939d-158">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a939d-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




