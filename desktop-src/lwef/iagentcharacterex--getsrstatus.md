---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075536"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="08d26-103">IAgentCharacterEx::GetSRStatus</span><span class="sxs-lookup"><span data-stu-id="08d26-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="08d26-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="08d26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="08d26-105">Recupera el estado de la condición necesaria para admitir la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="08d26-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="08d26-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="08d26-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="08d26-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="08d26-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="08d26-108">Dirección de una variable que recibe uno de los siguientes valores para la configuración de estado:</span><span class="sxs-lookup"><span data-stu-id="08d26-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="08d26-109">Value</span><span class="sxs-lookup"><span data-stu-id="08d26-109">Value</span></span>                                                                               | <span data-ttu-id="08d26-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="08d26-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d26-111">**const unsigned Long** **Listen \_ status \_ CANLISTEN = 0;**</span><span class="sxs-lookup"><span data-stu-id="08d26-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="08d26-112">Las condiciones admiten la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="08d26-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="08d26-113">**const unsigned Long** **Listen \_ status \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="08d26-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="08d26-114">No hay ningún dispositivo de entrada de audio disponible en este sistema.</span><span class="sxs-lookup"><span data-stu-id="08d26-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="08d26-115">(Tenga en cuenta que esto no detecta si hay un micrófono instalado; solo puede detectar si el usuario tiene una tarjeta de sonido habilitada para la entrada instalada correctamente con un controlador de trabajo).</span><span class="sxs-lookup"><span data-stu-id="08d26-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="08d26-116">**const unsigned Long** **Listen \_ status \_ NOTTOPMOST = 2;**</span><span class="sxs-lookup"><span data-stu-id="08d26-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="08d26-117">Otro cliente es el cliente activo de este carácter o el carácter actual no es el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="08d26-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="08d26-118">**const unsigned Long** **Listen \_ status \_ CANTOPENAUDIO = 3;**</span><span class="sxs-lookup"><span data-stu-id="08d26-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="08d26-119">El canal de entrada o salida de audio está ocupado actualmente, otra aplicación está usando audio.</span><span class="sxs-lookup"><span data-stu-id="08d26-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="08d26-120">**const unsigned Long** **Listen \_ status \_ COULDNTINITIALIZESPEECH = 4;**</span><span class="sxs-lookup"><span data-stu-id="08d26-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="08d26-121">Se produjo un error no especificado en el proceso de inicialización del subsistema de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="08d26-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="08d26-122">Esto incluye la posibilidad de que no haya ningún motor de voz disponible que coincida con la configuración de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="08d26-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="08d26-123">**const unsigned Long** **Listen \_ status \_ SPEECHDISABLED = 5;**</span><span class="sxs-lookup"><span data-stu-id="08d26-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="08d26-124">El usuario ha deshabilitado la entrada de voz en la ventana Opciones de carácter avanzadas.</span><span class="sxs-lookup"><span data-stu-id="08d26-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="08d26-125">**const unsigned Long** **Listen \_ error status \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="08d26-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="08d26-126">Error al comprobar el estado de audio, pero el sistema no ha devuelto la causa del error.</span><span class="sxs-lookup"><span data-stu-id="08d26-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="08d26-127">Esta función permite consultar si las condiciones actuales admiten la entrada del reconocimiento de voz, incluido el estado del dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="08d26-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="08d26-128">Si su aplicación usa el método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) , puede usar esta función para asegurarse de que la llamada se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="08d26-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="08d26-129">La llamada a este método también carga el motor de voz si aún no está cargado.</span><span class="sxs-lookup"><span data-stu-id="08d26-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="08d26-130">Sin embargo, no activa el modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="08d26-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="08d26-131">Cuando se habilita la entrada de voz en la hoja de propiedades del agente (opciones de caracteres avanzadas), al consultar el estado se cargará el motor asociado (si aún no está cargado) e iniciará servicios de voz.</span><span class="sxs-lookup"><span data-stu-id="08d26-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="08d26-132">Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible.</span><span class="sxs-lookup"><span data-stu-id="08d26-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="08d26-133">(La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.</span><span class="sxs-lookup"><span data-stu-id="08d26-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="08d26-134">Esta función solo devuelve el valor del uso de la aplicación cliente del carácter; la configuración no refleja otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="08d26-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





