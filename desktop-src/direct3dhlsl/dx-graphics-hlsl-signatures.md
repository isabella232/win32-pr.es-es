---
title: Prototipos
description: Una firma de sombreador es una lista de los parámetros que son la entrada o la salida de una función de sombreador.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996796"
---
# <a name="signatures"></a><span data-ttu-id="b6621-103">Prototipos</span><span class="sxs-lookup"><span data-stu-id="b6621-103">Signatures</span></span>

<span data-ttu-id="b6621-104">Una firma de sombreador es una lista de los parámetros que son la entrada o la salida de una función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b6621-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="b6621-105">En Direct3D 10, las fases adyacentes comparten eficazmente una matriz de registros, donde el sombreador de salida (o la fase de canalización) escribe datos en ubicaciones específicas de la matriz de registro y el sombreador de entrada debe leer desde las mismas ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="b6621-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="b6621-106">La API usa firmas de sombreador para enlazar salidas de sombreador con entradas sin la sobrecarga de la resolución semántica.</span><span class="sxs-lookup"><span data-stu-id="b6621-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="b6621-107">En Direct3D 10, las firmas de entrada se generan a partir de una declaración de entrada de sombreador y la firma de salida se genera a partir de una declaración de salida de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b6621-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="b6621-108">Se dice que una firma de entrada es compatible con una firma de salida cuando la firma de salida es un subconjunto estricto (tipo de argumento y coincidencia de orden) de la firma de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6621-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="b6621-109">La manera más sencilla de lograrlo es vincular las entradas y salidas de sombreador correspondientes con el mismo tipo de estructura.</span><span class="sxs-lookup"><span data-stu-id="b6621-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="b6621-110">Este es un ejemplo de firmas compatibles.</span><span class="sxs-lookup"><span data-stu-id="b6621-110">Here is an example of compatible signatures.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



<span data-ttu-id="b6621-111">A continuación se muestra un ejemplo de firmas incompatibles; el orden de los parámetros en la signatura de entrada no coincide con el orden de la firma de salida.</span><span class="sxs-lookup"><span data-stu-id="b6621-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



<span data-ttu-id="b6621-112">PSInWorks es un subconjunto compatible de VSOut (las dos primeras entradas coinciden con el tipo y el orden con las dos primeras entradas en VSOut).</span><span class="sxs-lookup"><span data-stu-id="b6621-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="b6621-113">Sin embargo, PSInFails es incompatible porque el orden no coincide con VSOut.</span><span class="sxs-lookup"><span data-stu-id="b6621-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6621-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6621-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6621-115">Funciones</span><span class="sxs-lookup"><span data-stu-id="b6621-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




