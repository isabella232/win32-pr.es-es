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
ms.openlocfilehash: 44bd976d05c0734ca2e498b5de405564f689e20d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998392"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="62eb8-103">dcl \_ usage input (sm1, sm2, sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="62eb8-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="62eb8-104">Declare la asociación entre el uso de un elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="62eb8-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="62eb8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62eb8-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="62eb8-106">dcl \_ usage \[ index \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="62eb8-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="62eb8-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="62eb8-107">Where:</span></span>

-   <span data-ttu-id="62eb8-108">dcl \_ usage identifica cómo se usarán los datos de registro.</span><span class="sxs-lookup"><span data-stu-id="62eb8-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="62eb8-109">Este es el mismo valor que los miembros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sin el prefijo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="62eb8-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="62eb8-110">usage \_ index es un índice entero opcional entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="62eb8-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="62eb8-111">Modifica los datos de uso.</span><span class="sxs-lookup"><span data-stu-id="62eb8-111">It modifies the usage data.</span></span> <span data-ttu-id="62eb8-112">El índice coincide con el índice de uso en una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="62eb8-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="62eb8-113">Vea [Declaración de vértices (Direct3D 9).](/windows/desktop/direct3d9/vertex-declaration)</span><span class="sxs-lookup"><span data-stu-id="62eb8-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="62eb8-114">El índice se anexa al valor de uso (dcl \_ usage ) sin espacio.</span><span class="sxs-lookup"><span data-stu-id="62eb8-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="62eb8-115">Si no se proporciona, se supone que es 0.</span><span class="sxs-lookup"><span data-stu-id="62eb8-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="62eb8-116">v \# es un registro de [entrada.](dx9-graphics-reference-asm-vs-registers-input.md)</span><span class="sxs-lookup"><span data-stu-id="62eb8-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62eb8-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62eb8-117">Remarks</span></span>



| <span data-ttu-id="62eb8-118">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="62eb8-118">Vertex shader versions</span></span> | <span data-ttu-id="62eb8-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="62eb8-119">1\_1</span></span> | <span data-ttu-id="62eb8-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="62eb8-120">2\_0</span></span> | <span data-ttu-id="62eb8-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="62eb8-121">2\_x</span></span> | <span data-ttu-id="62eb8-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="62eb8-122">2\_sw</span></span> | <span data-ttu-id="62eb8-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="62eb8-123">3\_0</span></span> | <span data-ttu-id="62eb8-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="62eb8-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="62eb8-125">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="62eb8-125">dcl\_usage</span></span>             | <span data-ttu-id="62eb8-126">x</span><span class="sxs-lookup"><span data-stu-id="62eb8-126">x</span></span>    | <span data-ttu-id="62eb8-127">x</span><span class="sxs-lookup"><span data-stu-id="62eb8-127">x</span></span>    | <span data-ttu-id="62eb8-128">x</span><span class="sxs-lookup"><span data-stu-id="62eb8-128">x</span></span>    | <span data-ttu-id="62eb8-129">x</span><span class="sxs-lookup"><span data-stu-id="62eb8-129">x</span></span>     | <span data-ttu-id="62eb8-130">x</span><span class="sxs-lookup"><span data-stu-id="62eb8-130">x</span></span>    | <span data-ttu-id="62eb8-131">x</span><span class="sxs-lookup"><span data-stu-id="62eb8-131">x</span></span>     |



 

<span data-ttu-id="62eb8-132">Todas las instrucciones de uso de dcl \_ deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="62eb8-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62eb8-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62eb8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62eb8-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="62eb8-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
