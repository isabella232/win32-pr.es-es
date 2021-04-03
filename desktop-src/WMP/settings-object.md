---
title: Objeto Settings (SDK de Windows Media Player)
description: El objeto de configuración proporciona una manera de modificar diversas opciones de configuración de Windows Media Player mediante el uso de las siguientes propiedades y métodos.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Objeto de configuración Windows Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "103904271"
---
# <a name="settings-object"></a><span data-ttu-id="57123-104">Objeto de configuración</span><span class="sxs-lookup"><span data-stu-id="57123-104">Settings Object</span></span>

<span data-ttu-id="57123-105">El objeto de **configuración** proporciona una manera de modificar diversas opciones de configuración de Windows Media Player mediante el uso de las siguientes propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="57123-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="57123-106">El objeto de **configuración** admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="57123-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="57123-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="57123-107">Property</span></span>                                                  | <span data-ttu-id="57123-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="57123-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57123-109">Automáticamente</span><span class="sxs-lookup"><span data-stu-id="57123-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="57123-110">Especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="57123-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="57123-111">balancea</span><span class="sxs-lookup"><span data-stu-id="57123-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="57123-112">Especifica o recupera el equilibrio estéreo actual.</span><span class="sxs-lookup"><span data-stu-id="57123-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="57123-113">baseURL</span><span class="sxs-lookup"><span data-stu-id="57123-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="57123-114">Especifica o recupera la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="57123-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="57123-115">defaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="57123-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="57123-116">Recupera el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="57123-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="57123-117">defaultFrame</span><span class="sxs-lookup"><span data-stu-id="57123-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="57123-118">Especifica o recupera el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **comando** .</span><span class="sxs-lookup"><span data-stu-id="57123-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="57123-119">enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="57123-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="57123-120">Especifica o recupera un valor que indica si los cuadros de diálogo de error se muestran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="57123-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="57123-121">invokeURLs</span><span class="sxs-lookup"><span data-stu-id="57123-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="57123-122">Especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="57123-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="57123-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="57123-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="57123-124">Recupera si un tipo de información especificado está disponible o se puede realizar una acción especificada.</span><span class="sxs-lookup"><span data-stu-id="57123-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="57123-125">mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="57123-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="57123-126">Recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="57123-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="57123-127">silenciar</span><span class="sxs-lookup"><span data-stu-id="57123-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="57123-128">Especifica o recupera un valor que indica si el audio está silenciado.</span><span class="sxs-lookup"><span data-stu-id="57123-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="57123-129">playCount</span><span class="sxs-lookup"><span data-stu-id="57123-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="57123-130">Especifica o recupera el número de veces que se reproducirá un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="57123-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="57123-131">Rate</span><span class="sxs-lookup"><span data-stu-id="57123-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="57123-132">Especifica o recupera la velocidad de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="57123-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="57123-133">volume</span><span class="sxs-lookup"><span data-stu-id="57123-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="57123-134">Especifica o recupera el volumen actual.</span><span class="sxs-lookup"><span data-stu-id="57123-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="57123-135">El objeto de **configuración** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="57123-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="57123-136">Método</span><span class="sxs-lookup"><span data-stu-id="57123-136">Method</span></span>                                                            | <span data-ttu-id="57123-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="57123-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="57123-138">getMode</span><span class="sxs-lookup"><span data-stu-id="57123-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="57123-139">Determina si el modo de bucle o el modo de orden aleatorio está activo.</span><span class="sxs-lookup"><span data-stu-id="57123-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="57123-140">requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="57123-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="57123-141">Solicita un nivel de acceso especificado a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="57123-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="57123-142">setMode</span><span class="sxs-lookup"><span data-stu-id="57123-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="57123-143">Establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="57123-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="57123-144">Se tiene acceso al objeto de **configuración** a través de la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="57123-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="57123-145">Object</span><span class="sxs-lookup"><span data-stu-id="57123-145">Object</span></span>                      | <span data-ttu-id="57123-146">Propiedad</span><span class="sxs-lookup"><span data-stu-id="57123-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="57123-147">Reproductor</span><span class="sxs-lookup"><span data-stu-id="57123-147">Player</span></span>](player-object.md) | [<span data-ttu-id="57123-148">settings</span><span class="sxs-lookup"><span data-stu-id="57123-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="57123-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="57123-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57123-150">**Referencia del modelo de objetos para scripting**</span><span class="sxs-lookup"><span data-stu-id="57123-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




