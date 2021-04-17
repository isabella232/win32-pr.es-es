---
description: Las técnicas proporcionan el músculo de representación. Una técnica encapsula el estado del efecto que determina un estilo de representación. Una técnica se compone de una o varias fases.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Técnicas y pasos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686422"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="645c9-105">Técnicas y pasos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="645c9-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="645c9-106">Las técnicas proporcionan el músculo de representación.</span><span class="sxs-lookup"><span data-stu-id="645c9-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="645c9-107">Una técnica encapsula el estado del efecto que determina un estilo de representación.</span><span class="sxs-lookup"><span data-stu-id="645c9-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="645c9-108">Una técnica se compone de una o varias fases.</span><span class="sxs-lookup"><span data-stu-id="645c9-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="645c9-109">Descrita</span><span class="sxs-lookup"><span data-stu-id="645c9-109">Techniques</span></span>

<span data-ttu-id="645c9-110">La sintaxis para llamar a una técnica es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="645c9-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="645c9-111">Donde:</span><span class="sxs-lookup"><span data-stu-id="645c9-111">Where:</span></span>

-   <span data-ttu-id="645c9-112">ID es un nombre único opcional.</span><span class="sxs-lookup"><span data-stu-id="645c9-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="645c9-113">la anotación es cero o más partes opcionales de la información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="645c9-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="645c9-114">Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="645c9-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="645c9-115">Pass (es) es cero o más pasos.</span><span class="sxs-lookup"><span data-stu-id="645c9-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="645c9-116">Cada paso contiene asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="645c9-116">Each pass contains state assignments.</span></span> <span data-ttu-id="645c9-117">Vea a continuación.</span><span class="sxs-lookup"><span data-stu-id="645c9-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="645c9-118">Paso</span><span class="sxs-lookup"><span data-stu-id="645c9-118">Passes</span></span>

<span data-ttu-id="645c9-119">Un paso contiene las asignaciones de estado necesarias para representarlas.</span><span class="sxs-lookup"><span data-stu-id="645c9-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="645c9-120">Donde:</span><span class="sxs-lookup"><span data-stu-id="645c9-120">Where:</span></span>

-   <span data-ttu-id="645c9-121">ID es un nombre único opcional.</span><span class="sxs-lookup"><span data-stu-id="645c9-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="645c9-122">la anotación es una parte opcional de la información específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="645c9-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="645c9-123">Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="645c9-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="645c9-124">asignación (s) asigna cero o más valores de estado o evalúa una o varias expresiones.</span><span class="sxs-lookup"><span data-stu-id="645c9-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="645c9-125">Vea [Estados de efectos (Direct3D 9)](effect-states.md) y [expresiones (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="645c9-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="645c9-126">Pasa por alto todas las asignaciones menos la última en un conjunto de asignaciones repetidas al mismo estado.</span><span class="sxs-lookup"><span data-stu-id="645c9-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="645c9-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="645c9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="645c9-128">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="645c9-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



