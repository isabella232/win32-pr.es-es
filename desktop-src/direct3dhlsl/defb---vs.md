---
title: defb-vs
description: Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995280"
---
# <a name="defb---vs"></a><span data-ttu-id="5a00e-103">defb-vs</span><span class="sxs-lookup"><span data-stu-id="5a00e-103">defb - vs</span></span>

<span data-ttu-id="5a00e-104">Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a00e-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a00e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a00e-105">Syntax</span></span>



| <span data-ttu-id="5a00e-106">defb Dest, booleanValue</span><span class="sxs-lookup"><span data-stu-id="5a00e-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="5a00e-107">, donde</span><span class="sxs-lookup"><span data-stu-id="5a00e-107">where</span></span>

-   <span data-ttu-id="5a00e-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5a00e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="5a00e-109">booleanValue es un valor booleano, ya sea true o false.</span><span class="sxs-lookup"><span data-stu-id="5a00e-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a00e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a00e-110">Remarks</span></span>



| <span data-ttu-id="5a00e-111">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5a00e-111">Vertex shader versions</span></span> | <span data-ttu-id="5a00e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="5a00e-112">1\_1</span></span> | <span data-ttu-id="5a00e-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a00e-113">2\_0</span></span> | <span data-ttu-id="5a00e-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a00e-114">2\_x</span></span> | <span data-ttu-id="5a00e-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5a00e-115">2\_sw</span></span> | <span data-ttu-id="5a00e-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a00e-116">3\_0</span></span> | <span data-ttu-id="5a00e-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5a00e-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5a00e-118">defb</span><span class="sxs-lookup"><span data-stu-id="5a00e-118">defb</span></span>                   |      | <span data-ttu-id="5a00e-119">x</span><span class="sxs-lookup"><span data-stu-id="5a00e-119">x</span></span>    | <span data-ttu-id="5a00e-120">x</span><span class="sxs-lookup"><span data-stu-id="5a00e-120">x</span></span>    | <span data-ttu-id="5a00e-121">x</span><span class="sxs-lookup"><span data-stu-id="5a00e-121">x</span></span>     | <span data-ttu-id="5a00e-122">x</span><span class="sxs-lookup"><span data-stu-id="5a00e-122">x</span></span>    | <span data-ttu-id="5a00e-123">x</span><span class="sxs-lookup"><span data-stu-id="5a00e-123">x</span></span>     |



 

<span data-ttu-id="5a00e-124">La instrucción defb-vs define una constante de sombreador booleano cuyo valor se carga cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a00e-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="5a00e-125">Se denominan constantes inmediatas.</span><span class="sxs-lookup"><span data-stu-id="5a00e-125">These are called immediate constants.</span></span> <span data-ttu-id="5a00e-126">Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetVertexShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="5a00e-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="5a00e-127">Hay dos maneras de establecer una constante booleana en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="5a00e-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="5a00e-128">Use defb-vs para definir la constante directamente dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="5a00e-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="5a00e-129">Use los métodos de la API para establecer una constante.</span><span class="sxs-lookup"><span data-stu-id="5a00e-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="5a00e-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) para establecer una constante booleana.</span><span class="sxs-lookup"><span data-stu-id="5a00e-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a00e-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a00e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a00e-132">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5a00e-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="5a00e-133">DEF-vs</span><span class="sxs-lookup"><span data-stu-id="5a00e-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="5a00e-134">defi-vs</span><span class="sxs-lookup"><span data-stu-id="5a00e-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 