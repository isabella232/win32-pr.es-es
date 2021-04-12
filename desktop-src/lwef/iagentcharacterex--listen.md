---
title: IAgentCharacterEx escucha
description: IAgentCharacterEx escucha
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357277"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="84e2b-103">IAgentCharacterEx:: Listen</span><span class="sxs-lookup"><span data-stu-id="84e2b-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="84e2b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="84e2b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="84e2b-105">Activa o desactiva el modo de escucha (entrada de reconocimiento de voz).</span><span class="sxs-lookup"><span data-stu-id="84e2b-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="84e2b-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="84e2b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="84e2b-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span><span class="sxs-lookup"><span data-stu-id="84e2b-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="84e2b-108">Marca de modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="84e2b-108">Listening mode flag.</span></span> <span data-ttu-id="84e2b-109">Si este parámetro es **true**, el modo de escucha está activado; Si es **false**, el modo de escucha está desactivado.</span><span class="sxs-lookup"><span data-stu-id="84e2b-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="84e2b-110">Al establecer este método en **true** , se habilita el modo de escucha (activa el reconocimiento de voz) durante un período de tiempo fijo.</span><span class="sxs-lookup"><span data-stu-id="84e2b-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="84e2b-111">Aunque no se puede establecer el valor del tiempo de espera, puede desactivar el modo de escucha antes de que expire el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="84e2b-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="84e2b-112">Además, si el modo de escucha ya está activado porque usted (u otro cliente) estableció correctamente el método en **true** antes de que expire el tiempo de espera, el método se ejecuta correctamente y restablece el tiempo de espera. Sin embargo, si el modo de escucha ya está activado porque el usuario está presionando la clave de escucha, el método se ejecuta correctamente, pero el tiempo de espera se omite y el modo de escucha finaliza en función de la interacción del usuario con la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="84e2b-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="84e2b-113">Este método se realizará correctamente solo cuando lo llame el cliente de entrada y de actividad.</span><span class="sxs-lookup"><span data-stu-id="84e2b-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="84e2b-114">Por lo tanto, se producirá un error en el método si el cliente no es el cliente activo del carácter más alto.</span><span class="sxs-lookup"><span data-stu-id="84e2b-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="84e2b-115">También se producirá un error en el método si intenta establecer el método en **false** y el usuario está presionando la clave de escucha.</span><span class="sxs-lookup"><span data-stu-id="84e2b-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="84e2b-116">También puede producir un error si no hay ningún motor de voz compatible disponible que coincida con el valor de ID. de idioma del carácter o el usuario ha deshabilitado la entrada de voz mediante la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="84e2b-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="84e2b-117">Sin embargo, el método no generará un error si el dispositivo de audio está ocupado.</span><span class="sxs-lookup"><span data-stu-id="84e2b-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="84e2b-118">Cuando se establece correctamente este método en **true**, el servidor desencadena el evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) .</span><span class="sxs-lookup"><span data-stu-id="84e2b-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="84e2b-119">El servidor también envía **IAgentNotifySinkEx:: ListeningState** cuando se completa el tiempo de espera del modo de escucha o cuando se establece [**IAgentCharacterEx:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) en **false**.</span><span class="sxs-lookup"><span data-stu-id="84e2b-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="84e2b-120">Este método no llama automáticamente a [**IAgentCharacter:: stopAll**](iagentcharacter--stopall.md) y reproduce una animación de estado de escucha del carácter como ocurre cuando el usuario presiona la tecla de escucha.</span><span class="sxs-lookup"><span data-stu-id="84e2b-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="84e2b-121">Esto le permite usar el evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) para determinar si desea detener la animación actual y reproducir su propia animación adecuada.</span><span class="sxs-lookup"><span data-stu-id="84e2b-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="84e2b-122">Sin embargo, una vez que se detecta un utterance de usuario, el servidor llama automáticamente a **IAgentCharacter:: stopAll** y reproduce una animación del estado de la audición.</span><span class="sxs-lookup"><span data-stu-id="84e2b-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="84e2b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84e2b-123">See Also</span></span>

<span data-ttu-id="84e2b-124">[**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="84e2b-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




