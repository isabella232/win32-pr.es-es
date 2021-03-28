---
title: FRC-PS
description: Devuelve la parte fraccionaria de cada componente de entrada. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362282"
---
# <a name="frc---ps"></a><span data-ttu-id="8cb39-104">FRC-PS</span><span class="sxs-lookup"><span data-stu-id="8cb39-104">frc - ps</span></span>

<span data-ttu-id="8cb39-105">Devuelve la parte fraccionaria de cada componente de entrada.</span><span class="sxs-lookup"><span data-stu-id="8cb39-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb39-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cb39-106">Syntax</span></span>



| <span data-ttu-id="8cb39-107">FRC DST, src</span><span class="sxs-lookup"><span data-stu-id="8cb39-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="8cb39-108">, donde</span><span class="sxs-lookup"><span data-stu-id="8cb39-108">where</span></span>

-   <span data-ttu-id="8cb39-109">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="8cb39-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8cb39-110">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="8cb39-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cb39-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cb39-111">Remarks</span></span>



| <span data-ttu-id="8cb39-112">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8cb39-112">Pixel shader versions</span></span> | <span data-ttu-id="8cb39-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="8cb39-113">1\_1</span></span> | <span data-ttu-id="8cb39-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="8cb39-114">1\_2</span></span> | <span data-ttu-id="8cb39-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8cb39-115">1\_3</span></span> | <span data-ttu-id="8cb39-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="8cb39-116">1\_4</span></span> | <span data-ttu-id="8cb39-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8cb39-117">2\_0</span></span> | <span data-ttu-id="8cb39-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8cb39-118">2\_x</span></span> | <span data-ttu-id="8cb39-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8cb39-119">2\_sw</span></span> | <span data-ttu-id="8cb39-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8cb39-120">3\_0</span></span> | <span data-ttu-id="8cb39-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8cb39-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8cb39-122">frc</span><span class="sxs-lookup"><span data-stu-id="8cb39-122">frc</span></span>                   |      |      |      |      | <span data-ttu-id="8cb39-123">x</span><span class="sxs-lookup"><span data-stu-id="8cb39-123">x</span></span>    | <span data-ttu-id="8cb39-124">x</span><span class="sxs-lookup"><span data-stu-id="8cb39-124">x</span></span>    | <span data-ttu-id="8cb39-125">x</span><span class="sxs-lookup"><span data-stu-id="8cb39-125">x</span></span>     | <span data-ttu-id="8cb39-126">x</span><span class="sxs-lookup"><span data-stu-id="8cb39-126">x</span></span>    | <span data-ttu-id="8cb39-127">x</span><span class="sxs-lookup"><span data-stu-id="8cb39-127">x</span></span>     |



 

<span data-ttu-id="8cb39-128">En el fragmento de código siguiente se muestra conceptualmente cómo funciona la instrucción.</span><span class="sxs-lookup"><span data-stu-id="8cb39-128">The following code snippet shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="8cb39-129">La función Floor convierte el argumento que se pasa al entero más grande que es menor o igual que el argumento.</span><span class="sxs-lookup"><span data-stu-id="8cb39-129">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="8cb39-130">Esto se convierte en un valor float y, a continuación, se resta pantalla el valor original.</span><span class="sxs-lookup"><span data-stu-id="8cb39-130">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="8cb39-131">El valor fraccionario resultante oscila entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="8cb39-131">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cb39-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cb39-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cb39-133">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="8cb39-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




