---
title: Propiedad SRStatus
description: Propiedad SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076390"
---
# <a name="srstatus-property"></a><span data-ttu-id="1d973-103">Propiedad SRStatus</span><span class="sxs-lookup"><span data-stu-id="1d973-103">SRStatus Property</span></span>

<span data-ttu-id="1d973-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d973-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1d973-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="1d973-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1d973-106">Devuelve si se puede iniciar la entrada de voz para el carácter.</span><span class="sxs-lookup"><span data-stu-id="1d973-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="1d973-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="1d973-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1d973-108">*directivas. ***Caracteres ("*** CharacterID \* *"). SRStatus**</span><span class="sxs-lookup"><span data-stu-id="1d973-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="1d973-109">Value</span><span class="sxs-lookup"><span data-stu-id="1d973-109">Value</span></span> | <span data-ttu-id="1d973-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d973-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d973-111">0</span><span class="sxs-lookup"><span data-stu-id="1d973-111">0</span></span>     | <span data-ttu-id="1d973-112">Las condiciones admiten la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="1d973-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="1d973-113">1</span><span class="sxs-lookup"><span data-stu-id="1d973-113">1</span></span>     | <span data-ttu-id="1d973-114">No hay ningún dispositivo de entrada de audio disponible en este sistema.</span><span class="sxs-lookup"><span data-stu-id="1d973-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="1d973-115">(Tenga en cuenta que esto no detecta si hay un micrófono instalado; solo puede detectar si el usuario tiene una tarjeta de sonido habilitada para la entrada instalada correctamente con un controlador de trabajo).</span><span class="sxs-lookup"><span data-stu-id="1d973-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="1d973-116">2</span><span class="sxs-lookup"><span data-stu-id="1d973-116">2</span></span>     | <span data-ttu-id="1d973-117">Otro cliente es el cliente activo de este carácter o el carácter actual no es el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="1d973-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="1d973-118">3</span><span class="sxs-lookup"><span data-stu-id="1d973-118">3</span></span>     | <span data-ttu-id="1d973-119">El canal de entrada o salida de audio está ocupado actualmente, una aplicación está utilizando audio.</span><span class="sxs-lookup"><span data-stu-id="1d973-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="1d973-120">4</span><span class="sxs-lookup"><span data-stu-id="1d973-120">4</span></span>     | <span data-ttu-id="1d973-121">Se produjo un error no especificado en el proceso de inicialización del subsistema de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="1d973-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="1d973-122">Esto incluye la posibilidad de que no haya ningún motor de voz disponible que coincida con la configuración de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="1d973-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="1d973-123">5</span><span class="sxs-lookup"><span data-stu-id="1d973-123">5</span></span>     | <span data-ttu-id="1d973-124">El usuario ha deshabilitado la entrada de voz en las opciones de caracteres avanzadas.</span><span class="sxs-lookup"><span data-stu-id="1d973-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="1d973-125">6</span><span class="sxs-lookup"><span data-stu-id="1d973-125">6</span></span>     | <span data-ttu-id="1d973-126">Error al comprobar el estado de audio, pero el sistema no ha devuelto la causa del error.</span><span class="sxs-lookup"><span data-stu-id="1d973-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d973-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d973-127">Remarks</span></span>

<span data-ttu-id="1d973-128">Esta propiedad devuelve las condiciones necesarias para admitir la entrada de voz, incluido el estado del dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="1d973-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="1d973-129">Puede comprobar esta propiedad antes de llamar al método [**Listen**](listen-method.md) para garantizar mejor su éxito.</span><span class="sxs-lookup"><span data-stu-id="1d973-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="1d973-130">Cuando se habilita la entrada de voz en la hoja de propiedades del agente (opciones avanzadas de caracteres), al consultar esta propiedad se cargará el motor asociado, si aún no está cargado, y se iniciarán los servicios de voz.</span><span class="sxs-lookup"><span data-stu-id="1d973-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="1d973-131">Es decir, la clave de escucha está disponible y la sugerencia de escucha se puede mostrar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1d973-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="1d973-132">(La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.</span><span class="sxs-lookup"><span data-stu-id="1d973-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="1d973-133">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="1d973-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d973-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1d973-134">See Also</span></span>

[<span data-ttu-id="1d973-135">**Listen (método)**</span><span class="sxs-lookup"><span data-stu-id="1d973-135">**Listen method**</span></span>](listen-method.md)


 

 




