---
description: Un efecto (que suele almacenarse en un archivo con una extensión de archivo. FX) declara el estado de la canalización establecido por un efecto.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato de efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423488"
---
# <a name="effect-format-direct3d-10"></a><span data-ttu-id="aeed5-103">Formato de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aeed5-103">Effect Format (Direct3D 10)</span></span>

<span data-ttu-id="aeed5-104">Un efecto (que suele almacenarse en un archivo con una extensión de archivo. FX) declara el estado de la canalización establecido por un efecto.</span><span class="sxs-lookup"><span data-stu-id="aeed5-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="aeed5-105">El estado del efecto puede dividirse aproximadamente en tres categorías:</span><span class="sxs-lookup"><span data-stu-id="aeed5-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="aeed5-106">[Variables](d3d10-effect-variable-syntax.md), que se declaran normalmente en la parte superior de un efecto.</span><span class="sxs-lookup"><span data-stu-id="aeed5-106">[Variables](d3d10-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="aeed5-107">[Funciones](d3d10-effect-function-syntax.md), que implementan código de sombreador o que otras funciones usan como funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="aeed5-107">[Functions](d3d10-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="aeed5-108">[Técnica](d3d10-effect-technique-syntax.md), que implementa secuencias de representación utilizando uno o más efectos.</span><span class="sxs-lookup"><span data-stu-id="aeed5-108">[A technique](d3d10-effect-technique-syntax.md), which implements rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="aeed5-109">Cada paso establece uno o más [grupos de Estados](d3d10-effect-states.md) y llama a las funciones de sombreador.</span><span class="sxs-lookup"><span data-stu-id="aeed5-109">Each pass sets one or more [state groups](d3d10-effect-states.md) and calls shader functions.</span></span>

![diagrama de las categorías de estado de efecto](images/d3d10-effect-intro.png)

<span data-ttu-id="aeed5-111">En el diagrama anterior se muestran las categorías de estado de efecto.</span><span class="sxs-lookup"><span data-stu-id="aeed5-111">The preceding diagram shows the categories of effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeed5-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aeed5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeed5-113">Referencia de efectos</span><span class="sxs-lookup"><span data-stu-id="aeed5-113">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



