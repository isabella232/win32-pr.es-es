---
title: DEF-vs
description: Define las constantes del sombreador de vértices.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271360"
---
# <a name="def---vs"></a><span data-ttu-id="b607d-103">DEF-vs</span><span class="sxs-lookup"><span data-stu-id="b607d-103">def - vs</span></span>

<span data-ttu-id="b607d-104">Define las constantes del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="b607d-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="b607d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b607d-105">Syntax</span></span>



| <span data-ttu-id="b607d-106">DEF DST, float1, float2, float3, FLOAT4</span><span class="sxs-lookup"><span data-stu-id="b607d-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="b607d-107">, donde</span><span class="sxs-lookup"><span data-stu-id="b607d-107">where</span></span>

-   <span data-ttu-id="b607d-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b607d-108">dst is the destination register.</span></span>
-   <span data-ttu-id="b607d-109">float1, float2, float3, FLOAT4 son cuatro números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="b607d-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="b607d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b607d-110">Remarks</span></span>



| <span data-ttu-id="b607d-111">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b607d-111">Vertex shader versions</span></span> | <span data-ttu-id="b607d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="b607d-112">1\_1</span></span> | <span data-ttu-id="b607d-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b607d-113">2\_0</span></span> | <span data-ttu-id="b607d-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b607d-114">2\_x</span></span> | <span data-ttu-id="b607d-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b607d-115">2\_sw</span></span> | <span data-ttu-id="b607d-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b607d-116">3\_0</span></span> | <span data-ttu-id="b607d-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b607d-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b607d-118">def</span><span class="sxs-lookup"><span data-stu-id="b607d-118">def</span></span>                    | <span data-ttu-id="b607d-119">x</span><span class="sxs-lookup"><span data-stu-id="b607d-119">x</span></span>    | <span data-ttu-id="b607d-120">x</span><span class="sxs-lookup"><span data-stu-id="b607d-120">x</span></span>    | <span data-ttu-id="b607d-121">x</span><span class="sxs-lookup"><span data-stu-id="b607d-121">x</span></span>    | <span data-ttu-id="b607d-122">x</span><span class="sxs-lookup"><span data-stu-id="b607d-122">x</span></span>     | <span data-ttu-id="b607d-123">x</span><span class="sxs-lookup"><span data-stu-id="b607d-123">x</span></span>    | <span data-ttu-id="b607d-124">x</span><span class="sxs-lookup"><span data-stu-id="b607d-124">x</span></span>     |



 

<span data-ttu-id="b607d-125">La instrucción Def define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b607d-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="b607d-126">Se denominan constantes inmediatas.</span><span class="sxs-lookup"><span data-stu-id="b607d-126">These are called immediate constants.</span></span> <span data-ttu-id="b607d-127">Las constantes inmediatas tienen prioridad sobre las constantes establecidas por los métodos de API SetVertexShaderConstantF.</span><span class="sxs-lookup"><span data-stu-id="b607d-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="b607d-128">Hay dos maneras de establecer una constante en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="b607d-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="b607d-129">Use Def-vs para definir la constante directamente dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="b607d-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="b607d-130">DEF-vs solo puede definir constantes de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="b607d-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="b607d-131">Use los métodos de la API para establecer una constante.</span><span class="sxs-lookup"><span data-stu-id="b607d-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="b607d-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) para establecer una constante de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="b607d-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b607d-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b607d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b607d-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b607d-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="b607d-135">defi-vs</span><span class="sxs-lookup"><span data-stu-id="b607d-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="b607d-136">defb-vs</span><span class="sxs-lookup"><span data-stu-id="b607d-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 