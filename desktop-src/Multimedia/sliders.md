---
title: Controles deslizantes (Windows multimedia)
description: Controles deslizantes
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- Mezcladores de audio, controles
- Mezcladores de audio, controles deslizantes
- mezcladores, controles
- mezcladores, controles deslizantes
- controles deslizantes
- Estructura de MIXERCONTROLDETAILS_SIGNED
- control de panorámica
- Control pan de QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421799"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="66c71-111">Controles deslizantes (Windows multimedia)</span><span class="sxs-lookup"><span data-stu-id="66c71-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="66c71-112">Los controles deslizantes suelen ser controles horizontales que se pueden ajustar a la izquierda o a la derecha.</span><span class="sxs-lookup"><span data-stu-id="66c71-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="66c71-113">Estos controles usan la [**estructura \_ firmada MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) para recuperar y establecer las propiedades del control.</span><span class="sxs-lookup"><span data-stu-id="66c71-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="66c71-114">En la tabla siguiente se describen los tipos de controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="66c71-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="66c71-115">Control</span><span class="sxs-lookup"><span data-stu-id="66c71-115">Control</span></span>    | <span data-ttu-id="66c71-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="66c71-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c71-117">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="66c71-117">Slider</span></span>     | <span data-ttu-id="66c71-118">Tiene un intervalo de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="66c71-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="66c71-119">El controlador del mezclador define los límites de este control.</span><span class="sxs-lookup"><span data-stu-id="66c71-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="66c71-120">Movimiento panorámico</span><span class="sxs-lookup"><span data-stu-id="66c71-120">Pan</span></span>        | <span data-ttu-id="66c71-121">Tiene un intervalo de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="66c71-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="66c71-122">El controlador de mezclador define los límites de este control, con 0 como valor de intervalo intermedio.</span><span class="sxs-lookup"><span data-stu-id="66c71-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="66c71-123">QSound pan</span><span class="sxs-lookup"><span data-stu-id="66c71-123">QSound Pan</span></span> | <span data-ttu-id="66c71-124">Proporciona un control de sonido expandido a través de QSound.</span><span class="sxs-lookup"><span data-stu-id="66c71-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="66c71-125">Este control tiene un intervalo de – 15 a 15.</span><span class="sxs-lookup"><span data-stu-id="66c71-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 
