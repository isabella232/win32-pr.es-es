---
description: 'Esta sección contiene información acerca de las siguientes funciones de efecto:'
ms.assetid: b76643f0-387f-49c6-80e5-4d7b406b4db7
title: Funciones de efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111fdcb34bbf1d9a86a295e62f734938991dda99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539040"
---
# <a name="effect-functions-direct3d-10"></a><span data-ttu-id="d99e9-103">Funciones de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d99e9-103">Effect Functions (Direct3D 10)</span></span>

<span data-ttu-id="d99e9-104">Esta sección contiene información acerca de las siguientes funciones de efecto:</span><span class="sxs-lookup"><span data-stu-id="d99e9-104">This section contains information about the following effect functions:</span></span>



| <span data-ttu-id="d99e9-105">Functions</span><span class="sxs-lookup"><span data-stu-id="d99e9-105">Functions</span></span>                                                                      | <span data-ttu-id="d99e9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d99e9-106">Description</span></span>                                                         |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="d99e9-107">**D3D10CompileEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="d99e9-107">**D3D10CompileEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)           | <span data-ttu-id="d99e9-108">Compilar un efecto.</span><span class="sxs-lookup"><span data-stu-id="d99e9-108">Compile an effect.</span></span>                                                  |
| [<span data-ttu-id="d99e9-109">**D3D10CreateEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="d99e9-109">**D3D10CreateEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectfrommemory)             | <span data-ttu-id="d99e9-110">Cree un efecto.</span><span class="sxs-lookup"><span data-stu-id="d99e9-110">Create an effect.</span></span>                                                   |
| [<span data-ttu-id="d99e9-111">**D3D10CreateEffectPoolFromMemory**</span><span class="sxs-lookup"><span data-stu-id="d99e9-111">**D3D10CreateEffectPoolFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectpoolfrommemory)     | <span data-ttu-id="d99e9-112">Cree un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="d99e9-112">Create an effect pool.</span></span>                                              |
| [<span data-ttu-id="d99e9-113">**D3D10CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="d99e9-113">**D3D10CreateStateBlock**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createstateblock)                         | <span data-ttu-id="d99e9-114">Cree un bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="d99e9-114">Create a state block.</span></span>                                               |
| [<span data-ttu-id="d99e9-115">**D3D10DisassembleEffect**</span><span class="sxs-lookup"><span data-stu-id="d99e9-115">**D3D10DisassembleEffect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10disassembleeffect)                       | <span data-ttu-id="d99e9-116">Desensamblar un efecto compilado en las instrucciones de ensamblado de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d99e9-116">Disassemble a compiled effect into shader assembly instructions.</span></span>    |
| [<span data-ttu-id="d99e9-117">**D3D10StateBlockMaskDifference**</span><span class="sxs-lookup"><span data-stu-id="d99e9-117">**D3D10StateBlockMaskDifference**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdifference)         | <span data-ttu-id="d99e9-118">Combine dos máscaras de bloques de estado con una XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="d99e9-118">Combine two state-block masks with a bitwise XOR.</span></span>                   |
| [<span data-ttu-id="d99e9-119">**D3D10StateBlockMaskDisableAll**</span><span class="sxs-lookup"><span data-stu-id="d99e9-119">**D3D10StateBlockMaskDisableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisableall)         | <span data-ttu-id="d99e9-120">Deshabilitar la captura de estado.</span><span class="sxs-lookup"><span data-stu-id="d99e9-120">Disable state capturing.</span></span>                                            |
| [<span data-ttu-id="d99e9-121">**D3D10StateBlockMaskDisableCapture**</span><span class="sxs-lookup"><span data-stu-id="d99e9-121">**D3D10StateBlockMaskDisableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisablecapture) | <span data-ttu-id="d99e9-122">Deshabilitar la captura de estado con una máscara de bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="d99e9-122">Disable state capturing with a state-block mask.</span></span>                    |
| [<span data-ttu-id="d99e9-123">**D3D10StateBlockMaskEnableAll**</span><span class="sxs-lookup"><span data-stu-id="d99e9-123">**D3D10StateBlockMaskEnableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenableall)           | <span data-ttu-id="d99e9-124">Habilite una máscara de bloque de estado para capturar y aplicar todas las variables de estado.</span><span class="sxs-lookup"><span data-stu-id="d99e9-124">Enable a state-block mask to capture and apply all state variables.</span></span> |
| [<span data-ttu-id="d99e9-125">**D3D10StateBlockMaskEnableCapture**</span><span class="sxs-lookup"><span data-stu-id="d99e9-125">**D3D10StateBlockMaskEnableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenablecapture)   | <span data-ttu-id="d99e9-126">Habilitación de un intervalo de valores de estado en una máscara de bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="d99e9-126">Enable a range of state values in a state block mask.</span></span>               |
| [<span data-ttu-id="d99e9-127">**D3D10StateBlockMaskGetSetting**</span><span class="sxs-lookup"><span data-stu-id="d99e9-127">**D3D10StateBlockMaskGetSetting**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskgetsetting)         | <span data-ttu-id="d99e9-128">Obtiene un elemento en una máscara de bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="d99e9-128">Get an element in a state-block mask.</span></span>                               |
| [<span data-ttu-id="d99e9-129">**D3D10StateBlockMaskIntersect**</span><span class="sxs-lookup"><span data-stu-id="d99e9-129">**D3D10StateBlockMaskIntersect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskintersect)           | <span data-ttu-id="d99e9-130">Combine dos máscaras de bloques de estado con una operación and bit a bit.</span><span class="sxs-lookup"><span data-stu-id="d99e9-130">Combine two state-block masks with a bitwise AND.</span></span>                   |
| [<span data-ttu-id="d99e9-131">**D3D10StateBlockMaskUnion**</span><span class="sxs-lookup"><span data-stu-id="d99e9-131">**D3D10StateBlockMaskUnion**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskunion)                   | <span data-ttu-id="d99e9-132">Combine dos máscaras de bloques de estado con una operación OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="d99e9-132">Combine two state-block masks with a bitwise OR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="d99e9-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d99e9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d99e9-134">Referencia de efectos</span><span class="sxs-lookup"><span data-stu-id="d99e9-134">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



