---
title: entrada de dcl_usage (SM1, SM2, SM3-vs ASM)
description: Declare la asociación entre un uso de elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487930"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="17d36-103">\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="17d36-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="17d36-104">Declare la asociación entre un uso de elemento de vértice y un índice de uso para un registro de entrada del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="17d36-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d36-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17d36-105">Syntax</span></span>



|                                |
|--------------------------------|
| <span data-ttu-id="17d36-106">Índice de uso de DCL \_ \[ \_ \] v\#</span><span class="sxs-lookup"><span data-stu-id="17d36-106">dcl\_usage\[usage\_index\] v\#</span></span> |



 

<span data-ttu-id="17d36-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="17d36-107">Where:</span></span>

-   <span data-ttu-id="17d36-108">\_el uso de DCL identifica cómo se utilizarán los datos de registro.</span><span class="sxs-lookup"><span data-stu-id="17d36-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="17d36-109">Este es el mismo valor que los miembros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sin el prefijo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="17d36-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="17d36-110">el \_ Índice de uso es un índice entero opcional entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="17d36-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="17d36-111">Modifica los datos de uso.</span><span class="sxs-lookup"><span data-stu-id="17d36-111">It modifies the usage data.</span></span> <span data-ttu-id="17d36-112">El índice coincide con el índice de uso en una declaración de vértice.</span><span class="sxs-lookup"><span data-stu-id="17d36-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="17d36-113">Vea [declaración de vértices (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="17d36-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="17d36-114">El índice se anexa al valor de uso ( \_ uso de DCL) sin espacio.</span><span class="sxs-lookup"><span data-stu-id="17d36-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="17d36-115">Si no se proporciona, se supone que es 0.</span><span class="sxs-lookup"><span data-stu-id="17d36-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="17d36-116">v \# es un [registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="17d36-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="17d36-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17d36-117">Remarks</span></span>



| <span data-ttu-id="17d36-118">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="17d36-118">Vertex shader versions</span></span> | <span data-ttu-id="17d36-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="17d36-119">1\_1</span></span> | <span data-ttu-id="17d36-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17d36-120">2\_0</span></span> | <span data-ttu-id="17d36-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17d36-121">2\_x</span></span> | <span data-ttu-id="17d36-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17d36-122">2\_sw</span></span> | <span data-ttu-id="17d36-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17d36-123">3\_0</span></span> | <span data-ttu-id="17d36-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17d36-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="17d36-125">uso de DCL \_</span><span class="sxs-lookup"><span data-stu-id="17d36-125">dcl\_usage</span></span>             | <span data-ttu-id="17d36-126">x</span><span class="sxs-lookup"><span data-stu-id="17d36-126">x</span></span>    | <span data-ttu-id="17d36-127">x</span><span class="sxs-lookup"><span data-stu-id="17d36-127">x</span></span>    | <span data-ttu-id="17d36-128">x</span><span class="sxs-lookup"><span data-stu-id="17d36-128">x</span></span>    | <span data-ttu-id="17d36-129">x</span><span class="sxs-lookup"><span data-stu-id="17d36-129">x</span></span>     | <span data-ttu-id="17d36-130">x</span><span class="sxs-lookup"><span data-stu-id="17d36-130">x</span></span>    | <span data-ttu-id="17d36-131">x</span><span class="sxs-lookup"><span data-stu-id="17d36-131">x</span></span>     |



 

<span data-ttu-id="17d36-132">Todas \_ las instrucciones de uso de DCL deben aparecer antes de la primera instrucción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="17d36-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17d36-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17d36-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d36-134">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="17d36-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 