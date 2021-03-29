---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418865"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="79273-103">IAgentAudioOutputPropertiesEx:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="79273-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="79273-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="79273-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="79273-105">Recupera el estado del canal de audio.</span><span class="sxs-lookup"><span data-stu-id="79273-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="79273-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="79273-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="79273-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="79273-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="79273-108">Estado del canal de salida de audio, que puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="79273-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="79273-109">Value</span><span class="sxs-lookup"><span data-stu-id="79273-109">Value</span></span>                                                                         | <span data-ttu-id="79273-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="79273-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79273-111">**const unsigned short** **audio \_ status \_ disponible = 0;**</span><span class="sxs-lookup"><span data-stu-id="79273-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="79273-112">El canal de salida de audio está disponible (no está ocupado).</span><span class="sxs-lookup"><span data-stu-id="79273-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="79273-113">**const unsigned short** **audio \_ status \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="79273-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="79273-114">No se admite la salida de audio; por ejemplo, dado que no hay ninguna tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="79273-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="79273-115">**const unsigned short** **audio \_ status \_ CANTOPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="79273-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="79273-116">No se puede abrir el canal de salida de audio (está ocupado). por ejemplo, debido a que otra aplicación está reproduciendo audio.</span><span class="sxs-lookup"><span data-stu-id="79273-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="79273-117">**const unsigned short** **audio \_ status \_ USERSPEAKING = 3;**</span><span class="sxs-lookup"><span data-stu-id="79273-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="79273-118">El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz del usuario</span><span class="sxs-lookup"><span data-stu-id="79273-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="79273-119">**const unsigned short** **audio \_ status \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="79273-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="79273-120">El canal de salida de audio está ocupado porque un carácter está hablando actualmente.</span><span class="sxs-lookup"><span data-stu-id="79273-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="79273-121">**const unsigned short** **audio \_ status \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="79273-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="79273-122">El canal de salida de audio no está ocupado, pero está esperando la entrada de voz de usuario.</span><span class="sxs-lookup"><span data-stu-id="79273-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="79273-123">**const unsigned short** **audio \_ status \_ error = 6;**</span><span class="sxs-lookup"><span data-stu-id="79273-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="79273-124">Hubo otro problema (desconocido) al intentar acceder al canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="79273-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="79273-125">Esta configuración permite que la aplicación cliente consulte el estado del canal de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="79273-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="79273-126">Puede usar esta opción para determinar si el carácter debe hablar o intentar activar el modo de escucha (mediante [**IAgentCharacterEx:: Listen**](lwef.iagentcharacterex::listen_method)).</span><span class="sxs-lookup"><span data-stu-id="79273-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using [**IAgentCharacterEx::Listen**](lwef.iagentcharacterex::listen_method)).</span></span>

 

 





