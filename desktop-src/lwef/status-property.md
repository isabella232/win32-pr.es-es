---
title: Propiedad status
description: Propiedad status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704695"
---
# <a name="status-property"></a><span data-ttu-id="db786-103">Propiedad status</span><span class="sxs-lookup"><span data-stu-id="db786-103">Status Property</span></span>

<span data-ttu-id="db786-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db786-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="db786-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="db786-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="db786-106">Devuelve el estado del canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="db786-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="db786-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="db786-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="db786-108">*agente \* \* *. Estado de AudioOutput.**</span><span class="sxs-lookup"><span data-stu-id="db786-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="db786-109">Value</span><span class="sxs-lookup"><span data-stu-id="db786-109">Value</span></span> | <span data-ttu-id="db786-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="db786-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db786-111">0</span><span class="sxs-lookup"><span data-stu-id="db786-111">0</span></span>     | <span data-ttu-id="db786-112">El canal de salida de audio está disponible (no está ocupado).</span><span class="sxs-lookup"><span data-stu-id="db786-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="db786-113">1</span><span class="sxs-lookup"><span data-stu-id="db786-113">1</span></span>     | <span data-ttu-id="db786-114">No se admite la salida de audio; por ejemplo, dado que no hay ninguna tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="db786-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="db786-115">2</span><span class="sxs-lookup"><span data-stu-id="db786-115">2</span></span>     | <span data-ttu-id="db786-116">No se puede abrir el canal de salida de audio (está ocupado). por ejemplo, como otra aplicación está reproduciendo audio.</span><span class="sxs-lookup"><span data-stu-id="db786-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="db786-117">3</span><span class="sxs-lookup"><span data-stu-id="db786-117">3</span></span>     | <span data-ttu-id="db786-118">El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz de usuario.</span><span class="sxs-lookup"><span data-stu-id="db786-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="db786-119">4</span><span class="sxs-lookup"><span data-stu-id="db786-119">4</span></span>     | <span data-ttu-id="db786-120">El canal de salida de audio está ocupado porque un carácter está hablando actualmente.</span><span class="sxs-lookup"><span data-stu-id="db786-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="db786-121">5</span><span class="sxs-lookup"><span data-stu-id="db786-121">5</span></span>     | <span data-ttu-id="db786-122">El canal de salida de audio no está ocupado, pero está esperando la entrada de voz de usuario.</span><span class="sxs-lookup"><span data-stu-id="db786-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="db786-123">6</span><span class="sxs-lookup"><span data-stu-id="db786-123">6</span></span>     | <span data-ttu-id="db786-124">Hubo otro problema (desconocido) al intentar acceder al canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="db786-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db786-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db786-125">Remarks</span></span>

<span data-ttu-id="db786-126">Esta configuración permite a la aplicación cliente consultar el canal de salida de audio y devolver un valor entero que indica el estado del canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="db786-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="db786-127">Puede utilizar esta opción para determinar si es adecuado que el carácter hable o si es adecuado intentar activar el modo de escucha (mediante el método de [**escucha**](listen-method.md) ).</span><span class="sxs-lookup"><span data-stu-id="db786-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="db786-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="db786-128">See Also</span></span>

[<span data-ttu-id="db786-129">**Evento ListenComplete**</span><span class="sxs-lookup"><span data-stu-id="db786-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




