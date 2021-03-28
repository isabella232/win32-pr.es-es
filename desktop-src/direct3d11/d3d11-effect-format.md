---
title: Formato de efecto (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Más información sobre: formato de efectos (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274940"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="8ab16-103">Formato de efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="8ab16-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="8ab16-104">Un efecto (que suele almacenarse en un archivo con una extensión de archivo. FX) declara el estado de la canalización establecido por un efecto.</span><span class="sxs-lookup"><span data-stu-id="8ab16-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="8ab16-105">El estado del efecto puede dividirse aproximadamente en tres categorías:</span><span class="sxs-lookup"><span data-stu-id="8ab16-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="8ab16-106">[Variables](d3d11-effect-variable-syntax.md), que se declaran normalmente en la parte superior de un efecto.</span><span class="sxs-lookup"><span data-stu-id="8ab16-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="8ab16-107">[Funciones](d3d11-effect-function-syntax.md), que implementan código de sombreador o que otras funciones usan como funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="8ab16-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="8ab16-108">Las [técnicas](d3d11-effect-technique-syntax.md), que se pueden organizar en grupos de efectos, e implementan secuencias de representación mediante una o varias fases de efecto.</span><span class="sxs-lookup"><span data-stu-id="8ab16-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="8ab16-109">Cada paso establece uno o más [grupos de Estados](d3d11-effect-states.md) y llama a las funciones de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8ab16-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![diagrama de las categorías de declaraciones de efectos, incluidas las variables en la parte superior, las funciones del centro y las técnicas de la parte inferior.](images/d3d10-effect-intro.png)

<span data-ttu-id="8ab16-111">En el diagrama anterior se muestran las categorías de estado de efecto.</span><span class="sxs-lookup"><span data-stu-id="8ab16-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="8ab16-112">La definición del formato binario de efectos se puede encontrar en el archivo binario \\ EffectBinaryFormat. h en el código fuente de los efectos.</span><span class="sxs-lookup"><span data-stu-id="8ab16-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="8ab16-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8ab16-113">In this section</span></span>



| <span data-ttu-id="8ab16-114">Tema</span><span class="sxs-lookup"><span data-stu-id="8ab16-114">Topic</span></span>                                                                   | <span data-ttu-id="8ab16-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ab16-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ab16-116">Sintaxis de variables de efectos</span><span class="sxs-lookup"><span data-stu-id="8ab16-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="8ab16-117">Una variable de efecto se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8ab16-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="8ab16-118">Sintaxis de anotación</span><span class="sxs-lookup"><span data-stu-id="8ab16-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="8ab16-119">Una anotación es una parte de la información definida por el usuario, declarada con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8ab16-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="8ab16-120">Sintaxis de la función Effect</span><span class="sxs-lookup"><span data-stu-id="8ab16-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="8ab16-121">Una función Effect se escribe en HLSL y se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8ab16-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="8ab16-122">Sintaxis de la técnica de efectos</span><span class="sxs-lookup"><span data-stu-id="8ab16-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="8ab16-123">Una técnica de efecto se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8ab16-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="8ab16-124">Grupos de Estados de efecto</span><span class="sxs-lookup"><span data-stu-id="8ab16-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="8ab16-125">Los Estados de efecto son pares de nombre y valor en forma de expresión.</span><span class="sxs-lookup"><span data-stu-id="8ab16-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="8ab16-126">Sintaxis de grupo de efectos</span><span class="sxs-lookup"><span data-stu-id="8ab16-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="8ab16-127">Un grupo de efectos se declara con la sintaxis descrita en esta sección.</span><span class="sxs-lookup"><span data-stu-id="8ab16-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="8ab16-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ab16-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab16-129">Referencia de Effects 11</span><span class="sxs-lookup"><span data-stu-id="8ab16-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





