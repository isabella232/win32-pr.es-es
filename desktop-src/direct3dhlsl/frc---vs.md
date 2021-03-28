---
title: FRC-vs
description: Devuelve la parte fraccionaria de cada componente de entrada. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362281"
---
# <a name="frc---vs"></a><span data-ttu-id="971f0-104">FRC-vs</span><span class="sxs-lookup"><span data-stu-id="971f0-104">frc - vs</span></span>

<span data-ttu-id="971f0-105">Devuelve la parte fraccionaria de cada componente de entrada.</span><span class="sxs-lookup"><span data-stu-id="971f0-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="971f0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="971f0-106">Syntax</span></span>



| <span data-ttu-id="971f0-107">FRC DST, src</span><span class="sxs-lookup"><span data-stu-id="971f0-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="971f0-108">, donde</span><span class="sxs-lookup"><span data-stu-id="971f0-108">where</span></span>

-   <span data-ttu-id="971f0-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="971f0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="971f0-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="971f0-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="971f0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="971f0-111">Remarks</span></span>



| <span data-ttu-id="971f0-112">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="971f0-112">Vertex shader versions</span></span> | <span data-ttu-id="971f0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="971f0-113">1\_1</span></span> | <span data-ttu-id="971f0-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="971f0-114">2\_0</span></span> | <span data-ttu-id="971f0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="971f0-115">2\_x</span></span> | <span data-ttu-id="971f0-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="971f0-116">2\_sw</span></span> | <span data-ttu-id="971f0-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="971f0-117">3\_0</span></span> | <span data-ttu-id="971f0-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="971f0-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="971f0-119">frc</span><span class="sxs-lookup"><span data-stu-id="971f0-119">frc</span></span>                    | <span data-ttu-id="971f0-120">x</span><span class="sxs-lookup"><span data-stu-id="971f0-120">x</span></span>    | <span data-ttu-id="971f0-121">x</span><span class="sxs-lookup"><span data-stu-id="971f0-121">x</span></span>    | <span data-ttu-id="971f0-122">x</span><span class="sxs-lookup"><span data-stu-id="971f0-122">x</span></span>    | <span data-ttu-id="971f0-123">x</span><span class="sxs-lookup"><span data-stu-id="971f0-123">x</span></span>     | <span data-ttu-id="971f0-124">x</span><span class="sxs-lookup"><span data-stu-id="971f0-124">x</span></span>    | <span data-ttu-id="971f0-125">x</span><span class="sxs-lookup"><span data-stu-id="971f0-125">x</span></span>     |



 

<span data-ttu-id="971f0-126">En el fragmento de código siguiente se muestra conceptualmente cómo funciona la instrucción.</span><span class="sxs-lookup"><span data-stu-id="971f0-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="971f0-127">La función Floor convierte el argumento que se pasa al entero más grande que es menor o igual que el argumento.</span><span class="sxs-lookup"><span data-stu-id="971f0-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="971f0-128">Esto se convierte en un valor float y, a continuación, se resta pantalla el valor original.</span><span class="sxs-lookup"><span data-stu-id="971f0-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="971f0-129">El valor fraccionario resultante oscila entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="971f0-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="971f0-130">En el caso de la versión 1 \_ , las máscaras de escritura permitidas son. y y. XY (no se permite).</span><span class="sxs-lookup"><span data-stu-id="971f0-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="971f0-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="971f0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="971f0-132">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="971f0-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




