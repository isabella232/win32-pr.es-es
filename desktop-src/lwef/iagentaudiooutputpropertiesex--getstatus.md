---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380749"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="8768f-103">IAgentAudioOutputPropertiesEx::GetStatus</span><span class="sxs-lookup"><span data-stu-id="8768f-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="8768f-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8768f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="8768f-105">Recupera el estado del canal de audio.</span><span class="sxs-lookup"><span data-stu-id="8768f-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="8768f-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8768f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8768f-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="8768f-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="8768f-108">Estado del canal de salida de audio, que puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8768f-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="8768f-109">Value</span><span class="sxs-lookup"><span data-stu-id="8768f-109">Value</span></span>                                                                         | <span data-ttu-id="8768f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8768f-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8768f-111">**const unsigned short** **AUDIO STATUS AVAILABLE = \_ \_ 0;**</span><span class="sxs-lookup"><span data-stu-id="8768f-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="8768f-112">El canal de salida de audio está disponible (no está ocupado).</span><span class="sxs-lookup"><span data-stu-id="8768f-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="8768f-113">**const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**</span><span class="sxs-lookup"><span data-stu-id="8768f-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="8768f-114">No hay compatibilidad con la salida de audio; por ejemplo, porque no hay ninguna tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="8768f-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="8768f-115">**const unsigned short** **AUDIO STATUS \_ \_ DIMPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="8768f-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="8768f-116">No se puede abrir el canal de salida de audio (está ocupado); por ejemplo, porque otra aplicación reproduce audio.</span><span class="sxs-lookup"><span data-stu-id="8768f-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="8768f-117">**const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**</span><span class="sxs-lookup"><span data-stu-id="8768f-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="8768f-118">El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz del usuario.</span><span class="sxs-lookup"><span data-stu-id="8768f-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="8768f-119">**const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="8768f-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="8768f-120">El canal de salida de audio está ocupado porque un carácter está hablando actualmente.</span><span class="sxs-lookup"><span data-stu-id="8768f-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="8768f-121">**const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="8768f-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="8768f-122">El canal de salida de audio no está ocupado, pero está esperando la entrada de voz del usuario.</span><span class="sxs-lookup"><span data-stu-id="8768f-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="8768f-123">**const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**</span><span class="sxs-lookup"><span data-stu-id="8768f-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="8768f-124">Hubo algún otro problema (desconocido) al intentar acceder al canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="8768f-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="8768f-125">Esta configuración permite a la aplicación cliente consultar el estado del canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="8768f-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="8768f-126">Puede usarlo para determinar si el carácter habla o si intenta activar el modo de escucha (mediante **IAgentCharacterEx::Listen).**</span><span class="sxs-lookup"><span data-stu-id="8768f-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using **IAgentCharacterEx::Listen**).</span></span>

 

 





