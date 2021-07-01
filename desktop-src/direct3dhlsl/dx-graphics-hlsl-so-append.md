---
title: Append (objeto Stream-Output HLSL de DirectX)
description: Anexe los datos de geometry-shader-output a una secuencia existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120190"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="aa2db-103">Append (objeto Stream-Output HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="aa2db-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="aa2db-104">Anexe los datos de geometry-shader-output a una secuencia existente.</span><span class="sxs-lookup"><span data-stu-id="aa2db-104">Append geometry-shader-output data to an existing stream.</span></span>

<span data-ttu-id="aa2db-105">Append( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="aa2db-105">Append( *StreamDataType*);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="aa2db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa2db-106">Parameters</span></span>



| <span data-ttu-id="aa2db-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa2db-107">Item</span></span>                                                                                                                             | <span data-ttu-id="aa2db-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa2db-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2db-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="aa2db-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="aa2db-110">Descripción de la entrada de datos.</span><span class="sxs-lookup"><span data-stu-id="aa2db-110">A data input description.</span></span> <span data-ttu-id="aa2db-111">Esta descripción debe coincidir con el parámetro de plantilla stream-object denominado [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="aa2db-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="aa2db-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa2db-112">Return Value</span></span>

<span data-ttu-id="aa2db-113">None</span><span class="sxs-lookup"><span data-stu-id="aa2db-113">None</span></span>

## <a name="example"></a><span data-ttu-id="aa2db-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa2db-114">Example</span></span>

<span data-ttu-id="aa2db-115">Este fragmento de código (del ejemplo [CubeMapGS)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)muestra un ejemplo parcial de anexar primitivas de franja de triángulo a un objeto de salida de flujo.</span><span class="sxs-lookup"><span data-stu-id="aa2db-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="aa2db-116">Modelo mínimo de sombreador</span><span class="sxs-lookup"><span data-stu-id="aa2db-116">Minimum Shader Model</span></span>

<span data-ttu-id="aa2db-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="aa2db-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa2db-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="aa2db-118">Shader Model</span></span>                                              | <span data-ttu-id="aa2db-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="aa2db-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa2db-120">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="aa2db-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa2db-121">Sí</span><span class="sxs-lookup"><span data-stu-id="aa2db-121">yes</span></span>       |
| [<span data-ttu-id="aa2db-122">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2db-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa2db-123">No</span><span class="sxs-lookup"><span data-stu-id="aa2db-123">no</span></span>        |
| [<span data-ttu-id="aa2db-124">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2db-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa2db-125">No</span><span class="sxs-lookup"><span data-stu-id="aa2db-125">no</span></span>        |
| [<span data-ttu-id="aa2db-126">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa2db-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa2db-127">No</span><span class="sxs-lookup"><span data-stu-id="aa2db-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa2db-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa2db-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa2db-129">Objeto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="aa2db-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





