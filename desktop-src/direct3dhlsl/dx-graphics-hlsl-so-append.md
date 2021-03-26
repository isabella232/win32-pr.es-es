---
title: Append (objeto de Stream-Output de datos HLSL de DirectX)
description: Anexe los datos de salida del sombreador de geometría a un flujo existente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "104358556"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="a8cf2-103">Append (objeto de Stream-Output de datos HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="a8cf2-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="a8cf2-104">Anexe los datos de salida del sombreador de geometría a un flujo existente.</span><span class="sxs-lookup"><span data-stu-id="a8cf2-104">Append geometry-shader-output data to an existing stream.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="a8cf2-105">Append ( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="a8cf2-105">Append( *StreamDataType*);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a8cf2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8cf2-106">Parameters</span></span>



| <span data-ttu-id="a8cf2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8cf2-107">Item</span></span>                                                                                                                             | <span data-ttu-id="a8cf2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8cf2-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8cf2-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="a8cf2-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="a8cf2-110">Una descripción de entrada de datos.</span><span class="sxs-lookup"><span data-stu-id="a8cf2-110">A data input description.</span></span> <span data-ttu-id="a8cf2-111">Esta descripción debe coincidir con el parámetro de plantilla de objeto de secuencia denominado [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="a8cf2-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a8cf2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8cf2-112">Return Value</span></span>

<span data-ttu-id="a8cf2-113">None</span><span class="sxs-lookup"><span data-stu-id="a8cf2-113">None</span></span>

## <a name="example"></a><span data-ttu-id="a8cf2-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8cf2-114">Example</span></span>

<span data-ttu-id="a8cf2-115">Este fragmento de código (del [ejemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) muestra un ejemplo parcial de cómo anexar los primitivos de franja de triángulo a un objeto de salida de flujo.</span><span class="sxs-lookup"><span data-stu-id="a8cf2-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="a8cf2-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a8cf2-116">Minimum Shader Model</span></span>

<span data-ttu-id="a8cf2-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8cf2-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a8cf2-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8cf2-118">Shader Model</span></span>                                              | <span data-ttu-id="a8cf2-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="a8cf2-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8cf2-120">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a8cf2-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8cf2-121">sí</span><span class="sxs-lookup"><span data-stu-id="a8cf2-121">yes</span></span>       |
| [<span data-ttu-id="a8cf2-122">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8cf2-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8cf2-123">no</span><span class="sxs-lookup"><span data-stu-id="a8cf2-123">no</span></span>        |
| [<span data-ttu-id="a8cf2-124">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8cf2-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8cf2-125">no</span><span class="sxs-lookup"><span data-stu-id="a8cf2-125">no</span></span>        |
| [<span data-ttu-id="a8cf2-126">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8cf2-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8cf2-127">no</span><span class="sxs-lookup"><span data-stu-id="a8cf2-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8cf2-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8cf2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8cf2-129">Stream: salida de objeto</span><span class="sxs-lookup"><span data-stu-id="a8cf2-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





