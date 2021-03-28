---
title: hs_decls (SM5-ASM)
description: Inicie la fase de declaraciones en un sombreador de casco.
ms.assetid: 1C8552B1-F649-4B73-A365-D449A9121DAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e57207e35aab507a1404efaf90131a9648918ae7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149003"
---
# <a name="hs_decls-sm5---asm"></a><span data-ttu-id="26ace-103">HS \_ Decls (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="26ace-103">hs\_decls (sm5 - asm)</span></span>

<span data-ttu-id="26ace-104">Inicie la fase de declaraciones en un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="26ace-104">Start the declarations phase in a hull shader.</span></span>



| <span data-ttu-id="26ace-105">HS \_ Decls</span><span class="sxs-lookup"><span data-stu-id="26ace-105">hs\_decls</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="26ace-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26ace-106">Remarks</span></span>

<span data-ttu-id="26ace-107">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="26ace-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="26ace-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="26ace-108">Vertex</span></span> | <span data-ttu-id="26ace-109">Casco</span><span class="sxs-lookup"><span data-stu-id="26ace-109">Hull</span></span> | <span data-ttu-id="26ace-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="26ace-110">Domain</span></span> | <span data-ttu-id="26ace-111">Geometría</span><span class="sxs-lookup"><span data-stu-id="26ace-111">Geometry</span></span> | <span data-ttu-id="26ace-112">Píxel</span><span class="sxs-lookup"><span data-stu-id="26ace-112">Pixel</span></span> | <span data-ttu-id="26ace-113">Compute</span><span class="sxs-lookup"><span data-stu-id="26ace-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="26ace-114">X</span><span class="sxs-lookup"><span data-stu-id="26ace-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="26ace-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="26ace-115">Minimum Shader Model</span></span>

<span data-ttu-id="26ace-116">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="26ace-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="26ace-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="26ace-117">Shader Model</span></span>                                              | <span data-ttu-id="26ace-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="26ace-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="26ace-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="26ace-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="26ace-120">sí</span><span class="sxs-lookup"><span data-stu-id="26ace-120">yes</span></span>       |
| [<span data-ttu-id="26ace-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="26ace-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="26ace-122">no</span><span class="sxs-lookup"><span data-stu-id="26ace-122">no</span></span>        |
| [<span data-ttu-id="26ace-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="26ace-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="26ace-124">no</span><span class="sxs-lookup"><span data-stu-id="26ace-124">no</span></span>        |
| [<span data-ttu-id="26ace-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ace-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="26ace-126">no</span><span class="sxs-lookup"><span data-stu-id="26ace-126">no</span></span>        |
| [<span data-ttu-id="26ace-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ace-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="26ace-128">no</span><span class="sxs-lookup"><span data-stu-id="26ace-128">no</span></span>        |
| [<span data-ttu-id="26ace-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ace-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="26ace-130">no</span><span class="sxs-lookup"><span data-stu-id="26ace-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="26ace-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26ace-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ace-132">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="26ace-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




