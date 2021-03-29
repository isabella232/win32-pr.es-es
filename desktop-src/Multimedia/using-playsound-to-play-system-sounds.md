---
title: Usar PlaySound para reproducir sonidos del sistema
description: Usar PlaySound para reproducir sonidos del sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- audio de onda, función PlaySound
- audio de onda, reproducir sonidos del sistema
- audio de onda, eventos de sonido
- Función PlaySound, reproducir sonidos del sistema
- Función PlaySound, eventos de sonido
- 'reproducir ondas de onda: sonidos del sistema de audio'
- eventos de sonido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904600"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="528bc-110">Usar PlaySound para reproducir sonidos del sistema</span><span class="sxs-lookup"><span data-stu-id="528bc-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="528bc-111">La función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) también reproducirá sonidos a los que se hace referencia mediante un KeyName en el registro.</span><span class="sxs-lookup"><span data-stu-id="528bc-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="528bc-112">Los usuarios pueden asignar sus propios sonidos a las alertas y advertencias del sistema, o bien a las acciones del usuario, como un clic del botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="528bc-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="528bc-113">Los sonidos que están asociados a las alertas y advertencias del sistema se denominan *eventos de sonido*.</span><span class="sxs-lookup"><span data-stu-id="528bc-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="528bc-114">Para reproducir un evento de sonido, llame a **PlaySound** con el parámetro *pszSound* que apunta a una cadena que contiene el nombre de la entrada del registro que identifica el sonido.</span><span class="sxs-lookup"><span data-stu-id="528bc-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="528bc-115">Por ejemplo, para reproducir el sonido asociado a la entrada "MouseClick" y esperar a que se complete el sonido antes de volver, use la siguiente instrucción:</span><span class="sxs-lookup"><span data-stu-id="528bc-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="528bc-116">Si la entrada del registro especificada o el archivo de audio de forma de onda que identifica no existe, o si el archivo no cabe en la memoria disponible, **PlaySound** reproduce el sonido predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="528bc-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="528bc-117">Los eventos de sonido que están predefinidos por el sistema pueden variar con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="528bc-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="528bc-118">La lista siguiente proporciona los eventos de sonido que se definen para todas las implementaciones de la API Win32:</span><span class="sxs-lookup"><span data-stu-id="528bc-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="528bc-119">SystemAsterisk</span><span class="sxs-lookup"><span data-stu-id="528bc-119">SystemAsterisk</span></span>
-   <span data-ttu-id="528bc-120">SystemExclamation</span><span class="sxs-lookup"><span data-stu-id="528bc-120">SystemExclamation</span></span>
-   <span data-ttu-id="528bc-121">SystemExit</span><span class="sxs-lookup"><span data-stu-id="528bc-121">SystemExit</span></span>
-   <span data-ttu-id="528bc-122">SystemHand</span><span class="sxs-lookup"><span data-stu-id="528bc-122">SystemHand</span></span>
-   <span data-ttu-id="528bc-123">SystemQuestion</span><span class="sxs-lookup"><span data-stu-id="528bc-123">SystemQuestion</span></span>
-   <span data-ttu-id="528bc-124">SystemStart</span><span class="sxs-lookup"><span data-stu-id="528bc-124">SystemStart</span></span>

<span data-ttu-id="528bc-125">Si una aplicación registra sus propios eventos de sonido, el usuario puede configurar el evento de sonido mediante la interfaz estándar del panel de control.</span><span class="sxs-lookup"><span data-stu-id="528bc-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="528bc-126">La aplicación debe registrar el evento de sonido mediante las funciones de registro estándar. para obtener más información, vea [Registry](../sysinfo/registry.md).</span><span class="sxs-lookup"><span data-stu-id="528bc-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="528bc-127">Las entradas pertenecen a la misma posición en la jerarquía del registro que el resto de los eventos de sonido.</span><span class="sxs-lookup"><span data-stu-id="528bc-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="528bc-128">Esta posición varía según la implementación de Win32.</span><span class="sxs-lookup"><span data-stu-id="528bc-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="528bc-129">El valor de datos adecuado también varía con la implementación de.</span><span class="sxs-lookup"><span data-stu-id="528bc-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="528bc-130">La función [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) siempre busca en el registro un KeyName que coincida con *lpszSound* antes de intentar cargar un archivo con este nombre.</span><span class="sxs-lookup"><span data-stu-id="528bc-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="528bc-131">La función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) acepta marcas que especifican la ubicación del sonido.</span><span class="sxs-lookup"><span data-stu-id="528bc-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 