---
title: Lit-vs
description: Proporciona compatibilidad parcial para la iluminación mediante el cálculo de los coeficientes de iluminación de dos productos DOT y un exponente.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983858"
---
# <a name="lit---vs"></a><span data-ttu-id="c0208-103">Lit-vs</span><span class="sxs-lookup"><span data-stu-id="c0208-103">lit - vs</span></span>

<span data-ttu-id="c0208-104">Proporciona compatibilidad parcial para la iluminación mediante el cálculo de los coeficientes de iluminación de dos productos DOT y un exponente.</span><span class="sxs-lookup"><span data-stu-id="c0208-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0208-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0208-105">Syntax</span></span>



| <span data-ttu-id="c0208-106">Lit DST, src</span><span class="sxs-lookup"><span data-stu-id="c0208-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="c0208-107">, donde</span><span class="sxs-lookup"><span data-stu-id="c0208-107">where</span></span>

-   <span data-ttu-id="c0208-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c0208-108">dst is the destination register.</span></span>
-   <span data-ttu-id="c0208-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="c0208-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0208-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0208-110">Remarks</span></span>



| <span data-ttu-id="c0208-111">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c0208-111">Vertex shader versions</span></span> | <span data-ttu-id="c0208-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="c0208-112">1\_1</span></span> | <span data-ttu-id="c0208-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0208-113">2\_0</span></span> | <span data-ttu-id="c0208-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c0208-114">2\_x</span></span> | <span data-ttu-id="c0208-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c0208-115">2\_sw</span></span> | <span data-ttu-id="c0208-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0208-116">3\_0</span></span> | <span data-ttu-id="c0208-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c0208-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c0208-118">encender</span><span class="sxs-lookup"><span data-stu-id="c0208-118">lit</span></span>                    | <span data-ttu-id="c0208-119">x</span><span class="sxs-lookup"><span data-stu-id="c0208-119">x</span></span>    | <span data-ttu-id="c0208-120">x</span><span class="sxs-lookup"><span data-stu-id="c0208-120">x</span></span>    | <span data-ttu-id="c0208-121">x</span><span class="sxs-lookup"><span data-stu-id="c0208-121">x</span></span>    | <span data-ttu-id="c0208-122">x</span><span class="sxs-lookup"><span data-stu-id="c0208-122">x</span></span>     | <span data-ttu-id="c0208-123">x</span><span class="sxs-lookup"><span data-stu-id="c0208-123">x</span></span>    | <span data-ttu-id="c0208-124">x</span><span class="sxs-lookup"><span data-stu-id="c0208-124">x</span></span>     |



 

<span data-ttu-id="c0208-125">Se supone que el vector de origen contiene los valores que se muestran en el siguiente pseudocódigo.</span><span class="sxs-lookup"><span data-stu-id="c0208-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="c0208-126">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="c0208-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="c0208-127">La aritmética de precisión reducida es aceptable en la evaluación del componente y de destino (dest. y).</span><span class="sxs-lookup"><span data-stu-id="c0208-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="c0208-128">Una implementación de debe admitir al menos ocho bits de fracción en el argumento de potencia.</span><span class="sxs-lookup"><span data-stu-id="c0208-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="c0208-129">Los productos de punto se calculan con vectores normalizados y los límites de la abrazadera son de-128 a 128.</span><span class="sxs-lookup"><span data-stu-id="c0208-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="c0208-130">El error debe corresponder a una combinación [logP-vs](logp---vs.md) y [exp-vs](exp---vs.md) , o no más de aproximadamente un bit significativo para un componente de color de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c0208-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0208-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0208-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0208-132">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c0208-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




