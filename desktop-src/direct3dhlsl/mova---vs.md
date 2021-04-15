---
title: mova-vs
description: Mueva los datos desde un registro de punto flotante al registro de direcciones, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983898"
---
# <a name="mova---vs"></a><span data-ttu-id="3cd82-103">mova-vs</span><span class="sxs-lookup"><span data-stu-id="3cd82-103">mova - vs</span></span>

<span data-ttu-id="3cd82-104">Mueva los datos desde un registro de punto flotante al [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="3cd82-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd82-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3cd82-105">Syntax</span></span>



| <span data-ttu-id="3cd82-106">mova DST, src</span><span class="sxs-lookup"><span data-stu-id="3cd82-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="3cd82-107">, donde</span><span class="sxs-lookup"><span data-stu-id="3cd82-107">where</span></span>

-   <span data-ttu-id="3cd82-108">DST debe ser el [registro de direcciones](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="3cd82-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="3cd82-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="3cd82-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd82-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cd82-110">Remarks</span></span>



| <span data-ttu-id="3cd82-111">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3cd82-111">Vertex shader versions</span></span> | <span data-ttu-id="3cd82-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="3cd82-112">1\_1</span></span> | <span data-ttu-id="3cd82-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3cd82-113">2\_0</span></span> | <span data-ttu-id="3cd82-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3cd82-114">2\_x</span></span> | <span data-ttu-id="3cd82-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3cd82-115">2\_sw</span></span> | <span data-ttu-id="3cd82-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3cd82-116">3\_0</span></span> | <span data-ttu-id="3cd82-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3cd82-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3cd82-118">mova</span><span class="sxs-lookup"><span data-stu-id="3cd82-118">mova</span></span>                   |      | <span data-ttu-id="3cd82-119">x</span><span class="sxs-lookup"><span data-stu-id="3cd82-119">x</span></span>    | <span data-ttu-id="3cd82-120">x</span><span class="sxs-lookup"><span data-stu-id="3cd82-120">x</span></span>    | <span data-ttu-id="3cd82-121">x</span><span class="sxs-lookup"><span data-stu-id="3cd82-121">x</span></span>     | <span data-ttu-id="3cd82-122">x</span><span class="sxs-lookup"><span data-stu-id="3cd82-122">x</span></span>    | <span data-ttu-id="3cd82-123">x</span><span class="sxs-lookup"><span data-stu-id="3cd82-123">x</span></span>     |



 

<span data-ttu-id="3cd82-124">Mueve los datos de punto flotante a un registro entero.</span><span class="sxs-lookup"><span data-stu-id="3cd82-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="3cd82-125">Los valores se convierten del punto flotante utilizando el redondeo al más próximo.</span><span class="sxs-lookup"><span data-stu-id="3cd82-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="3cd82-126">El registro de direcciones es el único registro de destino permitido.</span><span class="sxs-lookup"><span data-stu-id="3cd82-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="3cd82-127">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="3cd82-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="3cd82-128">En el caso de las versiones 2 \_ x y posteriores, el registro de direcciones es un vector de componente.</span><span class="sxs-lookup"><span data-stu-id="3cd82-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="3cd82-129">Por lo tanto, se permite cualquier máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="3cd82-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="3cd82-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cd82-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cd82-131">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3cd82-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




