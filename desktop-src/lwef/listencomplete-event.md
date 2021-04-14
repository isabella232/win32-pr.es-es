---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419060"
---
# <a name="listencomplete-event"></a><span data-ttu-id="04eda-103">Evento ListenComplete</span><span class="sxs-lookup"><span data-stu-id="04eda-103">ListenComplete Event</span></span>

<span data-ttu-id="04eda-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04eda-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="04eda-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="04eda-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="04eda-106">Tiene lugar cuando el modo de escucha (reconocimiento de voz) ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="04eda-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="04eda-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="04eda-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="04eda-108">**Sub** *Agent. \* \* \* ListenComplete (ByVal* \*  *CharacterID*, **ByVal** *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="04eda-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="04eda-109">Parte</span><span class="sxs-lookup"><span data-stu-id="04eda-109">Part</span></span>          | <span data-ttu-id="04eda-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="04eda-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04eda-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="04eda-111">*CharacterID*</span></span> | <span data-ttu-id="04eda-112">Devuelve el identificador del carácter de escucha como una cadena.</span><span class="sxs-lookup"><span data-stu-id="04eda-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="04eda-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="04eda-113">*Cause*</span></span>       | <span data-ttu-id="04eda-114">Devuelve la causa del evento completo como un entero que puede ser uno de los siguientes: 1 modo de escucha desactivado por el código del programa.</span><span class="sxs-lookup"><span data-stu-id="04eda-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="04eda-115">2 el modo de escucha (activado por el código del programa) agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="04eda-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="04eda-116">3 el modo de escucha (activado por la clave de escucha) agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="04eda-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="04eda-117">4 el modo de escucha estaba desactivado porque el usuario liberó la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="04eda-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="04eda-118">5 modo de escucha finalizado porque el usuario terminó de hablar.</span><span class="sxs-lookup"><span data-stu-id="04eda-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="04eda-119">6 modo de escucha finalizado porque el cliente de entrada-activo se desactivó.</span><span class="sxs-lookup"><span data-stu-id="04eda-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="04eda-120">7 el modo de escucha finalizó porque se cambió el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="04eda-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="04eda-121">8 el modo de escucha ha finalizado porque el usuario ha deshabilitado la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="04eda-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="04eda-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04eda-122">Remarks</span></span>

<span data-ttu-id="04eda-123">Este evento se envía a todos los clientes cuando finaliza el tiempo de espera del modo de escucha, una vez que el usuario libera la clave de escucha, cuando el cliente activo de entrada llama al método [**Listen**](listen-method.md) con **false** o el usuario ha terminado de hablar.</span><span class="sxs-lookup"><span data-stu-id="04eda-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="04eda-124">Puede usar este evento para determinar cuándo se debe reanudar la salida de caracteres hablados (audio).</span><span class="sxs-lookup"><span data-stu-id="04eda-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="04eda-125">Si activa el modo de escucha mediante el método de [**escucha**](listen-method.md) y, a continuación, el usuario presiona la tecla de escucha, el modo de escucha se restablece y continúa hasta que se completa el tiempo de espera de la clave de escucha, se libera la clave de escucha o el usuario termina de hablar, lo que sea posterior.</span><span class="sxs-lookup"><span data-stu-id="04eda-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="04eda-126">En esta situación, no recibirá un evento **ListenComplete** hasta que se complete el modo de la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="04eda-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="04eda-127">El evento devuelve el carácter a los clientes que actualmente tienen este carácter cargado.</span><span class="sxs-lookup"><span data-stu-id="04eda-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="04eda-128">El resto de clientes reciben un carácter nulo (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="04eda-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="04eda-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04eda-129">See Also</span></span>

<span data-ttu-id="04eda-130">[**Evento ListenStart**](listenstart-event.md), [ **método Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="04eda-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





