---
title: Mad-PS
description: Multiplicar y agregar instrucción. Establece el registro de destino en (src0 \ SRC1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419947"
---
# <a name="mad---ps"></a><span data-ttu-id="cfe71-104">Mad-PS</span><span class="sxs-lookup"><span data-stu-id="cfe71-104">mad - ps</span></span>

<span data-ttu-id="cfe71-105">Multiplicar y agregar instrucción.</span><span class="sxs-lookup"><span data-stu-id="cfe71-105">Multiply and add instruction.</span></span> <span data-ttu-id="cfe71-106">Establece el registro de destino en (src0 \* SRC1) + src2.</span><span class="sxs-lookup"><span data-stu-id="cfe71-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe71-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe71-107">Syntax</span></span>



| <span data-ttu-id="cfe71-108">Mad DST, src0, SRC1, src2</span><span class="sxs-lookup"><span data-stu-id="cfe71-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="cfe71-109">, donde</span><span class="sxs-lookup"><span data-stu-id="cfe71-109">where</span></span>

-   <span data-ttu-id="cfe71-110">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="cfe71-110">dst is the destination register.</span></span>
-   <span data-ttu-id="cfe71-111">src0 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="cfe71-111">src0 is a source register.</span></span>
-   <span data-ttu-id="cfe71-112">SRC1 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="cfe71-112">src1 is a source register.</span></span>
-   <span data-ttu-id="cfe71-113">src2 es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="cfe71-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe71-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfe71-114">Remarks</span></span>



| <span data-ttu-id="cfe71-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="cfe71-115">Pixel shader versions</span></span> | <span data-ttu-id="cfe71-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="cfe71-116">1\_1</span></span> | <span data-ttu-id="cfe71-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="cfe71-117">1\_2</span></span> | <span data-ttu-id="cfe71-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cfe71-118">1\_3</span></span> | <span data-ttu-id="cfe71-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="cfe71-119">1\_4</span></span> | <span data-ttu-id="cfe71-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cfe71-120">2\_0</span></span> | <span data-ttu-id="cfe71-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cfe71-121">2\_x</span></span> | <span data-ttu-id="cfe71-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cfe71-122">2\_sw</span></span> | <span data-ttu-id="cfe71-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cfe71-123">3\_0</span></span> | <span data-ttu-id="cfe71-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cfe71-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cfe71-125">Mad</span><span class="sxs-lookup"><span data-stu-id="cfe71-125">mad</span></span>                   | <span data-ttu-id="cfe71-126">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-126">x</span></span>    | <span data-ttu-id="cfe71-127">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-127">x</span></span>    | <span data-ttu-id="cfe71-128">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-128">x</span></span>    | <span data-ttu-id="cfe71-129">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-129">x</span></span>    | <span data-ttu-id="cfe71-130">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-130">x</span></span>    | <span data-ttu-id="cfe71-131">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-131">x</span></span>    | <span data-ttu-id="cfe71-132">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-132">x</span></span>     | <span data-ttu-id="cfe71-133">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-133">x</span></span>    | <span data-ttu-id="cfe71-134">x</span><span class="sxs-lookup"><span data-stu-id="cfe71-134">x</span></span>     |



 

<span data-ttu-id="cfe71-135">En el fragmento de código siguiente se muestran las operaciones realizadas.</span><span class="sxs-lookup"><span data-stu-id="cfe71-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="cfe71-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cfe71-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfe71-137">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="cfe71-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




