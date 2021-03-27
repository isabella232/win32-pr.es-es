---
title: 'fase: PS'
description: La instrucción de fase marca la transición entre la fase 1 y la fase 2. Si no hay ninguna instrucción de fase, todo el sombreador se ejecuta como si se tratase de un sombreador de fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077121"
---
# <a name="phase---ps"></a><span data-ttu-id="d28a5-104">fase: PS</span><span class="sxs-lookup"><span data-stu-id="d28a5-104">phase - ps</span></span>

<span data-ttu-id="d28a5-105">La instrucción de fase marca la transición entre la fase 1 y la fase 2.</span><span class="sxs-lookup"><span data-stu-id="d28a5-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="d28a5-106">Si no hay ninguna instrucción de fase, todo el sombreador se ejecuta como si se tratase de un sombreador de fase 2.</span><span class="sxs-lookup"><span data-stu-id="d28a5-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="d28a5-107">Esta instrucción solo se aplica a la versión \_ 4.</span><span class="sxs-lookup"><span data-stu-id="d28a5-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d28a5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d28a5-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="d28a5-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d28a5-109">Remarks</span></span>



| <span data-ttu-id="d28a5-110">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d28a5-110">Pixel shader versions</span></span> | <span data-ttu-id="d28a5-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="d28a5-111">1\_1</span></span> | <span data-ttu-id="d28a5-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="d28a5-112">1\_2</span></span> | <span data-ttu-id="d28a5-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d28a5-113">1\_3</span></span> | <span data-ttu-id="d28a5-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="d28a5-114">1\_4</span></span> | <span data-ttu-id="d28a5-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d28a5-115">2\_0</span></span> | <span data-ttu-id="d28a5-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d28a5-116">2\_x</span></span> | <span data-ttu-id="d28a5-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d28a5-117">2\_sw</span></span> | <span data-ttu-id="d28a5-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d28a5-118">3\_0</span></span> | <span data-ttu-id="d28a5-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d28a5-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d28a5-120">phase</span><span class="sxs-lookup"><span data-stu-id="d28a5-120">phase</span></span>                 |      |      |      | <span data-ttu-id="d28a5-121">x</span><span class="sxs-lookup"><span data-stu-id="d28a5-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="d28a5-122">Las instrucciones del sombreador que se producen antes de la instrucción de la fase son instrucciones de la fase 1.</span><span class="sxs-lookup"><span data-stu-id="d28a5-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="d28a5-123">Todas las demás instrucciones son instrucciones de la fase 2.</span><span class="sxs-lookup"><span data-stu-id="d28a5-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="d28a5-124">Si hay dos fases para las instrucciones, se aumenta el número máximo de instrucciones por sombreador.</span><span class="sxs-lookup"><span data-stu-id="d28a5-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="d28a5-125">El efecto secundario desafortunado de la transición de fase es que el componente alfa de los [registros temporales](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) no se mantiene en la transición.</span><span class="sxs-lookup"><span data-stu-id="d28a5-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="d28a5-126">En otras palabras, el componente alfa se debe reinicializar después de la instrucción de fase.</span><span class="sxs-lookup"><span data-stu-id="d28a5-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="d28a5-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d28a5-127">Example</span></span>

<span data-ttu-id="d28a5-128">En este ejemplo se muestra cómo agrupar instrucciones como instrucciones de fase 1 o fase 2 en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="d28a5-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="d28a5-129">La instrucción de fase también se denomina normalmente el marcador de fase porque marca la transición entre las instrucciones de las fases 1 y 2.</span><span class="sxs-lookup"><span data-stu-id="d28a5-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="d28a5-130">En un \_ sombreador de 4 píxeles de la versión 1, si el marcador de fase no está presente, el sombreador se ejecuta como si se estuviera ejecutando en la fase 2.</span><span class="sxs-lookup"><span data-stu-id="d28a5-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="d28a5-131">Esto es importante porque existen diferencias entre las instrucciones de las fases 1 y 2 y se registra la disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="d28a5-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="d28a5-132">Las diferencias se indican en la sección de referencia.</span><span class="sxs-lookup"><span data-stu-id="d28a5-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="d28a5-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d28a5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d28a5-134">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d28a5-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




