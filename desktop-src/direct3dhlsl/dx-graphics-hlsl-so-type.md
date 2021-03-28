---
title: Objeto Stream-Output
description: Un objeto de salida de flujo es un objeto con plantilla que transmite los datos fuera de la fase del sombreador de geometría. Use la siguiente sintaxis para declarar un objeto de salida de flujo.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420866"
---
# <a name="stream-output-object"></a><span data-ttu-id="6650d-104">Objeto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="6650d-104">Stream-Output Object</span></span>

<span data-ttu-id="6650d-105">Un objeto de salida de flujo es un objeto con plantilla que transmite los datos fuera de la [fase del sombreador de geometría](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6650d-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="6650d-106">Use la siguiente sintaxis para declarar un objeto de salida de flujo.</span><span class="sxs-lookup"><span data-stu-id="6650d-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="6650d-107">nombre del tipo de *StreamOutputObject* INOUT <  >  *;*</span><span class="sxs-lookup"><span data-stu-id="6650d-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6650d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6650d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6650d-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *DataType*  >    *Nombre* de</span><span class="sxs-lookup"><span data-stu-id="6650d-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="6650d-110">La declaración del objeto de salida de flujo (SO).</span><span class="sxs-lookup"><span data-stu-id="6650d-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="6650d-111">Stream-Output tipos de objeto</span><span class="sxs-lookup"><span data-stu-id="6650d-111">Stream-Output Object Types</span></span> | <span data-ttu-id="6650d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6650d-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="6650d-113">*PointStream*</span><span class="sxs-lookup"><span data-stu-id="6650d-113">*PointStream*</span></span>              | <span data-ttu-id="6650d-114">Secuencia de primitivas de punto.</span><span class="sxs-lookup"><span data-stu-id="6650d-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="6650d-115">*LineStream*</span><span class="sxs-lookup"><span data-stu-id="6650d-115">*LineStream*</span></span>               | <span data-ttu-id="6650d-116">Secuencia de primitivas de línea</span><span class="sxs-lookup"><span data-stu-id="6650d-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="6650d-117">*TriangleStream*</span><span class="sxs-lookup"><span data-stu-id="6650d-117">*TriangleStream*</span></span>           | <span data-ttu-id="6650d-118">Secuencia de primitivas triangulares</span><span class="sxs-lookup"><span data-stu-id="6650d-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="6650d-119">Tipo de datos *DataType* -Output; puede ser cualquier [tipo de datos HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="6650d-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="6650d-120">Debe ir entre corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="6650d-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="6650d-121">*Nombre* : nombre de la variable; cadena ASCII que identifica de forma única el objeto.</span><span class="sxs-lookup"><span data-stu-id="6650d-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="6650d-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6650d-122">Example</span></span>

<span data-ttu-id="6650d-123">Este es un ejemplo de una declaración de objeto de salida de flujo que transmite los primitivos triángulos cuyos datos se definen mediante la \_ mapa \_ de PS en la estructura.</span><span class="sxs-lookup"><span data-stu-id="6650d-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="6650d-124">El sombreador de geometría está limitado a la generación de 18 vértices.</span><span class="sxs-lookup"><span data-stu-id="6650d-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="6650d-125">Se trata de un fragmento de código del [ejemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="6650d-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="6650d-126">Stream-Output métodos de objeto</span><span class="sxs-lookup"><span data-stu-id="6650d-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="6650d-127">Use la siguiente sintaxis para llamar a los métodos Stream-Output-Object.</span><span class="sxs-lookup"><span data-stu-id="6650d-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="6650d-128">Se implementan los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="6650d-128">The following methods are implemented.</span></span>



| <span data-ttu-id="6650d-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="6650d-129">Methods</span></span>                                              | <span data-ttu-id="6650d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6650d-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="6650d-131">Append</span><span class="sxs-lookup"><span data-stu-id="6650d-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="6650d-132">Anexe los datos de salida a un flujo existente.</span><span class="sxs-lookup"><span data-stu-id="6650d-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="6650d-133">RestartStrip</span><span class="sxs-lookup"><span data-stu-id="6650d-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="6650d-134">Finalizar la franja primitiva actual e iniciar una nueva banda primitiva.</span><span class="sxs-lookup"><span data-stu-id="6650d-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6650d-135">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6650d-135">Minimum Shader Model</span></span>

<span data-ttu-id="6650d-136">Este objeto es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6650d-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="6650d-137">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6650d-137">Shader Model</span></span>                                                        | <span data-ttu-id="6650d-138">Compatible</span><span class="sxs-lookup"><span data-stu-id="6650d-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="6650d-139">Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="6650d-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="6650d-140">sí</span><span class="sxs-lookup"><span data-stu-id="6650d-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="6650d-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6650d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6650d-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6650d-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 