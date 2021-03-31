---
title: Preparación de IAgentCharacter
description: Preparación de IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077718"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="d2b4e-103">IAgentCharacter::P redondear</span><span class="sxs-lookup"><span data-stu-id="d2b4e-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="d2b4e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2b4e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="d2b4e-105">Recupera los datos de animación de un carácter.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="d2b4e-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="d2b4e-107">Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="d2b4e-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="d2b4e-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="d2b4e-109">Valor que indica el tipo de datos de animación que se va a cargar y que debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2b4e-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="d2b4e-110">Value</span><span class="sxs-lookup"><span data-stu-id="d2b4e-110">Value</span></span>                                                           | <span data-ttu-id="d2b4e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2b4e-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d2b4e-112">**const sin signo Short** **Prepárese \_ Animation = 0;**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="d2b4e-113">Datos de animación de un carácter.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="d2b4e-114">**const unsigned short** ( **Estado de preparación) \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="d2b4e-115">Datos de estado de un carácter.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="d2b4e-116">**const unsigned short** ( **preparación) \_ Wave = 2**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="d2b4e-117">Archivo de sonido de un carácter (. WAV o. LWV) para la salida de voz.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d2b4e-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="d2b4e-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="d2b4e-119">El nombre de la animación o el estado.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-119">The name of the animation or state.</span></span>

<span data-ttu-id="d2b4e-120">El nombre de la animación se basa en el definido para el carácter cuando se guardó con el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="d2b4e-121">En el caso de los Estados, el valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2b4e-121">For states, the value can be one of the following:</span></span>



|                      |                                                 |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="d2b4e-122">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-122">**"Gesturing"**</span></span>      | <span data-ttu-id="d2b4e-123">Para recuperar todas las animaciones de estado de **gesturing** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-123">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="d2b4e-124">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-124">**"GesturingDown"**</span></span>  | <span data-ttu-id="d2b4e-125">Para recuperar animaciones **GesturingDown** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-125">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="d2b4e-126">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-126">**"GesturingLeft"**</span></span>  | <span data-ttu-id="d2b4e-127">Para recuperar animaciones **GesturingLeft** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-127">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="d2b4e-128">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-128">**"GesturingRight"**</span></span> | <span data-ttu-id="d2b4e-129">Para recuperar animaciones **GesturingRight** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-129">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="d2b4e-130">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-130">**"GesturingUp"**</span></span>    | <span data-ttu-id="d2b4e-131">Para recuperar animaciones **GesturingUp** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-131">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="d2b4e-132">**Conde**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-132">**"Hiding"**</span></span>         | <span data-ttu-id="d2b4e-133">Para recuperar las animaciones de estado **ocultas** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-133">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="d2b4e-134">**Oye**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-134">**"Hearing"**</span></span>        | <span data-ttu-id="d2b4e-135">Para recuperar las animaciones del estado de la **audición** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-135">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="d2b4e-136">**Inactivo**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-136">**"Idling"**</span></span>         | <span data-ttu-id="d2b4e-137">Para recuperar todas las animaciones de estado de **ralentí** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-137">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="d2b4e-138">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-138">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="d2b4e-139">Para recuperar todas las animaciones **IdlingLevel1** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-139">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="d2b4e-140">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-140">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="d2b4e-141">Para recuperar todas las animaciones **IdlingLevel2** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-141">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="d2b4e-142">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-142">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="d2b4e-143">Para recuperar todas las animaciones **IdlingLevel3** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-143">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="d2b4e-144">**Escucha**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-144">**"Listening"**</span></span>      | <span data-ttu-id="d2b4e-145">Para recuperar las animaciones de estado de **escucha** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-145">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="d2b4e-146">**Moverlo**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-146">**"Moving"**</span></span>         | <span data-ttu-id="d2b4e-147">Para recuperar todas las animaciones de estado en **movimiento** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-147">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="d2b4e-148">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-148">**"MovingDown"**</span></span>     | <span data-ttu-id="d2b4e-149">Para recuperar todas las animaciones en **movimiento** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-149">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="d2b4e-150">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-150">**"MovingLeft"**</span></span>     | <span data-ttu-id="d2b4e-151">Para recuperar todas las animaciones **MovingLeft** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-151">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="d2b4e-152">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-152">**"MovingRight"**</span></span>    | <span data-ttu-id="d2b4e-153">Para recuperar todas las animaciones **MovingRight** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-153">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="d2b4e-154">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-154">**"MovingUp"**</span></span>       | <span data-ttu-id="d2b4e-155">Para recuperar todas las animaciones **MovingUp** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-155">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="d2b4e-156">**Mostrar**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-156">**"Showing"**</span></span>        | <span data-ttu-id="d2b4e-157">Para recuperar las animaciones de estado **que se muestran** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-157">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="d2b4e-158">**Habla**</span><span class="sxs-lookup"><span data-stu-id="d2b4e-158">**"Speaking"**</span></span>       | <span data-ttu-id="d2b4e-159">Para recuperar las animaciones de estado de **habla** .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-159">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="d2b4e-160">Para. Archivos WAV, establezca *bszName* en la dirección URL o especificación de archivo para. Archivo WAV.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-160">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="d2b4e-161">Si la especificación no está completa, se interpreta como relativa a la especificación utilizada en el método [**Load**](https://www.bing.com/search?q=**Load**) .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-161">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="d2b4e-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="d2b4e-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="d2b4e-163">Un valor booleano que especifica si el servidor pone en cola la solicitud de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-163">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="d2b4e-164">**True** pone en cola la solicitud y hace que cualquier solicitud de animación que le siga espere hasta que se carguen los datos de animación que especifica.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-164">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="d2b4e-165">**False** recupera los datos de animación de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-165">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="d2b4e-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="d2b4e-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="d2b4e-167">Dirección de una variable que recibe el identificador de solicitud de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-167">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="d2b4e-168">Si carga un carácter mediante el protocolo HTTP (. ACF), debe usar el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para recuperar los datos de animación antes de poder reproducir la animación.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-168">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="d2b4e-169">No puede usar este método si cargó el carácter mediante el protocolo UNC (. Archivo de ACS).</span><span class="sxs-lookup"><span data-stu-id="d2b4e-169">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="d2b4e-170">Tampoco puede recuperar datos HTTP para un carácter mediante **Prepárese** Si cargó ese carácter mediante el protocolo UNC (. Archivo de caracteres de ACS).</span><span class="sxs-lookup"><span data-stu-id="d2b4e-170">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="d2b4e-171">Los datos de animación o de sonido recuperados con el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) se almacenan en la memoria caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-171">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="d2b4e-172">Las llamadas subsiguientes comprobarán la memoria caché y, si los datos de la animación ya están allí, el control cargará los datos directamente desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-172">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="d2b4e-173">Una vez cargados, los datos de animación o sonido se pueden reproducir con los métodos [**Play**](/windows/desktop/lwef/iagentcharacter--play) o [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-173">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="d2b4e-174">Puede especificar varias animaciones y Estados separándolos con comas.</span><span class="sxs-lookup"><span data-stu-id="d2b4e-174">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="d2b4e-175">Sin embargo, no se pueden mezclar tipos en la misma instrucción [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="d2b4e-175">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

