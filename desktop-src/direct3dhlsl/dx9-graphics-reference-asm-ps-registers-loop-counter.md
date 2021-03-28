---
title: Registro de contadores de bucle (referencia de PS de HLSL)
description: El único registro de este banco es el registro del contador de bucle actual (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785075"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="f26c2-103">Registro de contadores de bucle (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="f26c2-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="f26c2-104">El único registro de este banco es el registro del contador de bucle actual (aL).</span><span class="sxs-lookup"><span data-stu-id="f26c2-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="f26c2-105">Se incrementa automáticamente en cada ejecución del bloque [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f26c2-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="f26c2-106">Por lo tanto, se puede usar en el bloque para el direccionamiento relativo si es necesario y no es válido para usarlo fuera del bucle.</span><span class="sxs-lookup"><span data-stu-id="f26c2-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="f26c2-107">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f26c2-107">Pixel shader versions</span></span> | <span data-ttu-id="f26c2-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="f26c2-108">1\_1</span></span> | <span data-ttu-id="f26c2-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="f26c2-109">1\_2</span></span> | <span data-ttu-id="f26c2-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f26c2-110">1\_3</span></span> | <span data-ttu-id="f26c2-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="f26c2-111">1\_4</span></span> | <span data-ttu-id="f26c2-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f26c2-112">2\_0</span></span> | <span data-ttu-id="f26c2-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f26c2-113">2\_sw</span></span> | <span data-ttu-id="f26c2-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f26c2-114">2\_x</span></span> | <span data-ttu-id="f26c2-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f26c2-115">3\_0</span></span> | <span data-ttu-id="f26c2-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f26c2-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="f26c2-117">Registro de contador de bucle</span><span class="sxs-lookup"><span data-stu-id="f26c2-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="f26c2-118">x</span><span class="sxs-lookup"><span data-stu-id="f26c2-118">x</span></span>    | <span data-ttu-id="f26c2-119">x</span><span class="sxs-lookup"><span data-stu-id="f26c2-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="f26c2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f26c2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f26c2-121">Registra</span><span class="sxs-lookup"><span data-stu-id="f26c2-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




