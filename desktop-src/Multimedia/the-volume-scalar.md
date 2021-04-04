---
title: El volumen escalar
description: El volumen escalar
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Interfaz digital de instrumentos musicales (MIDI), volumen escalar
- MIDI (interfaz digital de instrumentos musicales), escalar volumen
- Asignador de MIDI, escalar de volumen
- escalar del volumen
- Asignador de MIDI, ajustar los niveles de salida
- ajustar los niveles de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076381"
---
# <a name="the-volume-scalar"></a><span data-ttu-id="707d2-109">El volumen escalar</span><span class="sxs-lookup"><span data-stu-id="707d2-109">The Volume Scalar</span></span>

<span data-ttu-id="707d2-110">El propósito del volumen escalar es permitir ajustes entre los niveles de salida relativos de distintas revisiones en un sintetizador.</span><span class="sxs-lookup"><span data-stu-id="707d2-110">The purpose of the volume scalar is to allow adjustments between the relative output levels of different patches on a synthesizer.</span></span> <span data-ttu-id="707d2-111">Por ejemplo, si la revisión de graves de un sintetizador es demasiado alta en comparación con su revisión de piano, puede cambiar el mapa de configuración para reducir el volumen de graves o el volumen de piano hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="707d2-111">For example, if the bass patch on a synthesizer is too loud compared with its piano patch, you can change the setup map to scale the bass volume down or the piano volume up.</span></span>

<span data-ttu-id="707d2-112">El volumen escalar especifica un valor de porcentaje para cambiar todos los mensajes de controlador principal de volumen MIDI que siguen un mensaje de cambio de programa asociado.</span><span class="sxs-lookup"><span data-stu-id="707d2-112">The volume scalar specifies a percentage value for changing all MIDI main-volume controller messages that follow an associated program-change message.</span></span> <span data-ttu-id="707d2-113">Por ejemplo, si el valor escalar del volumen es del 50%, el asignador MIDI modifica los mensajes del controlador principal del volumen MIDI, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="707d2-113">For example, if the volume scalar value is 50%, the MIDI Mapper modifies MIDI main-volume controller messages as shown in the following illustration.</span></span>

![imagen del asignador MIDI](images/mmap-a04.gif)

 

 




