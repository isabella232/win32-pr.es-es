---
title: Preciso
description: Deshabilitación por instrucción de la refactorización aritmética.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532860"
---
# <a name="precise"></a><span data-ttu-id="17ad7-103">Preciso</span><span class="sxs-lookup"><span data-stu-id="17ad7-103">Precise</span></span>

<span data-ttu-id="17ad7-104">Deshabilitación por instrucción de la refactorización aritmética.</span><span class="sxs-lookup"><span data-stu-id="17ad7-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="17ad7-105">preciso (máscara de componentes)</span><span class="sxs-lookup"><span data-stu-id="17ad7-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="17ad7-106">Este modificador requiere la marca del sombreador global "Refactoring \_ allowed".</span><span class="sxs-lookup"><span data-stu-id="17ad7-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="17ad7-107">Cuando está presente la refactorización \_ permitida, los resultados de componentes individuales de las instrucciones individuales pueden verse obligados a ser precisos o no refactorizables por los compiladores o los controladores.</span><span class="sxs-lookup"><span data-stu-id="17ad7-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="17ad7-108">Si los componentes de una instrucción de [**Mad**](mad--sm4---asm-.md) se etiquetan como **precisos**, el hardware debe ejecutar una instrucción de **Mad** o el equivalente exacto, y no puede dividirlo en una multiplicación seguida de una suma.</span><span class="sxs-lookup"><span data-stu-id="17ad7-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="17ad7-109">Por el contrario, un multiplicado seguido por una suma, donde uno o ambos se marcan como **precisos**, no se pueden combinar en un **Mad** fundido.</span><span class="sxs-lookup"><span data-stu-id="17ad7-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="17ad7-110">Si \_ no se ha especificado la REfactorización permitido, no se permite el modificador **preciso** .</span><span class="sxs-lookup"><span data-stu-id="17ad7-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="17ad7-111">No es necesario porque todo es preciso.</span><span class="sxs-lookup"><span data-stu-id="17ad7-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="17ad7-112">El modificador **preciso** afecta a cualquier operación, no solo a aritmética.</span><span class="sxs-lookup"><span data-stu-id="17ad7-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="17ad7-113">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="17ad7-113">Minimum Shader Model</span></span>

<span data-ttu-id="17ad7-114">Este modificador es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="17ad7-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="17ad7-115">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="17ad7-115">Shader Model</span></span>                                              | <span data-ttu-id="17ad7-116">Compatible</span><span class="sxs-lookup"><span data-stu-id="17ad7-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="17ad7-117">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="17ad7-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="17ad7-118">sí</span><span class="sxs-lookup"><span data-stu-id="17ad7-118">yes</span></span>       |
| [<span data-ttu-id="17ad7-119">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="17ad7-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="17ad7-120">no</span><span class="sxs-lookup"><span data-stu-id="17ad7-120">no</span></span>        |
| [<span data-ttu-id="17ad7-121">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="17ad7-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="17ad7-122">sí</span><span class="sxs-lookup"><span data-stu-id="17ad7-122">yes</span></span>       |
| [<span data-ttu-id="17ad7-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17ad7-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="17ad7-124">no</span><span class="sxs-lookup"><span data-stu-id="17ad7-124">no</span></span>        |
| [<span data-ttu-id="17ad7-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17ad7-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="17ad7-126">no</span><span class="sxs-lookup"><span data-stu-id="17ad7-126">no</span></span>        |
| [<span data-ttu-id="17ad7-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17ad7-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="17ad7-128">no</span><span class="sxs-lookup"><span data-stu-id="17ad7-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="17ad7-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17ad7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ad7-130">Modificadores de instrucciones del modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="17ad7-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




