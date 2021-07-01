---
title: dcl_usage entrada (sm1, sm2, sm3 - vs asm)
description: Declare la asociación entre el uso de un elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129692"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="47aa6-103">dcl \_ usage input (sm1, sm2, sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="47aa6-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="47aa6-104">Declare la asociación entre el uso de un elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="47aa6-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="47aa6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47aa6-105">Syntax</span></span>

<span data-ttu-id="47aa6-106">dcl \_ usage \[ index \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="47aa6-106">dcl\_usage\[usage\_index\] v\#</span></span>



 

<span data-ttu-id="47aa6-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="47aa6-107">Where:</span></span>

-   <span data-ttu-id="47aa6-108">El uso \_ de dcl identifica cómo se usarán los datos de registro.</span><span class="sxs-lookup"><span data-stu-id="47aa6-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="47aa6-109">Este es el mismo valor que los miembros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sin el prefijo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="47aa6-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="47aa6-110">usage \_ index es un índice entero opcional entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="47aa6-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="47aa6-111">Modifica los datos de uso.</span><span class="sxs-lookup"><span data-stu-id="47aa6-111">It modifies the usage data.</span></span> <span data-ttu-id="47aa6-112">El índice coincide con el índice de uso de una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="47aa6-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="47aa6-113">Vea [Declaración de vértice (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration)</span><span class="sxs-lookup"><span data-stu-id="47aa6-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="47aa6-114">El índice se anexa al valor de uso (dcl \_ usage ) sin espacio.</span><span class="sxs-lookup"><span data-stu-id="47aa6-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="47aa6-115">Si no se proporciona, se supone que es 0.</span><span class="sxs-lookup"><span data-stu-id="47aa6-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="47aa6-116">v \# es un registro de [entrada.](dx9-graphics-reference-asm-vs-registers-input.md)</span><span class="sxs-lookup"><span data-stu-id="47aa6-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47aa6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47aa6-117">Remarks</span></span>



| <span data-ttu-id="47aa6-118">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="47aa6-118">Vertex shader versions</span></span> | <span data-ttu-id="47aa6-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="47aa6-119">1\_1</span></span> | <span data-ttu-id="47aa6-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="47aa6-120">2\_0</span></span> | <span data-ttu-id="47aa6-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="47aa6-121">2\_x</span></span> | <span data-ttu-id="47aa6-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="47aa6-122">2\_sw</span></span> | <span data-ttu-id="47aa6-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="47aa6-123">3\_0</span></span> | <span data-ttu-id="47aa6-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="47aa6-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="47aa6-125">Uso \_ de dcl</span><span class="sxs-lookup"><span data-stu-id="47aa6-125">dcl\_usage</span></span>             | <span data-ttu-id="47aa6-126">x</span><span class="sxs-lookup"><span data-stu-id="47aa6-126">x</span></span>    | <span data-ttu-id="47aa6-127">x</span><span class="sxs-lookup"><span data-stu-id="47aa6-127">x</span></span>    | <span data-ttu-id="47aa6-128">x</span><span class="sxs-lookup"><span data-stu-id="47aa6-128">x</span></span>    | <span data-ttu-id="47aa6-129">x</span><span class="sxs-lookup"><span data-stu-id="47aa6-129">x</span></span>     | <span data-ttu-id="47aa6-130">x</span><span class="sxs-lookup"><span data-stu-id="47aa6-130">x</span></span>    | <span data-ttu-id="47aa6-131">x</span><span class="sxs-lookup"><span data-stu-id="47aa6-131">x</span></span>     |



 

<span data-ttu-id="47aa6-132">Todas las instrucciones de uso de dcl \_ deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="47aa6-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47aa6-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47aa6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47aa6-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="47aa6-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
