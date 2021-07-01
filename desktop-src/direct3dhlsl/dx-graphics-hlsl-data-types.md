---
title: Tipos de datos (HLSL)
description: HLSL admite muchos tipos de datos intrínsecos diferentes. En esta tabla se muestran los tipos que se usarán para definir variables de sombreador.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129652"
---
# <a name="data-types-hlsl"></a><span data-ttu-id="f3cb7-104">Tipos de datos (HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3cb7-104">Data Types (HLSL)</span></span>

<span data-ttu-id="f3cb7-105">HLSL admite muchos tipos de datos intrínsecos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f3cb7-105">HLSL supports many different intrinsic data types.</span></span> <span data-ttu-id="f3cb7-106">En esta tabla se muestran los tipos que se usarán para definir variables de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f3cb7-106">This table shows which types to use to define shader variables.</span></span>



| <span data-ttu-id="f3cb7-107">Usar este tipo intrínseco</span><span class="sxs-lookup"><span data-stu-id="f3cb7-107">Use this intrinsic type</span></span>                                                                                                                         | <span data-ttu-id="f3cb7-108">Para definir esta variable de sombreador</span><span class="sxs-lookup"><span data-stu-id="f3cb7-108">To define this shader variable</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="f3cb7-109">Escalar</span><span class="sxs-lookup"><span data-stu-id="f3cb7-109">Scalar</span></span>](dx-graphics-hlsl-scalar.md)                                                                                   | <span data-ttu-id="f3cb7-110">Escalar de un componente</span><span class="sxs-lookup"><span data-stu-id="f3cb7-110">One-component scalar</span></span>                       |
| <span data-ttu-id="f3cb7-111">[Vector](dx-graphics-hlsl-vector.md), [Matriz](dx-graphics-hlsl-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="f3cb7-111">[Vector](dx-graphics-hlsl-vector.md), [Matrix](dx-graphics-hlsl-matrix.md)</span></span>                                            | <span data-ttu-id="f3cb7-112">Vector o matriz de varios componentes</span><span class="sxs-lookup"><span data-stu-id="f3cb7-112">Multiple-component vector or matrix</span></span>        |
| <span data-ttu-id="f3cb7-113">[Sampler,](dx-graphics-hlsl-sampler.md) [Texture o](dx-graphics-hlsl-texture.md) [Buffer](dx-graphics-hlsl-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="f3cb7-113">[Sampler](dx-graphics-hlsl-sampler.md), [Texture](dx-graphics-hlsl-texture.md) or [Buffer](dx-graphics-hlsl-buffer.md)</span></span>   | <span data-ttu-id="f3cb7-114">Muestreador, textura u objeto de búfer</span><span class="sxs-lookup"><span data-stu-id="f3cb7-114">Sampler, texture, or buffer object</span></span>         |
| <span data-ttu-id="f3cb7-115">[Struct](dx-graphics-hlsl-struct.md), [definido por el usuario](dx-graphics-hlsl-user-defined.md)</span><span class="sxs-lookup"><span data-stu-id="f3cb7-115">[Struct](dx-graphics-hlsl-struct.md), [User Defined](dx-graphics-hlsl-user-defined.md)</span></span>                                | <span data-ttu-id="f3cb7-116">Estructura personalizada o definición de tipo</span><span class="sxs-lookup"><span data-stu-id="f3cb7-116">Custom structure or typedef</span></span>                |
| <span data-ttu-id="f3cb7-117">Array</span><span class="sxs-lookup"><span data-stu-id="f3cb7-117">Array</span></span>                                                                                   | <span data-ttu-id="f3cb7-118">Expresiones escalares literales declaradas que contienen la mayoría de los demás tipos</span><span class="sxs-lookup"><span data-stu-id="f3cb7-118">Literal scalar expressions declared containing most other types</span></span>                       |
| [<span data-ttu-id="f3cb7-119">Objeto State</span><span class="sxs-lookup"><span data-stu-id="f3cb7-119">State Object</span></span>](dx-graphics-hlsl-state-object.md) | <span data-ttu-id="f3cb7-120">Representaciones HLSL de objetos de estado</span><span class="sxs-lookup"><span data-stu-id="f3cb7-120">HLSL representations of state objects</span></span> |


 

<span data-ttu-id="f3cb7-121">Para ayudarle a comprender mejor cómo usar vectores y matrices en HLSL, puede leer esta información general sobre cómo HLSL usa las matemáticas por [componente.](dx-graphics-hlsl-per-component-math.md)</span><span class="sxs-lookup"><span data-stu-id="f3cb7-121">To help you better understand how to use vectors and matrices in HLSL, you may want to read this background information on how HLSL uses [per-component](dx-graphics-hlsl-per-component-math.md) math.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3cb7-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3cb7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3cb7-123">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3cb7-123">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




