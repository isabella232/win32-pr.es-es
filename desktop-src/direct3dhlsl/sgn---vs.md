---
title: SGN-vs
description: Calcula el signo de la entrada.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419936"
---
# <a name="sgn---vs"></a><span data-ttu-id="d0307-103">SGN-vs</span><span class="sxs-lookup"><span data-stu-id="d0307-103">sgn - vs</span></span>

<span data-ttu-id="d0307-104">Calcula el signo de la entrada.</span><span class="sxs-lookup"><span data-stu-id="d0307-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0307-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0307-105">Syntax</span></span>



| <span data-ttu-id="d0307-106">SGN DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="d0307-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="d0307-107">, donde</span><span class="sxs-lookup"><span data-stu-id="d0307-107">where</span></span>

-   <span data-ttu-id="d0307-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="d0307-108">dst is the destination register.</span></span>
-   <span data-ttu-id="d0307-109">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="d0307-109">src0 is a source register.</span></span>
-   <span data-ttu-id="d0307-110">SRC1 es un registro temporal que contiene resultados intermedios.</span><span class="sxs-lookup"><span data-stu-id="d0307-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="d0307-111">Tras la ejecución, el contenido es indefinido.</span><span class="sxs-lookup"><span data-stu-id="d0307-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="d0307-112">src2 es un registro temporal que contiene resultados intermedios.</span><span class="sxs-lookup"><span data-stu-id="d0307-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="d0307-113">Tras la ejecución, el contenido es indefinido.</span><span class="sxs-lookup"><span data-stu-id="d0307-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0307-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0307-114">Remarks</span></span>



| <span data-ttu-id="d0307-115">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d0307-115">Vertex shader versions</span></span> | <span data-ttu-id="d0307-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="d0307-116">1\_1</span></span> | <span data-ttu-id="d0307-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0307-117">2\_0</span></span> | <span data-ttu-id="d0307-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d0307-118">2\_x</span></span> | <span data-ttu-id="d0307-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d0307-119">2\_sw</span></span> | <span data-ttu-id="d0307-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0307-120">3\_0</span></span> | <span data-ttu-id="d0307-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d0307-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d0307-122">signo</span><span class="sxs-lookup"><span data-stu-id="d0307-122">sgn</span></span>                    |      | <span data-ttu-id="d0307-123">x</span><span class="sxs-lookup"><span data-stu-id="d0307-123">x</span></span>    | <span data-ttu-id="d0307-124">x</span><span class="sxs-lookup"><span data-stu-id="d0307-124">x</span></span>    | <span data-ttu-id="d0307-125">x</span><span class="sxs-lookup"><span data-stu-id="d0307-125">x</span></span>     | <span data-ttu-id="d0307-126">x</span><span class="sxs-lookup"><span data-stu-id="d0307-126">x</span></span>    | <span data-ttu-id="d0307-127">x</span><span class="sxs-lookup"><span data-stu-id="d0307-127">x</span></span>     |



 

<span data-ttu-id="d0307-128">Esta instrucción funciona como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d0307-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="d0307-129">SRC1 y src2 deben ser [registros temporales](dx9-graphics-reference-asm-vs-registers-temporary.md)diferentes.</span><span class="sxs-lookup"><span data-stu-id="d0307-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0307-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0307-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0307-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d0307-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




