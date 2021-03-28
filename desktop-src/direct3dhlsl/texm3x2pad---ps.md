---
title: texm3x2pad-PS
description: Realiza la multiplicación de la primera fila de una matriz de dos filas. Esta instrucción debe combinarse con texm3x2tex-PS o texm3x2depth-PS. Consulte cualquiera de estas instrucciones para obtener más información sobre el uso de texmpad.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904294"
---
# <a name="texm3x2pad---ps"></a><span data-ttu-id="59666-105">texm3x2pad-PS</span><span class="sxs-lookup"><span data-stu-id="59666-105">texm3x2pad - ps</span></span>

<span data-ttu-id="59666-106">Realiza la multiplicación de la primera fila de una matriz de dos filas.</span><span class="sxs-lookup"><span data-stu-id="59666-106">Performs the first row multiplication of a two-row matrix multiply.</span></span> <span data-ttu-id="59666-107">Esta instrucción debe combinarse con [texm3x2tex-PS](texm3x2tex---ps.md) o [texm3x2depth-PS](texm3x2depth---ps.md).</span><span class="sxs-lookup"><span data-stu-id="59666-107">This instruction must be combined with either [texm3x2tex - ps](texm3x2tex---ps.md) or [texm3x2depth - ps](texm3x2depth---ps.md).</span></span> <span data-ttu-id="59666-108">Consulte cualquiera de estas instrucciones para obtener más información sobre el uso de texmpad.</span><span class="sxs-lookup"><span data-stu-id="59666-108">Refer to either of these instructions for details on using texmpad.</span></span>

## <a name="syntax"></a><span data-ttu-id="59666-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59666-109">Syntax</span></span>



| <span data-ttu-id="59666-110">tex3x2pad DST, src</span><span class="sxs-lookup"><span data-stu-id="59666-110">tex3x2pad dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="59666-111">, donde</span><span class="sxs-lookup"><span data-stu-id="59666-111">where</span></span>

-   <span data-ttu-id="59666-112">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="59666-112">dst is the destination register.</span></span>
-   <span data-ttu-id="59666-113">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="59666-113">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="59666-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59666-114">Remarks</span></span>



| <span data-ttu-id="59666-115">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="59666-115">Pixel shader versions</span></span> | <span data-ttu-id="59666-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="59666-116">1\_1</span></span> | <span data-ttu-id="59666-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="59666-117">1\_2</span></span> | <span data-ttu-id="59666-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="59666-118">1\_3</span></span> | <span data-ttu-id="59666-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="59666-119">1\_4</span></span> | <span data-ttu-id="59666-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59666-120">2\_0</span></span> | <span data-ttu-id="59666-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="59666-121">2\_x</span></span> | <span data-ttu-id="59666-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59666-122">2\_sw</span></span> | <span data-ttu-id="59666-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59666-123">3\_0</span></span> | <span data-ttu-id="59666-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="59666-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="59666-125">texm3x2pad</span><span class="sxs-lookup"><span data-stu-id="59666-125">texm3x2pad</span></span>            | <span data-ttu-id="59666-126">x</span><span class="sxs-lookup"><span data-stu-id="59666-126">x</span></span>    | <span data-ttu-id="59666-127">x</span><span class="sxs-lookup"><span data-stu-id="59666-127">x</span></span>    | <span data-ttu-id="59666-128">x</span><span class="sxs-lookup"><span data-stu-id="59666-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="59666-129">Esta instrucción no se puede usar por sí sola.</span><span class="sxs-lookup"><span data-stu-id="59666-129">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59666-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59666-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59666-131">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="59666-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




