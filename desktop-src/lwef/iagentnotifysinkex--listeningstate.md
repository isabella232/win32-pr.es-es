---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532212"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="8c14b-103">IAgentNotifySinkEx::ListeningState</span><span class="sxs-lookup"><span data-stu-id="8c14b-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="8c14b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c14b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="8c14b-105">Notifica a una aplicación cliente cuando cambia el modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="8c14b-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="8c14b-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8c14b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="8c14b-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span><span class="sxs-lookup"><span data-stu-id="8c14b-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="8c14b-108">Carácter para el que ha cambiado el estado de escucha.</span><span class="sxs-lookup"><span data-stu-id="8c14b-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="8c14b-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span><span class="sxs-lookup"><span data-stu-id="8c14b-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="8c14b-110">Estado del modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="8c14b-110">The Listening mode state.</span></span> <span data-ttu-id="8c14b-111">**True** indica que se ha iniciado el modo de escucha; **False**, el modo de escucha ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="8c14b-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="8c14b-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="8c14b-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="8c14b-113">La causa del evento, que puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c14b-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="8c14b-114">Value</span><span class="sxs-lookup"><span data-stu-id="8c14b-114">Value</span></span>                                                                             | <span data-ttu-id="8c14b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c14b-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8c14b-116">**const unsigned Long** **LSCOMPLETE \_ causa \_ PROGRAMDISABLED = 1;**</span><span class="sxs-lookup"><span data-stu-id="8c14b-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="8c14b-117">El modo de escucha estaba desactivado por el código del programa.</span><span class="sxs-lookup"><span data-stu-id="8c14b-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="8c14b-118">**const unsigned Long** **LSCOMPLETE \_ causa \_ PROGRAMTIMEDOUT = 2;**</span><span class="sxs-lookup"><span data-stu-id="8c14b-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="8c14b-119">Se agotó el tiempo de espera para el modo de escucha (activado por el código del programa).</span><span class="sxs-lookup"><span data-stu-id="8c14b-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="8c14b-120">**const unsigned Long** **LSCOMPLETE \_ causa \_ USERTIMEDOUT = 3;**</span><span class="sxs-lookup"><span data-stu-id="8c14b-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="8c14b-121">Se agotó el tiempo de espera para el modo de escucha (activado por la clave de escucha).</span><span class="sxs-lookup"><span data-stu-id="8c14b-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="8c14b-122">**const unsigned Long** **LSCOMPLETE \_ causa \_ USERRELEASEDKEY = 4;**</span><span class="sxs-lookup"><span data-stu-id="8c14b-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="8c14b-123">El modo de escucha estaba desactivado porque el usuario liberó la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="8c14b-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="8c14b-124">**const unsigned Long** **LSCOMPLETE \_ causa \_ USERUTTERANCEENDED = 5;**</span><span class="sxs-lookup"><span data-stu-id="8c14b-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="8c14b-125">El modo de escucha estaba desactivado porque el usuario terminó de hablar.</span><span class="sxs-lookup"><span data-stu-id="8c14b-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="8c14b-126">**const unsigned Long** **LSCOMPLETE \_ causa \_ CLIENTDEACTIVATED = 6;**</span><span class="sxs-lookup"><span data-stu-id="8c14b-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="8c14b-127">El modo de escucha estaba desactivado porque se desactivó el cliente activo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c14b-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="8c14b-128">**const unsigned Long** **LSCOMPLETE \_ causa \_ DEFAULTCHARCHANGE = 7**</span><span class="sxs-lookup"><span data-stu-id="8c14b-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="8c14b-129">El modo de escucha estaba desactivado porque se cambió el carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8c14b-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="8c14b-130">**const unsigned Long** **LSCOMPLETE \_ causa \_ USERDISABLED = 8**</span><span class="sxs-lookup"><span data-stu-id="8c14b-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="8c14b-131">El modo de escucha estaba desactivado porque el usuario deshabilitó la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="8c14b-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="8c14b-132">Este evento se envía a todos los clientes cuando el modo de escucha comienza después de que el usuario presione la tecla de escucha o cuando finalice el tiempo de espera, o cuando el cliente de entrada-activo llame al método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) con **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="8c14b-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="8c14b-133">El evento devuelve valores a los clientes que actualmente tienen este carácter cargado.</span><span class="sxs-lookup"><span data-stu-id="8c14b-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="8c14b-134">El resto de clientes reciben un carácter nulo (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="8c14b-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c14b-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c14b-135">See Also</span></span>

[<span data-ttu-id="8c14b-136">**IAgentCharacterEx:: Listen**</span><span class="sxs-lookup"><span data-stu-id="8c14b-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 





