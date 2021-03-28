---
title: CND-PS
description: Condicionalmente elige entre SRC1 y src2, en función de la comparación src0 0,5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1fd3a14e2ac4bd283a4e67724fbb42ac965ea707
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148993"
---
# <a name="cnd---ps"></a><span data-ttu-id="5b5d7-103">CND-PS</span><span class="sxs-lookup"><span data-stu-id="5b5d7-103">cnd - ps</span></span>

<span data-ttu-id="5b5d7-104">Condicionalmente elige entre SRC1 y src2, en función de la comparación src0 > 0,5.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-104">Conditionally chooses between src1 and src2, based on the comparison src0 > 0.5.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5d7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b5d7-105">Syntax</span></span>



| <span data-ttu-id="5b5d7-106">CND DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="5b5d7-106">cnd dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="5b5d7-107">, donde</span><span class="sxs-lookup"><span data-stu-id="5b5d7-107">where</span></span>

-   <span data-ttu-id="5b5d7-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-108">dst is the destination register.</span></span>
-   <span data-ttu-id="5b5d7-109">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-109">src0 is a source register.</span></span>
-   <span data-ttu-id="5b5d7-110">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-110">src1 is a source register.</span></span>
-   <span data-ttu-id="5b5d7-111">src2 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5d7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b5d7-112">Remarks</span></span>



| <span data-ttu-id="5b5d7-113">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5b5d7-113">Pixel shader versions</span></span> | <span data-ttu-id="5b5d7-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b5d7-114">1\_1</span></span> | <span data-ttu-id="5b5d7-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="5b5d7-115">1\_2</span></span> | <span data-ttu-id="5b5d7-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5b5d7-116">1\_3</span></span> | <span data-ttu-id="5b5d7-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="5b5d7-117">1\_4</span></span> | <span data-ttu-id="5b5d7-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b5d7-118">2\_0</span></span> | <span data-ttu-id="5b5d7-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b5d7-119">2\_x</span></span> | <span data-ttu-id="5b5d7-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b5d7-120">2\_sw</span></span> | <span data-ttu-id="5b5d7-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b5d7-121">3\_0</span></span> | <span data-ttu-id="5b5d7-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b5d7-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5b5d7-123">cnd</span><span class="sxs-lookup"><span data-stu-id="5b5d7-123">cnd</span></span>                   | <span data-ttu-id="5b5d7-124">x</span><span class="sxs-lookup"><span data-stu-id="5b5d7-124">x</span></span>    | <span data-ttu-id="5b5d7-125">x</span><span class="sxs-lookup"><span data-stu-id="5b5d7-125">x</span></span>    | <span data-ttu-id="5b5d7-126">x</span><span class="sxs-lookup"><span data-stu-id="5b5d7-126">x</span></span>    | <span data-ttu-id="5b5d7-127">x</span><span class="sxs-lookup"><span data-stu-id="5b5d7-127">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="5b5d7-128">En el caso de las versiones 1 \_ a 1 \_ 3, src0 debe ser R0. a.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-128">For versions 1\_1 to 1\_3, src0 must be r0.a.</span></span>


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



<span data-ttu-id="5b5d7-129">La versión 1 \_ 4 compara cada canal por separado.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-129">Version 1\_4 compares each channel separately.</span></span>


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



<span data-ttu-id="5b5d7-130">En estos ejemplos se muestra una comparación de cuatro canales realizada en un sombreador de la versión 1 \_ 4, así como una comparación de canal único posible en un sombreador de la versión 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-130">These examples show a four-channel comparison done in a version 1\_4 shader, as well as a single-channel comparison possible in a version 1\_1 shader.</span></span>


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



<span data-ttu-id="5b5d7-131">La versión 1 \_ 1 a 1 \_ 3 se compara únicamente con el canal alfa replicado de R0.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-131">Version 1\_1 to 1\_3 compares against the replicated alpha channel of r0 only.</span></span>


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



<span data-ttu-id="5b5d7-132">En este ejemplo se comparan dos valores, A y B. En el ejemplo se da por supuesto que se carga en V0 y B en v1.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-132">This example compares two values, A and B. The example assumes A is loaded into v0 and B is loaded into v1.</span></span> <span data-ttu-id="5b5d7-133">A y B deben estar en el intervalo de-1 a + 1, y dado que los registros de color (VN) se definen para estar entre 0 y 1, la restricción se cumple en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5b5d7-133">Both A and B must be in the range of -1 to +1, and since the color registers (vₙ) are defined to be between 0 and 1, the restriction happens to be satisfied in this example.</span></span>


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a><span data-ttu-id="5b5d7-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b5d7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b5d7-135">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5b5d7-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




