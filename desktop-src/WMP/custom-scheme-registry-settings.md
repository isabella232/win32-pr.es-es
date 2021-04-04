---
title: Configuración del registro de esquema personalizado
description: Configuración del registro de esquema personalizado
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, configuración del registro de esquema personalizado
- Media Player de Windows, esquemas
- Media Player de Windows, registro
- registro, configuración de esquema personalizado
- registro, esquemas
- registro, configuración para Windows Media Player
- esquemas
- configuración del registro de esquema personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075312"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="733b2-111">Configuración del registro de esquema personalizado</span><span class="sxs-lookup"><span data-stu-id="733b2-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="733b2-112">Los esquemas son protocolos personalizados.</span><span class="sxs-lookup"><span data-stu-id="733b2-112">Schemes are custom protocols.</span></span> <span data-ttu-id="733b2-113">Windows Media Player mantiene una lista de esquemas del registro en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="733b2-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="733b2-114">Cuando el usuario intenta reproducir un archivo multimedia digital, el reproductor comprueba primero si el SDK de Windows Media Format es compatible con el esquema.</span><span class="sxs-lookup"><span data-stu-id="733b2-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="733b2-115">Si no es así, el reproductor comprueba el esquema con la lista del registro.</span><span class="sxs-lookup"><span data-stu-id="733b2-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="733b2-116">Si se encuentra una coincidencia, el reproductor comprueba un valor que indica qué tecnología subyacente, o *tiempo de ejecución* (como Microsoft DirectShow o el SDK de Windows Media Format), se puede usar para reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="733b2-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="733b2-117">Si no se encuentra ninguna coincidencia, el reproductor presenta al usuario un cuadro de diálogo de advertencia que solicita permiso al usuario para intentar reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="733b2-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="733b2-118">Si transmite por secuencias archivos multimedia digitales mediante un esquema de protocolo personalizado, puede evitar que esta advertencia aparezca en el equipo del usuario registrando el esquema y proporcionando un valor para el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="733b2-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="733b2-119">La lista de esquemas se mantiene como un conjunto de claves del registro que coinciden con los esquemas registrados, sin los dos puntos y las dos barras diagonales (://).</span><span class="sxs-lookup"><span data-stu-id="733b2-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="733b2-120">Por ejemplo, la clave para el esquema wmhtml://, que se usa para transmitir multimedia enriquecidas, se denomina "wmhtml".</span><span class="sxs-lookup"><span data-stu-id="733b2-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="733b2-121">Se mantiene una lista independiente para el equipo local y para cada usuario.</span><span class="sxs-lookup"><span data-stu-id="733b2-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="733b2-122">En el caso del equipo local, las claves de esquema son subclaves de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="733b2-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="733b2-123">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ schemes\\**</span><span class="sxs-lookup"><span data-stu-id="733b2-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="733b2-124">Por ejemplo, la clave del esquema wmhtml://para el equipo local es:</span><span class="sxs-lookup"><span data-stu-id="733b2-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="733b2-125">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimedia \\ WMPlayer \\ schemes \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="733b2-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="733b2-126">Para cambiar los valores de esta clave o para crear una nueva subclave, el usuario actual debe ser administrador del equipo.</span><span class="sxs-lookup"><span data-stu-id="733b2-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="733b2-127">Para usuarios individuales, las claves de esquema son subclaves de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="733b2-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="733b2-128">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ schemes\\**</span><span class="sxs-lookup"><span data-stu-id="733b2-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="733b2-129">Por ejemplo, la clave del esquema wmhtml://para el usuario actual es:</span><span class="sxs-lookup"><span data-stu-id="733b2-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="733b2-130">**HKEY \_ Current \_ User \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ schemes \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="733b2-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="733b2-131">Al comprobar los esquemas registrados, el reproductor comprueba primero los valores ubicados en **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="733b2-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="733b2-132">Si no se encuentra ninguno para el esquema actual, el reproductor comprueba después los valores de **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="733b2-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="733b2-133">Si no se encuentra ninguno para el esquema actual, el reproductor muestra la advertencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="733b2-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="733b2-134">Cada subclave de esquema puede contener uno de los siguientes valores posibles para el *tiempo de ejecución*.</span><span class="sxs-lookup"><span data-stu-id="733b2-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="733b2-135">Value</span><span class="sxs-lookup"><span data-stu-id="733b2-135">Value</span></span> | <span data-ttu-id="733b2-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="733b2-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="733b2-137">6</span><span class="sxs-lookup"><span data-stu-id="733b2-137">6</span></span>     | <span data-ttu-id="733b2-138">Se representa mediante el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="733b2-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="733b2-139">7</span><span class="sxs-lookup"><span data-stu-id="733b2-139">7</span></span>     | <span data-ttu-id="733b2-140">Se representa mediante Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="733b2-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="733b2-141">Cambiar el valor *en tiempo de ejecución* de un esquema compatible con el SDK de Windows Media Format no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="733b2-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="733b2-142">El reproductor siempre usará el SDK de Windows Media Format como tiempo de ejecución para los esquemas compatibles con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="733b2-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="733b2-143">Este valor del registro está diseñado para permitir la configuración en tiempo de ejecución para esquemas personalizados.</span><span class="sxs-lookup"><span data-stu-id="733b2-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="733b2-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="733b2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="733b2-145">**Configuración del registro**</span><span class="sxs-lookup"><span data-stu-id="733b2-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




