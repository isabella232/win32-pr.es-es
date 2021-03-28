---
title: MOV-vs
description: Mueve los datos de punto flotante entre los registros.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784990"
---
# <a name="mov---vs"></a><span data-ttu-id="2de0b-103">MOV-vs</span><span class="sxs-lookup"><span data-stu-id="2de0b-103">mov - vs</span></span>

<span data-ttu-id="2de0b-104">Mueve los datos de punto flotante entre los registros.</span><span class="sxs-lookup"><span data-stu-id="2de0b-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2de0b-105">Syntax</span></span>



| <span data-ttu-id="2de0b-106">MOV. DST, src</span><span class="sxs-lookup"><span data-stu-id="2de0b-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="2de0b-107">, donde</span><span class="sxs-lookup"><span data-stu-id="2de0b-107">where</span></span>

-   <span data-ttu-id="2de0b-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="2de0b-108">dst is the destination register.</span></span>
-   <span data-ttu-id="2de0b-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="2de0b-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de0b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2de0b-110">Remarks</span></span>



| <span data-ttu-id="2de0b-111">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2de0b-111">Vertex shader versions</span></span> | <span data-ttu-id="2de0b-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2de0b-112">1\_1</span></span> | <span data-ttu-id="2de0b-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2de0b-113">2\_0</span></span> | <span data-ttu-id="2de0b-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2de0b-114">2\_x</span></span> | <span data-ttu-id="2de0b-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2de0b-115">2\_sw</span></span> | <span data-ttu-id="2de0b-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2de0b-116">3\_0</span></span> | <span data-ttu-id="2de0b-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2de0b-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2de0b-118">MOV</span><span class="sxs-lookup"><span data-stu-id="2de0b-118">mov</span></span>                    | <span data-ttu-id="2de0b-119">x</span><span class="sxs-lookup"><span data-stu-id="2de0b-119">x</span></span>    | <span data-ttu-id="2de0b-120">x</span><span class="sxs-lookup"><span data-stu-id="2de0b-120">x</span></span>    | <span data-ttu-id="2de0b-121">x</span><span class="sxs-lookup"><span data-stu-id="2de0b-121">x</span></span>    | <span data-ttu-id="2de0b-122">x</span><span class="sxs-lookup"><span data-stu-id="2de0b-122">x</span></span>     | <span data-ttu-id="2de0b-123">x</span><span class="sxs-lookup"><span data-stu-id="2de0b-123">x</span></span>    | <span data-ttu-id="2de0b-124">x</span><span class="sxs-lookup"><span data-stu-id="2de0b-124">x</span></span>     |



 

<span data-ttu-id="2de0b-125">Se puede usar para datos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="2de0b-125">Can be used for floating point data.</span></span> <span data-ttu-id="2de0b-126">En el caso de la versión frente \_ \_ a 1 1, también se puede utilizar para escribir el registro de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2de0b-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="2de0b-127">Cuando se utiliza para actualizar los registros de direcciones, los valores se convierten del punto flotante mediante el redondeo al más próximo.</span><span class="sxs-lookup"><span data-stu-id="2de0b-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="2de0b-128">En el siguiente fragmento de código se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="2de0b-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="2de0b-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2de0b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de0b-130">Instrucciones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2de0b-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




