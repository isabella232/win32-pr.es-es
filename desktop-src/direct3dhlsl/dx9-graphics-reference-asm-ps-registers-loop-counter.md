---
title: Registro de contador de bucles (referencia de HLSL PS)
description: Obtenga información sobre el registro del contador de bucles para sombreadores de píxeles. El único registro de este banco es el registro del contador de bucles (aL) actual.
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405518"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="c7176-104">Registro de contador de bucles (referencia de HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="c7176-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="c7176-105">El único registro de este banco es el registro del contador de bucles (aL) actual.</span><span class="sxs-lookup"><span data-stu-id="c7176-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="c7176-106">Se incrementa automáticamente en cada ejecución del [bucle - ps](loop---ps.md) / [endloop - ps](endloop---ps.md) block.</span><span class="sxs-lookup"><span data-stu-id="c7176-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="c7176-107">Por lo tanto, se puede usar en el bloque para el direccionamiento relativo si es necesario y no es válido usarlo fuera del bucle.</span><span class="sxs-lookup"><span data-stu-id="c7176-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="c7176-108">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="c7176-108">Pixel shader versions</span></span> | <span data-ttu-id="c7176-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="c7176-109">1\_1</span></span> | <span data-ttu-id="c7176-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="c7176-110">1\_2</span></span> | <span data-ttu-id="c7176-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c7176-111">1\_3</span></span> | <span data-ttu-id="c7176-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="c7176-112">1\_4</span></span> | <span data-ttu-id="c7176-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7176-113">2\_0</span></span> | <span data-ttu-id="c7176-114">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7176-114">2\_sw</span></span> | <span data-ttu-id="c7176-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c7176-115">2\_x</span></span> | <span data-ttu-id="c7176-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c7176-116">3\_0</span></span> | <span data-ttu-id="c7176-117">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c7176-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="c7176-118">Registro de contador de bucles</span><span class="sxs-lookup"><span data-stu-id="c7176-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="c7176-119">x</span><span class="sxs-lookup"><span data-stu-id="c7176-119">x</span></span>    | <span data-ttu-id="c7176-120">x</span><span class="sxs-lookup"><span data-stu-id="c7176-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="c7176-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7176-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7176-122">Registros</span><span class="sxs-lookup"><span data-stu-id="c7176-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




