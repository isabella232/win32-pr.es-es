---
title: defb-PS
description: Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793030"
---
# <a name="defb---ps"></a><span data-ttu-id="6df7c-103">defb-PS</span><span class="sxs-lookup"><span data-stu-id="6df7c-103">defb - ps</span></span>

<span data-ttu-id="6df7c-104">Define un valor constante booleano, que se debe cargar cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6df7c-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6df7c-105">Syntax</span></span>



| <span data-ttu-id="6df7c-106">defb Dest, booleanValue</span><span class="sxs-lookup"><span data-stu-id="6df7c-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="6df7c-107">, donde</span><span class="sxs-lookup"><span data-stu-id="6df7c-107">where</span></span>

-   <span data-ttu-id="6df7c-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="6df7c-108">dst is the destination register.</span></span>
-   <span data-ttu-id="6df7c-109">booleanValue es un valor booleano único, ya sea true o false.</span><span class="sxs-lookup"><span data-stu-id="6df7c-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df7c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6df7c-110">Remarks</span></span>



| <span data-ttu-id="6df7c-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="6df7c-111">Pixel shader versions</span></span> | <span data-ttu-id="6df7c-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="6df7c-112">1\_1</span></span> | <span data-ttu-id="6df7c-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="6df7c-113">1\_2</span></span> | <span data-ttu-id="6df7c-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6df7c-114">1\_3</span></span> | <span data-ttu-id="6df7c-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="6df7c-115">1\_4</span></span> | <span data-ttu-id="6df7c-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6df7c-116">2\_0</span></span> | <span data-ttu-id="6df7c-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6df7c-117">2\_x</span></span> | <span data-ttu-id="6df7c-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6df7c-118">2\_sw</span></span> | <span data-ttu-id="6df7c-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6df7c-119">3\_0</span></span> | <span data-ttu-id="6df7c-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6df7c-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6df7c-121">defb</span><span class="sxs-lookup"><span data-stu-id="6df7c-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="6df7c-122">x</span><span class="sxs-lookup"><span data-stu-id="6df7c-122">x</span></span>    | <span data-ttu-id="6df7c-123">x</span><span class="sxs-lookup"><span data-stu-id="6df7c-123">x</span></span>     | <span data-ttu-id="6df7c-124">x</span><span class="sxs-lookup"><span data-stu-id="6df7c-124">x</span></span>    | <span data-ttu-id="6df7c-125">x</span><span class="sxs-lookup"><span data-stu-id="6df7c-125">x</span></span>     |



 

<span data-ttu-id="6df7c-126">La instrucción defb define una constante de sombreador booleana cuyo valor se carga cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6df7c-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="6df7c-127">Se denominan constantes inmediatas.</span><span class="sxs-lookup"><span data-stu-id="6df7c-127">These are called immediate constants.</span></span> <span data-ttu-id="6df7c-128">Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="6df7c-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="6df7c-129">Hay dos maneras de establecer un BooleanConstant en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="6df7c-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="6df7c-130">Use defb para definir la constante directamente dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="6df7c-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="6df7c-131">Use los métodos de la API para establecer una constante.</span><span class="sxs-lookup"><span data-stu-id="6df7c-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="6df7c-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para establecer una constante booleana.</span><span class="sxs-lookup"><span data-stu-id="6df7c-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6df7c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6df7c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df7c-134">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="6df7c-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="6df7c-135">DEF-PS</span><span class="sxs-lookup"><span data-stu-id="6df7c-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="6df7c-136">defi-PS</span><span class="sxs-lookup"><span data-stu-id="6df7c-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 